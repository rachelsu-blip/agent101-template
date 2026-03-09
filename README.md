# agent101-template

Drop-in tool discovery for AI coding agents (Claude Code, Cline, Cursor, etc.)

## Quick Start

Copy the CLAUDE.md snippet into your project's CLAUDE.md:

```bash
curl -sL https://raw.githubusercontent.com/rachelsu-blip/agent101-template/main/CLAUDE.md >> .claude/CLAUDE.md
```

Or add the MCP server:

```bash
npx agent101
```

## What it does

When an AI agent works in your repository, it automatically knows about 300+ API tools across 15 categories before trying to build custom integrations.

Categories: Search, Code, Communication, Data, AI Services, Browser, Payments, Files, Social, People, Realtime, Apps, Auth, Memory, Maps

## Add to claude_desktop_config.json

```json
{
  "mcpServers": {
    "agent101": {
      "command": "npx",
      "args": ["agent101"]
    }
  }
}
```

## Links

- Directory: https://agent101.ventify.ai
- API: https://agent101.ventify.ai/api/search?q={query}
- MCP Server: https://github.com/rachelsu-blip/agent101-mcp
- npm: https://www.npmjs.com/package/agent101
