# Of Record

Run an executive search from a conversation with your AI assistant: Claude, ChatGPT, Codex, Cursor, or any assistant that supports remote MCP connectors. Describe the role you need to fill. Of Record writes a research plan for you to approve, researches real people with a public professional presence against your brief, and returns a ranked shortlist in which every stated fact links to its source. The full report also arrives by email as a print-ready PDF.

## What is in this plugin

| Part | What it does |
|---|---|
| `skills/executive-search` | Tells the assistant how to take a brief, relay the research plan for your approval, and present the shortlist without adding anything |
| `.mcp.json`, `mcp.codex.json`, `mcp.cursor.json` | Connect the assistant to the Of Record service at `https://ofrecord-service.vercel.app/mcp` |
| `.claude-plugin/`, `.codex-plugin/`, `.cursor-plugin/` | The same plugin, described for Claude Code, Codex and Cursor |

The plugin contains no research code and runs nothing on your computer. The research engine runs on the Of Record service. The connector's tools carry the same instructions as the skill, so an assistant without the skill still follows the same steps.

## Getting started

Add the connector, sign in, then describe the role.

- **Claude (web, desktop, mobile):** Settings → Connectors → Add custom connector, with the URL above.
- **Claude Code:** `/plugin marketplace add Tarn-Labs-VStudio/ofrecord-plugins`, then `/plugin install ofrecord@ofrecord`.
- **ChatGPT:** with developer mode on, create a connector with the URL above and OAuth sign-in. Starting a search is a write action, so it needs a ChatGPT plan with full MCP support.
- **Codex:** `codex mcp add ofrecord --url https://ofrecord-service.vercel.app/mcp`, then `codex mcp login ofrecord`. Or install the plugin: `codex plugin marketplace add https://github.com/Tarn-Labs-VStudio/ofrecord-plugins`, then `codex plugin add ofrecord@ofrecord`.
- **Any other MCP client:** add the URL as a remote (streamable HTTP) server with OAuth.

Signing in: enter your work email on the Of Record page that opens, then type the code we email you. No password.

Then describe the role, for example: "Find a Chief Financial Officer for a utility in Abu Dhabi: listed companies and state-owned utilities, CFO or one rung below, ten years minimum, IPO experience."

## What is sent, and where

- **To Of Record:** your email address (to sign in and to send reports), and the brief you confirm in the conversation. Nothing else from your conversation is sent.
- **Of Record sends you:** sign-in codes, the research plan, and the finished report, by email from Of Record.
- **Of Record fetches:** public web pages about professionals (regulator listings, company biographies, government profiles, conference programmes) to research your brief. It does not collect private contact details.
- **Your assistant receives:** the research plan, search status, and the shortlist with sources, through the connector.

## Cost

Searches are quoted per search. Nothing runs, and nothing is charged, until you approve the research plan. A search that fails Of Record's quality check is held for review and is not charged.

## Privacy and support

Privacy policy and terms: to be published before public release. Support: vstudio@tarn-labs.com.
