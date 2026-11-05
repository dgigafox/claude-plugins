# dgigafox — Claude Code plugin marketplace

A catalog of Claude Code plugins. Add it once, then install any plugin listed here.

```
/plugin marketplace add dgigafox/claude-plugins
```

## Plugins

| Plugin | Install | What it does |
|--------|---------|--------------|
| **lucid** | `/plugin install lucid@dgigafox` | Manual, git-versioned curation of Claude Code's native per-project memory stores — dedup + reconcile safe hygiene in place, queue value-contradictions for your review. Source: [`dgigafox/lucid`](https://github.com/dgigafox/lucid). |
| **devteam** | `/plugin install devteam@dgigafox` | Takes one task — a ticket, a Story's Sub-tasks, or plain instructions — to a reviewed PR with area-owned agents, approving the plan, each phase, the commits and the push. Run `/devteam:setup` once per repo, then `/devteam:implement`. Source: [`dgigafox/devteam`](https://github.com/dgigafox/devteam). |

## Updating

```
/plugin marketplace update dgigafox
```
This refreshes the catalog; installed plugins update to the versions their repos now declare.

## Adding a new plugin

Append an entry to `.claude-plugin/marketplace.json` → `plugins[]` pointing at the plugin's repo:

```json
{
  "name": "my-plugin",
  "source": { "source": "github", "repo": "dgigafox/my-plugin" },
  "description": "..."
}
```
Users who already added this marketplace get it on their next `/plugin marketplace update dgigafox`
— no second `marketplace add` needed.
