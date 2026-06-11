# ik — interview kit plugin

Claude Code plugin for AI-assisted coding interviews. Installs phase slash
commands and injects behavioral ground rules at session start.

## Install (inside Claude Code)

```
/plugin marketplace add tractatus7/ik-plugin
/plugin install ik@ik-plugin
```

## What you get

- **Ground rules** injected into context at session start (`context.md` via a
  SessionStart hook): human makes decisions, AI implements; run after every
  change; no test-weakening shortcuts; terse output; `tc N` / `??` time codes.
- **Commands**: `/ik:requirements`, `/ik:options`, `/ik:edges`, `/ik:verify`,
  `/ik:checkpoint`, `/ik:wrap` — one per interview phase.

## Not included (plugin limitations)

Permission allowlist and DECISIONS.md scaffolding can't ship in a plugin.
For the full kit, use the script install instead:

```
curl -sL github.com/tractatus7/ik/raw/main/setup.sh | bash
```

This plugin is the fallback channel; `setup.sh` in
[tractatus7/ik](https://github.com/tractatus7/ik) is the source of truth —
`commands/` and `context.md` here are generated from it.
