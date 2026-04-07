# Model Context Protocol (MCP)

## Claude Code

`~/.claude.json`

## Installation

- https://github.com/paoloricciuti/mcp-add

### Context7

- https://github.com/upstash/context7

```sh
claude mcp add --scope user context7 -- npx -y @upstash/context7-mcp --api-key YOUR_API_KEY
# or with bunx
claude mcp add --scope user context7 -- bunx -y --bun @upstash/context7-mcp --api-key YOUR_API_KEY
```

### Vercel Grep

- https://vercel.com/blog/grep-a-million-github-repositories-via-mcp

```sh
claude mcp add --scope user --transport http grep https://mcp.grep.app
```
