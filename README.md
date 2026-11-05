<p align="center"><img src="assets/logo.png" alt="Destava" width="96"></p>

# Destava job search for AI agents

Search current job postings from companies' own career sites, from Claude, ChatGPT, Cursor, Gemini, Grok or any MCP
client. Free, and no account is needed to search.

| | |
|---|---|
| MCP server | `https://destava.com/mcp` (streamable HTTP, no authentication) |
| Docs | https://destava.com/mcp/docs |
| Official MCP Registry | `com.destava/jobs` |

## Tools

All three are read-only.

- **`search_jobs`**: current postings for a role, skills and a place, up to 20 a call. Each carries the company's own
  link to apply, the day it was first seen, how often it was reposted, and level and pay where the company states them.
- **`get_job`**: one posting by its link or ID. Open or closed (within the last 30 days), its age, reposts, the places
  it names and a short excerpt.
- **`watch_search`**: a link that sets up the same search every morning on your own Destava account. Nothing is set up
  until you open it, sign in with Google and approve it.

## Add it

| Client | How |
|---|---|
| Claude (claude.ai, Desktop) | Settings → Connectors → Add custom connector → `https://destava.com/mcp` |
| Claude Code | `claude mcp add --transport http destava https://destava.com/mcp` |
| ChatGPT | Plugins → Add → Add custom MCP server → `https://destava.com/mcp`, No authentication |
| Cursor | [`mcp.json`](mcp.json) in your project's `.cursor/` folder, or Settings → MCP → Add |
| VS Code | "MCP: Add Server" → HTTP → `https://destava.com/mcp` |
| Gemini CLI | `gemini extensions install https://github.com/askdestava/destava-mcp` |
| Grok | grok.com/connectors → New Connector → Custom → `https://destava.com/mcp` |

Then ask, for example: "Find AI engineer jobs in San Francisco posted this week."

## Privacy

Destava records the query and your client's name, not who asked; our host's request logs keep network addresses for up
to 7 days. [Privacy Policy](https://destava.com/privacy) (section 8 covers searches and AI agents) ·
[Terms](https://destava.com/terms).

## About this repository

It holds connection files only. The server is run by Destava (Xprtis LLC) at `destava.com` and is not open source; the
files here are MIT licensed. Questions: ask@destava.com.
