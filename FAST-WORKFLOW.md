# Fast Workflow

## Plan and Parallel Execution

Interactively plan out code migrations, then execute in parallel using dozens of agents.
Each agent runs with full isolation using git worktrees, testing its work before putting up a PR.

```sh
/batch migrate src/ from Solid to React
```

- https://x.com/bcherny/status/2027534984534544489

## Simplify

```sh
/simplify
```

Alternative usage: `make this code change then run /simplify`

- https://x.com/bcherny/status/2027534984534544489

## Claude Code Insights

The /insights command in Claude Code generates a comprehensive HTML report analyzing your usage patterns across all your Claude Code sessions.
It’s designed to help you understand how you interact with Claude, what’s working well, where friction occurs, and how to improve your workflows.

- https://www.zolkos.com/2026/02/04/deep-dive-how-claude-codes-insights-command-works.html

```sh
/insights
```
