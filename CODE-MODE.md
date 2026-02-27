# Code Mode Pattern

> Transform your AI agents from clunky tool callers into efficient code executors — in just 3 lines.

## Why This Changes Everything

LLMs excel at writing code but struggle with tool calls. Instead of exposing hundreds of tools directly, give them ONE tool that executes TypeScript code with access to your entire toolkit.

[Apple](https://machinelearning.apple.com/research/codeact), [Cloudflare](https://blog.cloudflare.com/code-mode/), and [Anthropic](https://www.anthropic.com/engineering/code-execution-with-mcp) say that Code-Mode is a more efficient way to approach tool calling compared to the traditional dump function information and then extract a JSON for function calling.

## Benchmarks

Independent [Python benchmark study](https://github.com/imran31415/codemode_python_benchmark) validates the performance claims with **$9,536/year cost savings** at 1,000 scenarios/day:

| Scenario Complexity    | Traditional   | Code Mode   | **Improvement** |
| ---------------------- | ------------- | ----------- | --------------- |
| **Simple (2-3 tools)** | 3 iterations  | 1 execution | **67% faster**  |
| **Medium (4-7 tools)** | 8 iterations  | 1 execution | **75% faster**  |
| **Complex (8+ tools)** | 16 iterations | 1 execution | **88% faster**  |

### **Why Code Mode Dominates:**

**Batching Advantage** - Single code block replaces multiple API calls  
**Cognitive Efficiency** - LLMs excel at code generation vs. tool orchestration  
**Computational Efficiency** - No context re-processing between operations

## Tools

- https://github.com/universal-tool-calling-protocol/code-mode/tree/main/code-mode-mcp
- https://github.com/dmmulroy/opensrc-mcp

## Resources

- https://blog.cloudflare.com/code-mode/
- https://blog.cloudflare.com/code-mode-mcp/
