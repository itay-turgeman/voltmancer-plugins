---
name: ticket
description: Mint a board ticket from the live session — expands a one-liner into a context-rich card via ~/atlas-hq/bin/hq-ticket and replies with the new id. Use when Itay says "/ticket <one-liner>", "ticket this", "mint a ticket for X", "make that a ticket", or when the session surfaces follow-up work worth tracking (bug found mid-session, scope too big for now, "later"). Resolves the right board from the current repo (sentry→SY, reaper→RP, lola→LO, ~/atlas/ios→OR, otherwise→HQ).
---

# /ticket — session context → board card, zero CLI for Itay

Turn the current session's context into a properly-noted ticket on the right
atlas-hq board. Itay says what he wants tracked; you do the distilling, the
minting, and the reply. He never types a command.

## Flow

### 1. Resolve the board from where you are

| Current repo / cwd | `--board` | Prefix |
|--------------------|-----------|--------|
| `~/sentry` | `sentry` | SY |
| `~/reaper` | `reaper` | RP |
| `~/lola` | `lola` | LO |
| `~/atlas/ios` (cwd under it) | `orb` | OR |
| `~/atlas` (life-admin heads) | `hydra` | HY |
| `~/atlas-hq`, anywhere else, or unclear | `hq` | HQ |

Sanity-check with `~/atlas-hq/bin/hq-ticket board <name>` if unsure — it
prints the registry entry (name, prefix, board file, dispatch cwd). If the
*subject* of the ticket clearly belongs to a different project than the cwd
(e.g. a sentry bug discovered while in atlas), the subject wins.

### 2. Expand the one-liner into a real ticket

Distill the live session — not just the one-liner — into:

- **Title**: imperative, specific ("Fix servo jitter on PCA9685 channel 3",
  not "servo bug")
- **Notes** (3–5 bullets, each a `--note`): root cause or context the session
  uncovered, exact file paths and functions involved, repro steps if a bug,
  chosen approach if one was discussed, acceptance — what done looks like.

The bar: **a cold agent with zero session context can build from the notes
alone.** A bare title is a failed mint.

### 3. Mint

```bash
~/atlas-hq/bin/hq-ticket new "<title>" --board <board> \
  --note "context: ..." \
  --note "files: ..." \
  --note "acceptance: ..."
```

Prints the new id (e.g. `SY-007`). Never hand-edit a board file
(`TODO.md`/`BOARD.md`/`HYDRA.md`) — `hq-ticket` and the deck API are the
only writers.

### 4. Reply + offer dispatch

Reply with the id and title. The card is already live on the deck's project
page (:8400). Offer to dispatch:

```bash
~/atlas-hq/bin/hq-dispatch <ID>
```

spawns a dedicated agent on the card (tmux session `tickets`). Don't dispatch
unless Itay says yes — minting and starting work are separate decisions.

## No argument?

`/ticket` with no one-liner means "ticket the thing we were just talking
about" — pick the most recent ticket-worthy item from the session and confirm
the title with Itay before minting only if genuinely ambiguous.
