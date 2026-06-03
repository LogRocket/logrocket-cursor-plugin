# LogRocket Plugin for Cursor

Connect Cursor to [LogRocket](https://logrocket.com) to query session replays, metrics, issues, and user behavior using natural language — powered by the [LogRocket MCP Server](https://docs.logrocket.com/docs/mcp) and [Ask Galileo](https://docs.logrocket.com/docs/ask-galileo).

## What's Included

| Component | Description |
|-----------|-------------|
| **MCP Server** | Connects Cursor to the LogRocket API via the `use_logrocket` tool |
| **Use LogRocket Skill** | Teaches your AI agent how to query LogRocket on your behalf |

## Setup

1. Install the plugin from the Cursor Marketplace.
2. Connect to the LogRocket MCP server when prompted by Cursor, and authenticate via OAuth.

That's it — the MCP server connects to the root `https://mcp.logrocket.com/mcp` endpoint and gives the agent access to the same LogRocket organizations and projects you can access in your browser. No environment variables required.

## Example Prompts

- "User X reported a problem with checkout. Can you use LogRocket to watch their sessions and figure out the root cause?"
- "I'm about to work on the search feature — can you use LogRocket to help me understand how it's currently being used?"
- "Can you look at LogRocket for new issues from the past week, try to figure out their root causes, and then suggest which ones I can fix?"
- "Look at all commits from last week, and check LogRocket data to ensure they didn't introduce any regressions."
- "Use LogRocket to watch sessions and look at issues to figure out what is highest priority that I work on next."

## Learn More

- [LogRocket MCP Server Docs](https://docs.logrocket.com/docs/mcp)
- [Ask Galileo Docs](https://docs.logrocket.com/docs/ask-galileo)

## Repository structure

This is a multi-plugin marketplace repository, mirroring the layout of the official [cursor/plugins](https://github.com/cursor/plugins) repo. The root `.cursor-plugin/marketplace.json` lists all plugins, and each plugin lives in its own top-level directory:

```
.cursor-plugin/
└── marketplace.json       # Marketplace manifest (lists all plugins)
logrocket/
├── .cursor-plugin/
│   └── plugin.json        # Per-plugin manifest
├── skills/                # Agent skills (SKILL.md with frontmatter)
├── mcp.json               # MCP server definition
├── README.md
├── CHANGELOG.md
└── LICENSE
schemas/                   # JSON schemas for validation
scripts/validate-plugins.mjs
```

## Validation

Validate the plugin structure against the Cursor plugin schemas:

```sh
npm install --no-save ajv ajv-formats
node scripts/validate-plugins.mjs
```
