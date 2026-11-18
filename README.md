# Lovitations plugins

This repository publishes the [Lovitations plugin](plugins/lovitations/README.md):
wedding planning skills for Claude (the Claude app and Claude Code), ChatGPT
and Codex, Gemini CLI and Grok Build.

## Install

| Where | How |
|---|---|
| Claude (app) | Download `lovitations-<version>.zip` from the [latest release](https://github.com/lovitations/public/releases/latest) and upload it under Customize → Plugins. |
| Claude Code | `/plugin marketplace add lovitations/public`, then `/plugin install lovitations@lovitations` |
| Codex | `codex plugin marketplace add lovitations/public`, then `codex plugin add lovitations@lovitations` |
| Gemini CLI | `gemini extensions install https://github.com/lovitations/public` |
| Grok Build | Grok Build reads Claude Code marketplaces: add this repository as a marketplace source, then install `lovitations` from the Marketplace tab. |

## Layout

- `plugins/lovitations/`: the plugin, exactly as it ships (manifests for
  Claude, Codex and Gemini, skills, images, docs). No code.
- `.claude-plugin/marketplace.json`, `.agents/plugins/marketplace.json`: the
  Claude and Codex marketplaces, pointing at the plugin folder.
- `scripts/`, `.github/`: checks, version bump, ZIP build and release. See
  [RELEASING.md](RELEASING.md).

## Languages

One plugin serves every language. The skills answer in the language the user
writes in and follow the customs of the country the wedding is in; their
descriptions carry trigger phrases in Dutch, English, Spanish and German. The
manifests and directory listings are English, because plugin manifests have no
per-language fields.

## License

MIT. See `LICENSE`.
