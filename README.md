<div align="center">

# 🔌 VOLTMANCER · PLUGINS 🔌

### *Cross-machine Claude Code tools that travel with the human · one `/plugin install` away · zero portability tax*

</div>

<div align="center">

![phase](https://img.shields.io/badge/⚡_PHASE-1_marketplace_live-FFD75F?style=for-the-badge&labelColor=1a1a2e)
![surface](https://img.shields.io/badge/🔌_SURFACE-claude_code_plugins-87AFFF?style=for-the-badge&labelColor=1a1a2e)
![status](https://img.shields.io/badge/💚_STATUS-1_plugin_shipped-2ECC71?style=for-the-badge&labelColor=1a1a2e)

![install](https://img.shields.io/badge/🛒_install-/plugin_marketplace_add-FF87D7?style=flat-square&labelColor=1a1a2e)
![visibility](https://img.shields.io/badge/🌍_visibility-public-2ECC71?style=flat-square&labelColor=1a1a2e)
![brand](https://img.shields.io/badge/⚡_brand-voltmancer-FF5FAF?style=flat-square&labelColor=1a1a2e)
![style](https://img.shields.io/badge/🎨_style-atlas_color_language-FF5FAF?style=flat-square&labelColor=1a1a2e)
![works_on](https://img.shields.io/badge/🖥_runs_on-linux_•_macOS_•_anywhere_claude_runs-87CEEB?style=flat-square&labelColor=1a1a2e)
![cost](https://img.shields.io/badge/💵_cost-free-D7AFFF?style=flat-square&labelColor=1a1a2e)

</div>

---

<table align="center" width="100%">
<tr>
<td width="50%" bgcolor="#1a1a2e" align="center">

### ⚡ THE 60-SECOND PITCH

A **Claude Code plugin marketplace** that turns my best
single-machine workflows into one-line installs.

Skills, agents, hooks, commands, MCPs — bundled,
versioned, **portable across every box I touch.**

Linux desktop. Work Mac. Future laptop.
**Same `/scriber`, same muscle memory.**

</td>
<td width="50%" bgcolor="#3a1a2e" align="center">

### 🎯 THE 5-SECOND BET

Tools that only live on one machine die on that machine.

Claude Code's plugin contract is **good enough now**
to make personal automation **survive a reformat,
a new job, a new continent.**

Voltmancer is the brand carrying that promise.

</td>
</tr>
</table>

---

## ⚡ Live Status — *what's actually shipped right now*

> Last updated: **2026-04-28** · phase **1** · `marketplace live · 1 plugin shipped`

<table>
<tr>
  <td align="center" bgcolor="#ffd75f"><b>🚦 PHASE</b><br/><font color="#000">1 — Marketplace</font></td>
  <td align="center" bgcolor="#87afff"><b>🎯 ACTIVE</b><br/><font color="#000">scriber v0.1.0</font></td>
  <td align="center" bgcolor="#2ecc71"><b>💚 BLOCKED</b><br/><font color="#000">— nothing</font></td>
  <td align="center" bgcolor="#ff87d7"><b>📍 NEXT</b><br/><font color="#000">v0.2 polish + plugin #2</font></td>
</tr>
</table>

<br/>

| | |
|---|---|
| **Shipped plugins** | `scriber` v0.1.0 — live session → Notion page |
| **In flight** | scaffolding for plugin #2 candidate · marketplace `update` rehearsal |
| **Last activity** | 2026-04-28 — README v3 visual upgrade |
| **Repo** | `git@github-atlas:itay-turgeman/voltmancer-plugins.git` (public) |
| **Install command** | `/plugin marketplace add github:itay-turgeman/voltmancer-plugins` |

### 📍 You are here on the roadmap

```mermaid
flowchart LR
    P0[Phase 0<br/><b>📜 Concept</b>]:::output
    P1[Phase 1<br/><b>🛒 Marketplace</b>]:::active
    P2[Phase 2<br/>📦 Plugin Pack]:::deferred
    P3[Phase 3<br/>🤖 Agent Bundles]:::deferred
    P4[Phase 4<br/>🔗 MCP Bundles]:::deferred
    P5[Phase 5<br/>🌐 Public Discoverability]:::deferred

    P0 --> P1 --> P2 --> P3 --> P4 --> P5

    classDef output   fill:#2ecc71,stroke:#000,stroke-width:2px,color:#000
    classDef active   fill:#ffd75f,stroke:#000,stroke-width:4px,color:#000
    classDef deferred fill:#1a1a1a,stroke:#666,stroke-width:1px,color:#888
```

<details>
<summary><b>📜 Changelog</b> (click to expand)</summary>

- **2026-04-28** — README v3 ADHD-grade visual upgrade (mindmap, sankey, gantt, journey, sequence, pie, state, timeline)
- **2026-04-24** — Repo bootstrapped, marketplace.json declared, `scriber` v0.1.0 published, first cross-machine `/plugin install` confirmed working

</details>

---

## 🗺️ The whole marketplace in one picture

> 🎯 If you read **nothing else**, this mindmap is the project. Every other section expands one branch.

```mermaid
mindmap
  root((🔌 Voltmancer<br/>Plugins))
    🛒 Marketplace
      marketplace.json
      owner block
      plugin registry
      "/plugin install"
    📦 Shipped Plugins
      ✍️ scriber 🟢
        live session
        Notion page
        Lab → Scribe
    🧰 Plugin Surfaces
      📜 Skills
      🤖 Agents
      🪝 Hooks
      🎛 Commands
      🔗 MCP Servers
    🌍 Cross-Machine
      Linux desktop
      Work Mac
      Future laptop
      Anywhere Claude runs
    ⚡ Voltmancer Brand
      Creative identity
      Public-facing
      Distinct from Atlas
      Distinct from Itai Turgeman
    🛣 Future Plugins
      Voice tools?
      Smart-home bridge?
      Dev ergonomics?
      "TBD by recurrence"
```

---

## 📑 Table of Contents

| | Section | Visual flavor |
|---|---------|--------------|
| 1 | [⚡ Why This Exists](#-why-this-exists) | quadrant |
| 2 | [⚡ The Voltmancer Brand](#-the-voltmancer-brand) | flowchart TD |
| 3 | [🛒 The Plugin Catalog](#-the-plugin-catalog) | catalog cards |
| 4 | [🧰 Plugin Anatomy](#-plugin-anatomy) | flowchart TD + subgraphs |
| 5 | [📦 Repo Architecture](#-repo-architecture) | file tree + flow |
| 6 | [🛒 Install Flow](#-install-flow) | flowchart LR |
| 7 | [♻️ Plugin Lifecycle](#-plugin-lifecycle) | sequenceDiagram |
| 8 | [🔁 Plugin States](#-plugin-states) | stateDiagram-v2 |
| 9 | [📅 Roadmap](#-roadmap) | gantt + pie |
| 10 | [🕰️ Project Timeline](#-project-timeline) | timeline |
| 11 | [🌅 A Day in the Life](#-a-day-in-the-life) | journey |
| 12 | [🚫 What We Will NOT Build](#-what-we-will-not-build) | table |
| 13 | [🛠️ Tech Stack](#-tech-stack) | flowchart TD |
| 14 | [🏢 Org Position](#-org-position) | flowchart TD |
| 15 | [🤝 Contributing](#-contributing) | sequence + checklist |
| 16 | [📖 Glossary](#-glossary) | table |

### 🎨 Diagram legend

| | | | | |
|---|---|---|---|---|
| ![](https://placehold.co/16x16/ffd75f/ffd75f.png) **gold** = active focus | ![](https://placehold.co/16x16/ff5faf/ff5faf.png) **magenta** = root / brand | ![](https://placehold.co/16x16/87afff/87afff.png) **sky** = primary subsystem | ![](https://placehold.co/16x16/ff87d7/ff87d7.png) **pink** = flow / verb | ![](https://placehold.co/16x16/af87ff/af87ff.png) **purple** = data / state |
| ![](https://placehold.co/16x16/87ffff/87ffff.png) **cyan** = external API | ![](https://placehold.co/16x16/87d7af/87d7af.png) **mint** = support / glue | ![](https://placehold.co/16x16/d4ac0d/d4ac0d.png) **dark gold** = physical / hardware | ![](https://placehold.co/16x16/2ecc71/2ecc71.png) **green** = shipped | ![](https://placehold.co/16x16/ff5f5f/ff5f5f.png) **red** = critical |

---

## ⚡ Why This Exists

Personal automation has a **portability problem**. Every clever shell function, every dotfile, every "I'll remember to copy this" script — they all rot the second you touch a new machine.

Claude Code's plugin contract solves this for one specific class of tooling: **agentic workflows.** A plugin is a self-contained bundle of skills, agents, hooks, commands, and MCP servers, distributed via a `marketplace.json`, installed by name, versioned by tag.

Voltmancer is the brand that carries those bundles **across every machine the human touches.**

### 📈 Where this sits vs other distribution paths

```mermaid
quadrantChart
    title Portability vs Personal-Fit
    x-axis Generic --> Personal
    y-axis One Machine --> Cross Machine
    quadrant-1 The Sweet Spot 🎯
    quadrant-2 Public OSS (general)
    quadrant-3 Personal scripts (rotting)
    quadrant-4 Dotfiles repo (manual sync)
    Voltmancer Plugins: [0.85, 0.9]
    Anthropic Plugins: [0.2, 0.95]
    Community Plugins: [0.4, 0.85]
    Atlas (Itay's brain): [0.95, 0.15]
    Personal shell aliases: [0.95, 0.25]
    Stowed dotfiles: [0.7, 0.55]
    One-off bash scripts: [0.6, 0.1]
```

> 🎯 **THIS LINE** — Voltmancer occupies the **personal-fit + cross-machine** quadrant. Anthropic's official plugins are great but generic. Atlas is hyper-personal but locked to a Linux box full of secrets. Voltmancer is *my* tools, *anywhere I run Claude*.

### 🪜 The portability ladder

```mermaid
flowchart BT
    L1["<b>1. Shell aliases</b><br/>locked to one machine<br/>die in a reformat"]:::critical
    L2["<b>2. Dotfiles repo</b><br/>manual sync<br/>no versioning of behavior"]:::warning
    L3["<b>3. Custom skills</b><br/>per-repo CLAUDE.md<br/>still single-repo bound"]:::secondary
    L4["<b>🎯 4. Plugin marketplace</b><br/>versioned · installable<br/>discoverable · shareable"]:::active

    L1 --> L2 --> L3 --> L4

    classDef active    fill:#ffd75f,stroke:#000,stroke-width:3px,color:#000
    classDef secondary fill:#1a2e44,stroke:#87afff,stroke-width:1px,color:#87d7ff
    classDef warning   fill:#3a2a14,stroke:#ff9f43,stroke-width:1px,color:#ffd7af
    classDef critical  fill:#3a1a1a,stroke:#ff5f5f,stroke-width:2px,color:#ffafaf
```

**Most personal automation lives at L1.** Voltmancer forces it up to L4. **That's the move.**

---

## ⚡ The Voltmancer Brand

Itay runs three identities, on purpose. Each one carries a different kind of work.

```mermaid
flowchart TD
    H["<b>👤 Itay Turgeman</b><br/>real human · one body · three voices"]:::root

    H --> A["<b>💼 Itai Turgeman</b><br/>career / dev<br/>resume · LinkedIn · GitHub commits"]:::primary
    H --> V["<b>⚡ Voltmancer</b><br/>creative / social / public tooling<br/>this repo · YouTube · X · IG"]:::active
    H --> G["<b>🤖 Garage Robotics</b><br/>hardware brand<br/>Sentry Kickstarter · the trunk"]:::secondary

    V --> P["<b>🔌 voltmancer-plugins</b><br/>this marketplace"]:::flow
    V --> S["<b>🎙 future creator surfaces</b><br/>(voice / video / livestream)"]:::deferred

    classDef root      fill:#1a1a2e,stroke:#ff5faf,stroke-width:3px,color:#ff87d7
    classDef active    fill:#ffd75f,stroke:#000,stroke-width:3px,color:#000
    classDef primary   fill:#1e3a8a,stroke:#87afff,stroke-width:2px,color:#fff
    classDef secondary fill:#1a2e44,stroke:#87afff,stroke-width:1px,color:#87d7ff
    classDef flow      fill:#3a1a2e,stroke:#ff87d7,stroke-width:2px,color:#ffafd7
    classDef deferred  fill:#1a1a1a,stroke:#666,stroke-width:1px,color:#888
```

> 📌 **Why this repo lives under the Voltmancer name** — it's *public* and it's *personal*. Atlas is private and personal. Garage Robotics is public and product-focused. Voltmancer is where the loose, creative, "look what I made for myself and you can use it too" tools live.

---

## 🛒 The Plugin Catalog

### 🥧 What share each plugin type takes today

> Where the marketplace's mass currently sits. As more plugins ship, the wedge shifts — most likely toward agents and hooks.

```mermaid
pie title Marketplace Surface Mix (today)
    "📜 Skills" : 1
    "🤖 Agents" : 0
    "🪝 Hooks" : 0
    "🎛 Commands" : 0
    "🔗 MCP Servers" : 0
```

> 💡 The marketplace is intentionally **thin and honest**. One plugin, one surface. We add when a tool *recurs* across 3+ machines — not before.

### 📦 Plugin cards

<table>
<tr>
  <td width="50%" bgcolor="#1a1a2e" align="left" valign="top">

**✍️ scriber** · `v0.1.0` · 🟢 shipped

> Live session scribe into Notion. Builds a running page under `Lab → Scribe` with a `Now` block + adaptive sections (Timeline, Findings, Decisions, Open Questions, References) as you work. Hybrid manual/auto. Promotable to Lab Pipeline as a Draft.

| | |
|---|---|
| Surface | `📜 skill` |
| Trigger | `/scriber start <name>` |
| Backend | Notion MCP (account-scoped) |
| State dir | `~/.claude/scriber/sessions/` |

  </td>
  <td width="50%" bgcolor="#1a1a1a" align="left" valign="top">

**(slot reserved)** · `v—` · ⏸ deferred

> Next plugin lands when a workflow recurs across **≥3 machines**. Until then, the slot stays honest-empty. Candidates floating: voice-to-action capture, smart-home bridge for non-Atlas hosts, dev-ergonomics polish.

| | |
|---|---|
| Surface | TBD |
| Trigger | TBD |
| Status | candidate pool only |
| Bar to enter | "I missed it on machine #2" |

  </td>
</tr>
</table>

---

## 🧰 Plugin Anatomy

A Claude Code plugin is a directory with **five possible surfaces**. Voltmancer's plugins use whichever fit.

```mermaid
flowchart TD
    Root["<b>📦 plugin directory</b><br/>e.g. scriber/"]:::root

    subgraph Manifest["📋 Manifest — required"]
        M[".claude-plugin/plugin.json<br/>name · description · version · author"]:::primary
    end

    subgraph Surfaces["🧰 Surfaces — pick what fits"]
        SK["<b>📜 skills/</b><br/>SKILL.md per skill<br/>YAML frontmatter + body<br/>(/scriber)"]:::active
        AG["<b>🤖 agents/</b><br/>per-agent .md<br/>focused subagents"]:::secondary
        CM["<b>🎛 commands/</b><br/>slash commands<br/>parametric"]:::secondary
        HK["<b>🪝 hooks/</b><br/>PreToolUse · PostToolUse · Stop<br/>event-driven automation"]:::flow
        MC["<b>🔗 mcp/</b><br/>stdio / SSE / HTTP servers<br/>external tool bridges"]:::external
    end

    Root --> Manifest
    Root --> Surfaces
    Manifest -.declares.-> Surfaces

    classDef root      fill:#1a1a2e,stroke:#ff5faf,stroke-width:3px,color:#ff87d7
    classDef active    fill:#ffd75f,stroke:#000,stroke-width:3px,color:#000
    classDef primary   fill:#1e3a8a,stroke:#87afff,stroke-width:2px,color:#fff
    classDef secondary fill:#1a2e44,stroke:#87afff,stroke-width:1px,color:#87d7ff
    classDef flow      fill:#3a1a2e,stroke:#ff87d7,stroke-width:2px,color:#ffafd7
    classDef external  fill:#1a3a3a,stroke:#87ffff,stroke-width:1px,color:#87ffff
```

### 🧭 When to reach for which surface

| Surface | Use when | Don't use when |
|---------|----------|----------------|
| 📜 **Skill** | Multi-step workflow with named entry point a human would type | One-off explorations |
| 🤖 **Agent** | Focused subagent for a recurring scoped task | The work needs full session context |
| 🎛 **Command** | Parametric slash command, no decision tree | Workflow needs a state machine |
| 🪝 **Hook** | Behavior fires automatically on a Claude Code event | Behavior should be user-initiated |
| 🔗 **MCP** | Bridging an external service / API the plugin owns | Account-scoped MCP already covers it |

> 🎯 **Voltmancer's bias** — start with skills, graduate to agents when scope sharpens, add hooks only when the behavior should be silent and automatic. MCPs only if the plugin truly owns the integration.

---

## 📦 Repo Architecture

The marketplace is just a flat directory of plugins plus one manifest.

```
voltmancer-plugins/
├── 📋 .claude-plugin/
│   └── marketplace.json       ← the registry · owner block + plugin entries
├── ✍️ scriber/
│   ├── 📋 .claude-plugin/
│   │   └── plugin.json        ← name · description · version · author
│   └── 📜 skills/
│       └── scriber/
│           └── SKILL.md       ← the actual skill body + YAML frontmatter
├── 📜 README.md               ← this file
└── 🚫 .gitignore
```

### 🔁 How the manifest stitches it together

```mermaid
flowchart LR
    MP["<b>📋 marketplace.json</b><br/>owner + plugins[]"]:::primary
    PM["<b>📋 plugin.json</b><br/>per-plugin metadata"]:::primary
    SK["<b>📜 SKILL.md</b><br/>frontmatter + body"]:::flow
    CC["<b>🤖 Claude Code</b><br/>discovers via /plugin"]:::active

    MP -->|points to| PM
    PM -->|registers| SK
    CC -->|reads| MP
    CC -->|reads| PM
    CC -->|loads| SK

    classDef active   fill:#ffd75f,stroke:#000,stroke-width:3px,color:#000
    classDef primary  fill:#1e3a8a,stroke:#87afff,stroke-width:2px,color:#fff
    classDef flow     fill:#3a1a2e,stroke:#ff87d7,stroke-width:2px,color:#ffafd7
```

> 📌 **Why two manifests** — `marketplace.json` is the *outer* registry one repo can publish; `plugin.json` is the *inner* contract one plugin satisfies. The marketplace can host many plugins; each plugin can be installed independently.

---

## 🛒 Install Flow

The single most important user journey. From "fresh machine" to "/scriber works" in three commands.

```mermaid
flowchart LR
    U["<b>👤 Human</b><br/>fresh Claude Code session"]:::active
    A["<b>🛒 marketplace add</b><br/>github:itay-turgeman/<br/>voltmancer-plugins"]:::flow
    I["<b>📥 plugin install</b><br/>scriber@voltmancer-plugins"]:::flow
    R["<b>♻️ runtime registers</b><br/>/scriber discovered<br/>frontmatter parsed"]:::primary
    D["<b>✅ /scriber start &lt;name&gt;</b><br/>works in every session"]:::output

    U --> A --> I --> R --> D

    classDef active   fill:#ffd75f,stroke:#000,stroke-width:3px,color:#000
    classDef primary  fill:#1e3a8a,stroke:#87afff,stroke-width:2px,color:#fff
    classDef flow     fill:#3a1a2e,stroke:#ff87d7,stroke-width:2px,color:#ffafd7
    classDef output   fill:#2ecc71,stroke:#000,stroke-width:2px,color:#000
```

### 🖥 Install — fresh machine

```bash
# Inside Claude Code:
/plugin marketplace add github:itay-turgeman/voltmancer-plugins
/plugin install scriber@voltmancer-plugins
```

That's it. The skill registers as `/scriber` and is available in every session.

### 🧪 Local install — for testing before push

```bash
/plugin marketplace add ~/voltmancer-plugins
/plugin install scriber@voltmancer-plugins
```

### ♻️ Updating

```bash
/plugin marketplace update voltmancer-plugins
/plugin update scriber
```

> 💡 The whole point of this surface — *muscle memory transfers across machines*. Same three commands, same outcome, every box.

---

## ♻️ Plugin Lifecycle

The protocol between the human, the marketplace, and the runtime.

```mermaid
sequenceDiagram
    participant H as 👤 Human
    participant CC as 🤖 Claude Code
    participant MP as 🛒 Marketplace
    participant GH as 🐙 GitHub
    participant FS as 💾 Local cache

    H->>CC: /plugin marketplace add github:...
    CC->>GH: clone repo
    GH-->>CC: marketplace.json + plugins/
    CC->>FS: cache marketplace
    CC-->>H: ✅ marketplace registered

    H->>CC: /plugin install scriber@voltmancer-plugins
    CC->>MP: resolve plugin entry
    MP-->>CC: scriber path + version
    CC->>FS: install plugin → ~/.claude/plugins/
    CC->>CC: parse plugin.json + skills/
    CC-->>H: ✅ /scriber registered

    Note over H,FS: ─── time passes · plugin updated upstream ───

    H->>CC: /plugin marketplace update voltmancer-plugins
    CC->>GH: pull latest
    GH-->>CC: new commits
    CC->>FS: refresh cache

    H->>CC: /plugin update scriber
    CC->>FS: install new version
    CC-->>H: ✅ scriber upgraded
```

---

## 🔁 Plugin States

Every plugin in the marketplace lives one of these states. Today scriber is `Live`.

```mermaid
stateDiagram-v2
    [*] --> Candidate: idea recurs across 3+ machines
    Candidate --> Drafting: scaffolded under <name>/
    Drafting --> Review: manifest valid · skill loads<br/>local install works
    Review --> Live: pushed · registered in marketplace.json<br/>installed on a 2nd machine
    Live --> Patched: bug fix bumps patch
    Patched --> Live: marketplace update lands
    Live --> Deprecated: superseded · contract broke
    Deprecated --> Archived: removed from marketplace.json<br/>code retained for history
    Archived --> [*]

    note right of Live
        🟢 The healthy state
        scriber is here
    end note

    note right of Candidate
        ⏸ Idea pool
        bar to leave: 3-machine recurrence
    end note
```

| State | Meaning | Color |
|-------|---------|-------|
| `Candidate` | Idea floating; not yet justified | gray |
| `Drafting` | Scaffolded locally; not in marketplace.json | yellow |
| `Review` | Local install verified end-to-end | sky |
| `Live` | Published; installable from GitHub | 🟢 green |
| `Patched` | Mid-update; transient | pink |
| `Deprecated` | Will be removed | 🟠 orange |
| `Archived` | Removed from registry; commit history retained | ⚫ dark |

---

## 📅 Roadmap

### 🗓️ As a Gantt — see the actual time shape

```mermaid
gantt
    title Voltmancer Plugins Roadmap (estimated durations)
    dateFormat  YYYY-MM-DD
    axisFormat  %b %Y

    section 🛒 Phase 1 — Marketplace
    Repo bootstrap                  :done,    p1a, 2026-04-24, 1d
    scriber v0.1.0 ship             :done,    p1b, 2026-04-24, 1d
    README v3 visual upgrade        :active,  p1c, 2026-04-28, 2d

    section 📦 Phase 2 — Plugin Pack
    scriber v0.2 polish             :         p2a, after p1c, 14d
    Plugin #2 (TBD)                 :         p2b, after p2a, 21d
    Plugin #3 (TBD)                 :         p2c, after p2b, 21d

    section 🤖 Phase 3 — Agent Bundles
    First scoped agent              :         p3a, after p2c, 21d
    Agent + skill combo plugin      :         p3b, after p3a, 21d

    section 🔗 Phase 4 — MCP Bundles
    First MCP-bearing plugin        :         p4a, after p3b, 30d

    section 🌐 Phase 5 — Public Discoverability
    Landing copy + screenshots      :         p5a, after p4a, 14d
    Voltmancer creator surface tie  :         p5b, after p5a, 21d
```

### 🥧 Phase 2 attention budget — where the next chunk of effort goes

```mermaid
pie title Phase 2 Attention Budget
    "✍️ scriber polish (v0.2)" : 30
    "📦 Plugin #2 build" : 30
    "📦 Plugin #3 build" : 20
    "🛒 Marketplace UX (docs, /update flow)" : 10
    "🧪 Cross-machine smoke tests" : 10
```

> 📌 **The bar to add a plugin** — it must already exist as friction across **3+ machines**. No speculative bundles. No "wouldn't it be cool" plugins. The marketplace stays honest.

---

## 🕰️ Project Timeline

```mermaid
timeline
    title Voltmancer Plugins Project Timeline
    2026-04-24 : Repo bootstrapped
               : marketplace.json declared
               : scriber v0.1.0 published
               : Cross-machine /plugin install confirmed
    2026-04-28 : README v3 ADHD-grade visual upgrade
               : 9 distinct Mermaid diagram types
    2026-05-?? : scriber v0.2 polish 🎯
               : Plugin #2 candidate selected
    2026-06-?? : Phase 2 Plugin Pack complete
               : Phase 3 Agent Bundles begins
```

---

## 🌅 A Day in the Life

> *The journey from "new laptop in box" to "all my muscle memory works." This is what the marketplace exists to make trivial.*

```mermaid
journey
    title Fresh-Machine Setup with Voltmancer
    section 📦 Unbox
      Open laptop                         : 5: Itay
      Install Claude Code                 : 4: Itay
    section 🛒 Marketplace
      /plugin marketplace add github:...  : 5: Itay
      /plugin install scriber             : 5: Itay
    section ✍️ First Use
      /scriber start migration-day        : 5: Itay
      Notion page auto-created            : 5: Scriber, Notion
      Run live notes through the day      : 4: Itay, Scriber
    section 🎯 Resume tomorrow
      Open laptop, "where was I"          : 4: Itay
      Read Now block, instant context     : 5: Itay
```

---

## 🚫 What We Will NOT Build

| Won't build | Why |
|-------------|-----|
| Atlas-internal automation as plugins | Atlas stays private + Linux-only; secrets don't travel |
| Garage Robotics product code | Wrong brand · wrong audience · wrong distribution |
| Auth-bearing plugins (API keys baked in) | Account-scoped MCPs already carry credentials; plugins must stay credential-free |
| Plugins that need a backing service we don't run | Portability dies the moment a plugin needs `voltmancer-cloud.com` |
| Speculative "wouldn't it be cool" plugins | Bar to publish: friction recurs across **3+ machines** |
| One-machine niche tools | If it only works on the Linux box, it belongs in `~/atlas/` not here |
| Closed-source plugins | The marketplace is public — closed code defeats the brand promise |
| Forks of upstream Anthropic plugins | Use upstream; don't fragment the ecosystem |

> ⚠️ Most personal-tool repos die because they accumulate **everything the author ever wrote.** Voltmancer's bar is deliberate scarcity — only what survives across machines, only what justifies a `/plugin install`.

---

## 🛠️ Tech Stack

> 🎯 **The stack is intentionally tiny.** Markdown + JSON + the Claude Code runtime. No build step. No package manager. The plugin contract IS the platform.

```mermaid
flowchart TD
    User["<b>👤 USER LAYER</b><br/>Itay · any future user with Claude Code"]:::active
    CC["<b>🤖 RUNTIME</b><br/>Claude Code · /plugin command surface · auto-discovery"]:::root

    subgraph Plugin["📦 PLUGIN LAYER — what we author"]
        direction LR
        Manifest[("📋 <b>Manifest</b><br/>plugin.json<br/>marketplace.json<br/><i>JSON</i>")]:::data
        Skills[("📜 <b>Skill bodies</b><br/>SKILL.md<br/>YAML frontmatter<br/><i>Markdown</i>")]:::data
        Agents[("🤖 <b>Agent specs</b><br/><i>(future)</i>")]:::deferred
        Hooks[("🪝 <b>Hook configs</b><br/><i>(future)</i>")]:::deferred
        MCP[("🔗 <b>MCP servers</b><br/><i>(future)</i>")]:::deferred
    end

    Distribution["<b>🌐 DISTRIBUTION</b><br/>GitHub · public repo · clone-on-add<br/>Tag-based versioning"]:::external
    State["<b>💾 STATE LAYER</b><br/>~/.claude/plugins/ (installed)<br/>~/.claude/&lt;plugin&gt;/ (per-plugin state)"]:::support

    User -->|invokes| CC
    CC -->|reads| Plugin
    Plugin -->|hosted on| Distribution
    CC -->|caches in| State

    classDef root      fill:#1a1a2e,stroke:#ff5faf,stroke-width:3px,color:#ff87d7
    classDef active    fill:#ffd75f,stroke:#000,stroke-width:3px,color:#000
    classDef data      fill:#2a1a3a,stroke:#af87ff,stroke-width:2px,color:#d7afff
    classDef external  fill:#1a3a3a,stroke:#87ffff,stroke-width:1px,color:#87ffff
    classDef support   fill:#1a3a26,stroke:#87d7af,stroke-width:1px,color:#a7e8c4
    classDef deferred  fill:#1a1a1a,stroke:#666,stroke-width:1px,color:#888
```

### 📋 The full stack inventory

| Layer | Today | Future |
|-------|-------|--------|
| **Authoring** | Markdown · JSON · YAML frontmatter | Same — no build step ever |
| **Distribution** | GitHub public repo · `git clone` under the hood | Optionally tags/releases for pinning |
| **Discovery** | `/plugin marketplace add` | Maybe a Voltmancer landing page (Phase 5) |
| **Runtime** | Claude Code · plugin auto-discovery | Same |
| **State** | `~/.claude/plugins/` cache · per-plugin state dirs | Same |
| **Versioning** | `plugin.json` `version` field · semver | Git tags once stability matters |

> 💡 The stack stays **boring on purpose**. Every interesting decision lives inside individual plugins, not in marketplace plumbing.

---

## 🏢 Org Position

```mermaid
flowchart TD
    H["<b>👤 Itay Turgeman</b><br/>real human"]:::root

    H --> A["<b>💼 Itai Turgeman</b><br/>career identity"]:::secondary
    H --> V["<b>⚡ Voltmancer</b><br/>creative identity"]:::active
    H --> G["<b>🤖 Garage Robotics</b><br/>product brand"]:::secondary

    V --> P["<b>🔌 voltmancer-plugins</b><br/>this repo · public"]:::active

    A -.different brand.-> X["<i>career repos · resume</i>"]:::deferred
    G -.different brand.-> Y["<i>Sentry · Kickstarter</i>"]:::deferred

    Atlas["<b>🌌 Atlas</b><br/>private CEO brain<br/>Linux-only · secret-bearing"]:::data

    H -.runs.-> Atlas
    Atlas -.cannot ship from.-> P

    classDef root      fill:#1a1a2e,stroke:#ff5faf,stroke-width:3px,color:#ff87d7
    classDef active    fill:#ffd75f,stroke:#000,stroke-width:3px,color:#000
    classDef secondary fill:#1a2e44,stroke:#87afff,stroke-width:1px,color:#87d7ff
    classDef data      fill:#2a1a3a,stroke:#af87ff,stroke-width:2px,color:#d7afff
    classDef deferred  fill:#1a1a1a,stroke:#666,stroke-width:1px,color:#888
```

**voltmancer-plugins is intentionally orphan from Atlas.** Atlas is private, Linux-only, and full of personal-context secrets. This repo has to be installable on a work Mac, a borrowed laptop, anywhere. **Hard separation is the feature.**

> 📌 If a plugin idea ever needs Atlas state to function, it doesn't belong here. It belongs in Atlas.

---

## 🤝 Contributing

This is a personal marketplace — the bar to publish is "**Itay needs it on 3+ machines**" — but the install path is public, so the contribution surface is well-defined.

### 🛠️ Adding a new plugin (for future-Itay)

```mermaid
sequenceDiagram
    participant H as 👤 Future Itay
    participant FS as 💾 Repo
    participant MP as 📋 marketplace.json
    participant GH as 🐙 GitHub

    H->>FS: mkdir <plugin-name>/
    H->>FS: write .claude-plugin/plugin.json
    H->>FS: write skills/<name>/SKILL.md
    H->>FS: /plugin marketplace add ~/voltmancer-plugins
    H->>FS: /plugin install <plugin>@voltmancer-plugins
    Note over H,FS: local smoke test passes
    H->>MP: append plugin entry
    H->>GH: git commit + push origin main
    H->>GH: /plugin marketplace update voltmancer-plugins
    Note over H,GH: live on every consumer machine
```

### ✅ Plugin checklist

- [ ] `<plugin>/.claude-plugin/plugin.json` exists with `name`, `description`, `version`, `author`
- [ ] At least one surface populated (`skills/`, `agents/`, `commands/`, `hooks/`, or `mcp/`)
- [ ] Local install works: `/plugin marketplace add ~/voltmancer-plugins` → `/plugin install <name>@voltmancer-plugins`
- [ ] Skill frontmatter `description` triggers correctly (auto-discoverable)
- [ ] No baked-in credentials, IPs, or host-specific paths
- [ ] No dependency on private services Itay runs
- [ ] Plugin entry appended to root `.claude-plugin/marketplace.json`
- [ ] Commit message is atomic and traceable

> 🎯 **The brand bar** — every plugin in this marketplace has to feel like *Voltmancer would actually ship this*. Slop scaffolds get rejected at the local-install gate.

---

## 📖 Glossary

| Term | Meaning |
|------|---------|
| **Voltmancer** | Itay's creative / public identity — the brand behind this repo |
| **Marketplace** | A `marketplace.json` registry pointing to one or more plugins, hosted in a single git repo |
| **Plugin** | Self-contained bundle of Claude Code surfaces (skills/agents/commands/hooks/MCP), versioned via `plugin.json` |
| **Plugin contract** | The Claude Code spec describing the `plugin.json` shape and the surfaces a plugin can declare |
| **Skill** | A markdown file with YAML frontmatter that registers as a slash command and runs as a multi-step workflow |
| **Agent** | A focused subagent (its own context window) for a recurring scoped task |
| **Hook** | An event-driven script bound to a Claude Code lifecycle event (PreToolUse, PostToolUse, Stop, etc.) |
| **MCP server** | A Model Context Protocol server bridging external tools/data into Claude |
| **`/plugin` command** | The Claude Code surface for marketplace + plugin management |
| **Atlas** | Itay's private CEO-level system (Linux-only). **Not** the home for Voltmancer plugins |
| **Garage Robotics** | Itay's hardware product brand. **Not** the home for Voltmancer plugins |
| **scriber** | First Voltmancer plugin · live session → Notion page · v0.1.0 |
| **Lab → Scribe** | Notion page hierarchy scriber writes into |

---

## 🎨 Visual Style

This README follows the [Atlas Diagram Style Guide](https://github.com/itay-turgeman/atlas/blob/main/docs/diagram-style-guide.md) — the canonical visual language for all Itay-org READMEs across `atlas`, `parallax`, `lola`, `sentry`, `reaper`, and (now) `voltmancer-plugins`.

### 📊 Diagram inventory used in this README

| Type | Used for | Count |
|------|----------|-------|
| `flowchart LR` | Roadmap position · install flow · manifest stitching · portability ladder | 4 |
| `flowchart TD` | Brand identity · plugin anatomy · tech stack · org position | 4 |
| `mindmap` | One-picture marketplace overview | 1 |
| `quadrantChart` | Portability vs personal-fit positioning | 1 |
| `pie` | Surface mix · attention budget | 2 |
| `sequenceDiagram` | Plugin install lifecycle · contribution flow | 2 |
| `stateDiagram-v2` | Plugin state machine (candidate → archived) | 1 |
| `gantt` | Roadmap with parallel tracks | 1 |
| `timeline` | Project history (no durations) | 1 |
| `journey` | Fresh-machine setup UX | 1 |

**10 distinct types, 18 Mermaid blocks** — keeps every section visually distinct so the eye doesn't blur.

---

<div align="center">

**🔌 Voltmancer · Plugins**
*Tools that travel with the human.*

`/plugin marketplace add github:itay-turgeman/voltmancer-plugins`

</div>
