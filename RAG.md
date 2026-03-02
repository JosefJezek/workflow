# RAG (Retrieval-Augmented Generation)

RAG (Retrieval-Augmented Generation) is a technique that combines retrieval-based methods with generative models to enhance the performance of language models. It allows the model to access external knowledge sources, such as databases or documents, to generate more accurate and contextually relevant responses.

## LEANN

LEANN is a small RAG Vector DB that can be integrated with Claude Code using the Model Context Protocol (MCP). It allows you to build an index for your project and search for relevant information to assist in code generation and understanding.

- https://github.com/yichuan-w/LEANN
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
