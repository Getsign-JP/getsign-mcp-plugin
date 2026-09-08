# Changelog

## 1.1.1

- Points every install instruction and manifest link at `Getsign-JP/getsign-mcp-plugin`, the public home of this plugin.

## 1.1.0

- Installs in Cursor: the same directory now ships Agent Plugins 1.0 (`plugin.json` + `mcp.json`) and Cursor (`.cursor-plugin/`) manifests alongside the Claude Code pair.
- Skill frontmatter carries only the six Agent Skills fields — `when_to_use` is folded into `description`, which every client reads.
- Ships a square logo at `assets/logo.svg`, so the Cursor listing renders a tile rather than a blank square.

## 1.0.0

- First public release: `install-getsign-on-new-account`, `send-new-document`, `board-pending-signatures`, `create-or-update-workflow`, `sign-from-file-column`, `save-signed-document-to-file-column`.
- Bundles the hosted GetSign MCP server at `https://mcp.getsign.io/mcp`.
