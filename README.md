# voltmancer-plugins

Itay's personal Claude Code plugin marketplace — cross-machine tools that travel with him.

## Plugins

| Plugin | What it does |
|--------|--------------|
| **scriber** | Live session scribe into Notion. Builds a running page under `Lab → Scribe` with a `Now` block + adaptive sections as you work. Hybrid manual/auto. Promotes to the Lab Pipeline as a Draft when polished. |

## Install on a fresh machine

```bash
# Inside Claude Code:
/plugin marketplace add github:itay-turgeman/voltmancer-plugins
/plugin install scriber@voltmancer-plugins
```

That's it. The skill registers as `/scriber` and is available in every session.

## Local install (this repo, before pushing to GitHub)

For testing or running off a local clone:

```bash
/plugin marketplace add ~/voltmancer-plugins
/plugin install scriber@voltmancer-plugins
```

## Updating

```bash
/plugin marketplace update voltmancer-plugins
/plugin update scriber
```

## Adding a new plugin

1. Create `<plugin-name>/.claude-plugin/plugin.json` with `name`, `description`, `version`
2. Add skills/agents/commands/hooks under `<plugin-name>/skills/<name>/SKILL.md` etc.
3. Add the plugin entry to `.claude-plugin/marketplace.json`
4. Commit + push
5. Run `/plugin marketplace update voltmancer-plugins` on consumer machines

## Why a separate repo from atlas?

Atlas is the ops brain — Linux-only, full of secrets and host-specific config. This repo is just personal tooling that wants to live on every machine I run Claude Code on, including work environments where Atlas doesn't belong.
