# GetSign MCP Plugin

Plugin distribution repo for [GetSign](https://getsign.io) — e-signatures on monday.com boards, driven from chat. One tree, four clients: **Claude Code**, **Cursor**, **Codex**, and any other [Agent Plugins](https://agent-plugins.org) 1.0 host.

> [!IMPORTANT]
> **Everything under `plugins/getsign/`, `.claude-plugin/`, `.cursor-plugin/` and `.agents/` is generated** from the flow registry in the private [`getsign-mcp-server`](https://github.com/Jetpack-Work-Labs/getsign-mcp-server) repo and republished here by a one-way sync script. Only this file, `LICENSE` and `.github/workflows/validate.yml` are hand-written.
>
> **File issues on this repo — pull requests here will be silently overwritten by the next publish.** Fixes belong in `getsign-mcp-server` and flow back here through the normal generate → review → publish loop.

## Install

### Claude Code

```
/plugin marketplace add Getsign-JP/getsign-mcp-plugin
/plugin install getsign@getsign
```

### Codex

```
codex plugin marketplace add Getsign-JP/getsign-mcp-plugin
codex plugin add getsign@getsign
```

Or `/plugins` inside a session: pick the **GetSign** marketplace tab, open GetSign, install, and press Space to enable it.

### Cursor

**Settings → Plugins → Add Plugin Repo**, then install GetSign from **Customize → Plugins**.

---

See [`plugins/getsign/README.md`](plugins/getsign/README.md) for authentication, the skills this plugin ships, and what to do if you're already connected to the GetSign MCP server directly.

## What's in this repo

The plugin lives at `plugins/getsign/`. Every client discovers its skills at `skills/<name>/SKILL.md`; they disagree only on which manifest file to read, so the tree carries all of them and each client ignores the others'.

| Path | Read by |
| --- | --- |
| `.claude-plugin/marketplace.json` | Claude Code — `/plugin marketplace add` |
| `.cursor-plugin/marketplace.json` | Cursor's marketplace parser |
| `.agents/plugins/marketplace.json` | Codex — `codex plugin marketplace add` |
| `plugins/getsign/.claude-plugin/plugin.json` + `.mcp.json` | Claude Code |
| `plugins/getsign/plugin.json` + `mcp.json` | Agent Plugins 1.0 (Cursor and others) |
| `plugins/getsign/.cursor-plugin/plugin.json` | Cursor's native manifest |
| `plugins/getsign/.codex-plugin/plugin.json` | Codex's native manifest |
| `plugins/getsign/skills/` | all four |

All generated; see the note above.

## License

MIT — see [`LICENSE`](LICENSE).
