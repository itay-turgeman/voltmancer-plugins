---
name: scriber
description: Live session scribe into Notion. Builds a running page under Lab → Scribe with a "Now" block + adaptive sections (Timeline, Findings, Decisions, Open Questions, References) as you work. Hybrid manual/auto. Use when you want a session's work — debug, SOP, research, anything — captured as a Notion page you can resume after distractions or promote into the Lab Pipeline as a Draft.
---

# /scriber — Live session → Notion page

Scribe a working session into a Notion page as it unfolds. Every meaningful exchange updates the page: current state at the top, history below. When distraction hits, come back and read 4 lines to know exactly where you were.

## When to use

| Situation | Use /scriber? |
|-----------|---------------|
| Multi-hour debug where you'll touch multiple units/files/angles | ✅ Yes |
| Writing an SOP as you do the thing once | ✅ Yes |
| Research rabbit hole across many sources | ✅ Yes |
| Single one-off command | ❌ No |
| Pure conversation with no artifacts to capture | ❌ No |

## Architecture

```
Notion: 🔬 Lab (Atlas) → ✍️ Scribe → 🔴 Active/📦 Archive → <session pages>
Local:  ~/.claude/scriber/sessions/<name>.json  (page_id + metadata)
```

**Lab parent page**: search Notion for `Lab (Atlas)` and use that page ID. The skill must never hard-code Notion IDs — always resolve by name at call time.

**Scaffolding is self-bootstrapping.** First `/scriber start` ensures `✍️ Scribe`, `🔴 Active`, `📦 Archive` exist; creates what's missing.

## Command surface

### `/scriber start <name>`

1. **Resolve Lab parent** — `notion-search` for `Lab (Atlas)`. Must exist; if not, abort with clear error.
2. **Ensure scaffolding** — search under Lab for child page `✍️ Scribe`. If missing, create it with children `🔴 Active` and `📦 Archive`.
3. **Guard duplicates** — search Active for existing `<name>`. If found, ask: resume, overwrite, or rename.
4. **Create page** under `🔴 Active` with the template below.
5. **Persist state** — write `~/.claude/scriber/sessions/<name>.json`:
   ```json
   {
     "name": "<name>",
     "page_id": "...",
     "lab_parent_id": "...",
     "scribe_parent_id": "...",
     "active_parent_id": "...",
     "archive_parent_id": "...",
     "created_at": "<ISO8601>",
     "last_scribed_at": "<ISO8601>"
   }
   ```
6. **Arm hybrid mode** — from this point in the session, treat every meaningful exchange as a scribe trigger (see *Hybrid auto-scribe* below).
7. **Confirm** — one line: `✍️ Scribing <name> → <Notion URL>`.

### Initial page template

```markdown
# <name>

## Now
- **Working on:** _(not yet set)_
- **Target:** _(not yet set)_
- **Last did:** started scribing
- **Next:** _(not yet set)_

## Timeline
- `<HH:MM>` — session started

## Findings

## Decisions

## Open Questions

## References
```

All sections are created at start. Empty sections are fine — they fill in as work happens.

### `/scriber <free-text note>`

Explicit entry. Itay is pinning something specific.

1. Read `last_scribed_at` from state; update it to now.
2. Parse the note for state changes (target switched, task changed, decision made) and update `## Now` accordingly.
3. Append to `## Timeline` with timestamp.
4. Route to other sections based on content (see *Routing rules* below).
5. Confirm with one line: `✍️ scribed: <first 60 chars>`.

Always update the page via `notion-update-page` with targeted edits — never rewrite the whole page unless `## Now` is changing.

### `/scriber resume <name>`

1. Load state file. If missing, search Notion for the page by name under Scribe.
2. Fetch the page, read just the `## Now` block.
3. Brief Itay in Atlas format:
   ```
   ## Resuming <name>
   **Working on:** ...
   **Target:** ...
   **Last did:** ...
   **Next:** ...

   Last scribed <relative time> ago.
   ```
4. Arm hybrid mode for the rest of the session.

### `/scriber promote [<name>]`

Bridge from Scribe to Lab Pipeline.

1. **Find Pipeline database** — search for `Pipeline` database under Lab (database, not page).
2. **Fetch schema** — get the data source so you have the real Project + Stage dropdown options.
3. **Infer Project** — read the scribe page content + name, match against Project options. If ambiguous, ask Itay with the *live* dropdown values (never hard-coded).
4. **Extract signal** — pull `## Now`, `## Findings`, `## Decisions`, `## Open Questions`, `## References`. **Omit `## Timeline`** — the raw timeline stays on the scribe page as the audit trail.
5. **Create Pipeline row**:
   - Title: `<name>`
   - Project: inferred value
   - Stage: `🔴 Draft`
   - Body: extracted sections, reformatted as a proper draft doc (not a log)
6. **Mark the scribe page** — prepend a callout at the top: `📤 Promoted to Pipeline → <link>`.
7. Report: `📤 Promoted <name> to Pipeline as Draft`.

### `/scriber archive [<name>]`

1. Move the scribe page from `🔴 Active` to `📦 Archive` via `notion-move-pages`.
2. Move state file `sessions/<name>.json` → `archive/<name>.json`.
3. Disarm hybrid mode for this session.

### `/scriber list`

Read `~/.claude/scriber/sessions/*.json` and render a table:

| Name | Started | Last scribed | URL |
|------|---------|--------------|-----|

### `/scriber` (no args)

- 0 active sessions → show: `No active scribes. Start one with /scriber start <name>`.
- 1 active session → show its `## Now` block inline.
- 2+ active sessions → `list` behavior.

## Hybrid auto-scribe — the running behavior

Once `start` or `resume` arms a session, follow these rules for the rest of the conversation:

### Scribe triggers

Scribe when one of these surfaces in an exchange:
- **Finding** — "X turned out to be Y", discovery, observation with evidence, measurement
- **Decision** — choosing an approach, ruling one out, committing to a path
- **Target change** — new unit/file/host/artifact entered focus
- **Action taken** — command run with outcome, file edited, experiment performed
- **Open question** — something parked, waiting on external info
- **Context switch** — pausing to check something else, distraction beginning

### Scribe filters

Do NOT scribe:
- Clarifying questions (theirs or yours)
- File reads or greps with no outcome
- Tool exploration / listing
- Acknowledgments ("ok", "yes", "got it")
- Plan discussion without commitment
- Trivial status updates
- Exchanges that are purely about scribing itself

### Scribe cadence

- At most one scribe pass per meaningful exchange, not per message.
- Batch related findings in the same pass when they surface together.
- If nothing scribe-worthy happens in a pass, stay silent — no scribe.

### Routing rules

| Content type | Section |
|--------------|---------|
| State change (what Itay is doing *right now*) | `## Now` — **rewrite**, not append |
| Any happening with a timestamp | `## Timeline` — append |
| Observation with evidence | `## Findings` — append bullet |
| A path chosen (especially over alternatives) | `## Decisions` — append bullet |
| Parked question, unknown | `## Open Questions` — append bullet |
| New host, IP, file path, URL, unit ID | `## References` — append bullet (dedupe against existing) |

One entry can hit multiple sections (e.g., sshing to a new unit both adds to References and updates Now). That's fine.

### `## Now` structure — rewrite, don't append

Always exactly 4 bullets:
- **Working on:** <current high-level task, one line>
- **Target:** <current unit/file/host/artifact, or "—" if N/A>
- **Last did:** <most recent concrete action, past tense>
- **Next:** <planned next action, or "TBD">

When updating, replace the entire `## Now` block using `notion-update-page` with the new four-line body.

## Notion mechanics

All Notion operations go through the `mcp__claude_ai_Notion__*` tools. Key ones:

| Need | Tool |
|------|------|
| Find Lab / pages by name | `notion-search` |
| Inspect page or database schema | `notion-fetch` |
| Create scaffolding or session page | `notion-create-pages` |
| Update page content (scribe) | `notion-update-page` |
| Move Active ↔ Archive | `notion-move-pages` |
| Create Pipeline row on promote | `notion-create-pages` with `data_source_id` parent |

**Always fetch before update.** When appending to a section, fetch the current page content first so you can preserve existing bullets and insert new ones in the right place.

**Never hard-code IDs.** Always resolve by name. IDs change across workspaces; the skill must stay portable.

## State file contract

`~/.claude/scriber/sessions/<name>.json` — one per active session:

```json
{
  "name": "CAN_Q",
  "page_id": "uuid",
  "lab_parent_id": "uuid",
  "scribe_parent_id": "uuid",
  "active_parent_id": "uuid",
  "archive_parent_id": "uuid",
  "created_at": "2026-04-24T20:15:00-07:00",
  "last_scribed_at": "2026-04-24T21:03:00-07:00",
  "project_hint": null
}
```

`archive/<name>.json` — archived sessions (same shape, moved on `/scriber archive`).

## Failure modes

| Failure | Response |
|---------|----------|
| `Lab (Atlas)` page not found | Abort with: `/scriber needs a Notion page called "Lab (Atlas)" — create it first or tell me where the staging workspace is.` |
| Notion MCP tools unavailable (e.g., `--print` mode) | Abort with: `/scriber requires an interactive session with Notion MCP. Cron/print mode can't scribe.` |
| Session name collision on `start` | Ask: resume existing / overwrite / rename |
| Page manually deleted but state file exists | On next scribe, detect 404 and offer: recreate from state / clear state |
| Pipeline database has no Project option matching session | Ask Itay with live dropdown values; never invent |

## Design notes

- **Why a "Now" block?** — STATUS.md at the top of every Atlas-org repo solves exactly this problem. Porting the pattern to Notion.
- **Why adaptive sections?** — Scriber is project-agnostic. A rigid schema fights SOPs; no structure fights debug sessions. Sections grow only when they earn their place.
- **Why timeline stays in Scribe, not Pipeline?** — Pipeline Drafts are polished docs for future reuse. Raw timelines rot into noise. Promote extracts signal.
- **Why one file per session in state?** — Greppable, archivable by moving the file, no lock contention between concurrent sessions on different names.
- **Why self-bootstrapping scaffolding?** — The skill survives machine moves, workspace resets, accidental deletions. No manual setup step to forget.
