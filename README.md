# Infordisa Claude Code plugins

Internal [Claude Code](https://docs.claude.com/en/docs/claude-code) plugins for the Infordisa team, distributed as a plugin marketplace.

## Plugins

### `handoff` — `/handoff`

Wind down the current session and export it so a fresh agent can continue cold — for when the context window gets bloated. The agent captures whatever context matters (inline in the continuation chip, or in project docs / memory / a note as it sees fit) and creates a chip to resume the work in a new session.

> The continuation chip is produced by the `spawn_task` tool, which ships with the Claude Code app (desktop/IDE). In a plain terminal CLI the command still writes/points to the context and tells you where to pick up.

## Install (manual)

```text
/plugin marketplace add Infordisa/claude-plugins
/plugin install handoff@infordisa-tools
```

Then run `/handoff` in any session.

## Install for the whole org (managed settings)

On Team/Enterprise, an admin can force-enable this for everyone via server-managed settings, so no one has to install it by hand. Add to the org's `managed-settings.json` (Claude.ai Admin Console, or the on-disk managed-settings file):

```json
{
  "extraKnownMarketplaces": {
    "infordisa-tools": {
      "source": { "source": "github", "repo": "Infordisa/claude-plugins" }
    }
  },
  "enabledPlugins": {
    "handoff@infordisa-tools": true
  }
}
```

Teammates pick it up automatically on their next launch.
