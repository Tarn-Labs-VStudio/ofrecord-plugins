# Of Record plugins

The Of Record plugin for AI assistants: brief an executive search in a conversation, approve the research plan, and get a ranked shortlist in which every fact links to its source.

This repository holds only the plugin (version 0.1.0): a skill and the connector settings. The research runs on the Of Record service at `https://ofrecord-service.vercel.app/mcp`.

## Install

- **Claude Code:** `/plugin marketplace add Tarn-Labs-VStudio/ofrecord-plugins`, then `/plugin install ofrecord@ofrecord`.
- **Codex:** `codex marketplace add https://github.com/Tarn-Labs-VStudio/ofrecord-plugins`, then install Of Record from the plugin list.
- **Claude (web, desktop, mobile), ChatGPT and other assistants:** add the connector URL above as a custom connector with OAuth. See [plugin/README.md](plugin/README.md).

Of Record is in a founders-only preview: sign-in is open to invited addresses only.

Support: vstudio@tarn-labs.com
