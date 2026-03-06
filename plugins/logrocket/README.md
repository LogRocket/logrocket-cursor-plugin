# LogRocket Plugin for Cursor

Connect Cursor to [LogRocket](https://logrocket.com) to query session replays, metrics, issues, and user behavior using natural language.

Powered by the [LogRocket MCP Server](https://docs.logrocket.com/docs/mcp) and [Ask Galileo](https://docs.logrocket.com/docs/ask-galileo).

## What's Included

- **MCP Server** — Connects Cursor to the LogRocket API so your AI agent can query sessions, metrics, issues, and more.
- **Use LogRocket Skill** — A skill that teaches your agent how to invoke LogRocket queries on your behalf.

## Setup

1. Find your **App ID** under **Settings > Project Settings** in the LogRocket dashboard, or in the URL: `https://app.logrocket.com/<org_id>/<project_id>`.
2. Set the environment variables `LOGROCKET_ORG_ID` and `LOGROCKET_PROJECT_ID`, or replace them directly in `mcp.json`.
3. Connect to the MCP server when prompted by Cursor to authenticate.

## Learn More

- [LogRocket MCP Server Docs](https://docs.logrocket.com/docs/mcp)
- [Ask Galileo Docs](https://docs.logrocket.com/docs/ask-galileo)
