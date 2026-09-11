# Changelog

## 1.2.0

- First-class in Codex: ships OpenAI's `.codex-plugin/plugin.json` and a root `.agents/plugins/marketplace.json`, so `codex plugin marketplace add Getsign-JP/getsign-mcp-plugin` resolves GetSign's own listing — display name, category, and composer prompts — instead of falling back to the Claude-format index.
- Two steps added to the document flows, so the skills no longer stop short of a document that carries merge tags: `getsign_validate_document_placeholders` checks a DOCX's `{{Column Title}}` tokens once the template is on the workflow, and `getsign_map_board_fields` fills `{{Column Title}}` / `{columnId}` tags in a PDF from the item's Monday columns.

## 1.1.2

- Publishes under the GetSign name: the marketplace owner and the author block in all three manifests now read `GetSign` rather than the operating company.
- Restores `appsupport@jetpackwork.com` as the contact address in all three plugin manifests, where a merge had reverted it to an address that does not receive mail. The marketplace files were unaffected, which is why the listing looked right while every plugin manifest under it did not.

## 1.1.1

- Points every install instruction and manifest link at `Getsign-JP/getsign-mcp-plugin`, the public home of this plugin.

## 1.1.0

- Installs in Cursor: the same directory now ships Agent Plugins 1.0 (`plugin.json` + `mcp.json`) and Cursor (`.cursor-plugin/`) manifests alongside the Claude Code pair.
- Skill frontmatter carries only the six Agent Skills fields — `when_to_use` is folded into `description`, which every client reads.
- Ships a square logo at `assets/logo.svg`, so the Cursor listing renders a tile rather than a blank square.

## 1.0.0

- First public release: `install-getsign-on-new-account`, `send-new-document`, `board-pending-signatures`, `create-or-update-workflow`, `sign-from-file-column`, `save-signed-document-to-file-column`.
- Bundles the hosted GetSign MCP server at `https://mcp.getsign.io/mcp`.
