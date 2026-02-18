# Model Context Protocol (MCP)

## Claude Code

`~/.claude.json`

## Installation

### Context7

- https://github.com/upstash/context7

```sh
claude mcp add --scope user context7 -- npx -y @upstash/context7-mcp --api-key YOUR_API_KEY
# or with bunx
claude mcp add --scope user context7 -- bunx -y --bun @upstash/context7-mcp --api-key YOUR_API_KEY
```

### LEANN

Small RAG Vector DB.

- https://github.com/yichuan-w/LEANN/blob/main/packages/leann-mcp/README.md
- https://medium.com/data-science-in-your-pocket/leann-smallest-rag-vector-db-25d98e977ec6

```sh
uv tool install leann-core --with leann --python 3.13
claude mcp add --scope user leann-server -- leann_mcp

# Build an index for your project
# Set the index name (replace 'my-project' with your own)
leann build my-project --docs $(git ls-files)
```

Prompt: Help me understand this codebase. List available indexes and search for authentication patterns.
