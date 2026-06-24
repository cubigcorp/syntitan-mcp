# Installing the Syntitan MCP Server (guide for AI agents)

Syntitan is a **remote** MCP server hosted by CUBIG. There is **no package to
install** and **no API key to configure** — connect to the hosted endpoint and
the user signs in through OAuth on first use.

## Configuration

Add Syntitan as a **remote** MCP server using the `streamable-http` transport:

- **URL:** `https://mcp.syntitan.ai/mcp`
- **Transport:** `streamable-http`
- **Authentication:** OAuth 2.0 (browser-based sign-in; nothing to paste)

Representative MCP settings entry:

```json
{
  "mcpServers": {
    "syntitan": {
      "url": "https://mcp.syntitan.ai/mcp",
      "type": "streamable-http"
    }
  }
}
```

Do **not** add a `command`, package name, environment variables, or API keys —
this is a hosted remote server, not a local (stdio) one.

## First connection

On first connection the user's browser opens the Syntitan sign-in page. After
the user logs in and authorizes access, the client connects automatically.

## What it does

Once connected, Syntitan exposes tools to diagnose dataset AI-readiness,
inspect schemas and columns, and run data quality refinement — all through
natural language. See `README.md` for the full tool list.
