# Fast Workflow

## Brainstorming

```sh
/simple-brainstorm add table component for admin dashboard
```

- https://github.com/roin-orca/skills
- https://github.com/obra/superpowers

## Plan Only

```sh
/plan
```

- https://code.claude.com/docs/en/common-workflows#use-plan-mode-for-safe-code-analysis

## Refactor Code

```sh
/refactor
```

- https://github.com/github/awesome-copilot/blob/main/skills/refactor/SKILL.md
- https://code.claude.com/docs/en/common-workflows#refactor-code

### Repomix

```
This file contains all the files in the repository combined into one.
I want to refactor the code, so please review it first.
#file:repomix-output.xml
```

#### Refactoring Assistance

Get refactoring suggestions that maintain consistency across your entire codebase.

```
This codebase needs refactoring to improve maintainability.
Please suggest improvements while keeping the existing functionality intact.
```

- https://repomix.com/guide/use-cases#refactoring-assistance

## Review Plan

```sh
/plan-exit-review
```

- https://gist.github.com/garrytan/001f9074cab1a8f545ebecbc73a813df
- https://x.com/garrytan/status/2026778016463138882

## Plan and Parallel Execution

Research and interactively plan a `large-scale change`, then execute it in parallel using dozens of agents.
Each agent runs with full isolation using git worktrees, testing its work before putting up a PR.

```sh
/batch migrate src/ from Solid to React, use red/green TDD
```

- https://x.com/bcherny/status/2027534984534544489

## Simplify

```sh
/simplify
```

Alternative usage: `make this code change then run /simplify`

- https://x.com/bcherny/status/2027534984534544489
- https://www.youtube.com/watch?v=0_-Ld5vtw8M

## Insights

The /insights command in Claude Code generates a comprehensive HTML report analyzing your usage patterns across all your Claude Code sessions.
It’s designed to help you understand how you interact with Claude, what’s working well, where friction occurs, and how to improve your workflows.

- https://www.zolkos.com/2026/02/04/deep-dive-how-claude-codes-insights-command-works.html

```sh
/insights
```

## Memory

- https://github.com/blader/theorist
- https://github.com/blader/napkin

### Auto-Memory

Claude remembers what it learns across sessions — your project context, debugging patterns, preferred approaches — and recalls it later without you having to write anything down.

- https://code.claude.com/docs/en/memory#auto-memory
- https://x.com/trq212/status/2027109375765356723

### Memory Optimizer

```sh
/memory-optimize
```

- https://github.com/kochetkov-ma/claude-brewcode/tree/main/skills/memory-optimize
