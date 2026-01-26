# 💬 Claude Code

[Claude Code](https://github.com/anthropics/claude-code#readme) is a CLI tool to interact with Claude models from the terminal.

- 📖 [Best Practices for Claude Code](https://code.claude.com/docs/en/best-practices)
- 💡 [Prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-4-best-practices)
- ✍️ [Skill authoring best practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices)
- 📚 [Claude Cookbooks](https://github.com/anthropics/claude-cookbooks#readme)
- 🔧 [Use Claude Code in VS Code](https://code.claude.com/docs/en/vs-code)
- 💭 [Boris Cherny Tips](https://x.com/bcherny/status/2007179832300581177)
- 🎯 [Claude Code Tips](https://github.com/ykdojo/claude-code-tips)

## 🛠️ Tools

- 📊 [Claude Code Usage Analyzer](https://github.com/ryoppippi/ccusage#readme)
- [Claude Task Viewer](https://github.com/L1AD/claude-task-viewer#readme)
- [claude-tasks-viewer](https://github.com/burke/claude-tasks-viewer#readme)

## Tasks

`CLAUDE_CODE_TASK_LIST_ID=test claude`

- [Tasks are a new primitive that help Claude Code track projects](https://x.com/bcherny/status/2014485078815211652)

## 📟 Status line

```sh
/statusline set the status line to include: 
1. current git repository
2. current branch
3. model used
4. progress bar of 10 U+2588 or U+2591 showing context usage
5. total cost in USD.
Example: my-project: add-auth | Opus | Context: {{ progress bar }} 30% (60k / 200k) | $2.17
```

[source](https://x.com/claudeai/status/1999209597035331739)

## 🔌 Plugins

- 🎨 [Official Claude Code plugins](https://github.com/anthropics/claude-code/tree/main/plugins)

```sh
# List available plugins in JSON format.
claude plugin list --available --json > cc-plugins.json
```

### Installation

```sh
# Claude-Mem
# Seamlessly preserves context across sessions.
# https://github.com/thedotmack/claude-mem
claude plugin marketplace add thedotmack/claude-mem
claude plugin install claude-mem

### Oficial Claude Code Plugins ###

# Claude Code Setup
# Analyze codebases and recommend tailored Claude Code automations such as hooks, skills, MCP servers, and subagents.
claude plugin install claude-code-setup

# CLAUDE.md Management
# Tools to maintain and improve CLAUDE.md files - audit quality, capture session learnings, and keep project memory current.
claude plugin install claude-md-management

# Code Review
# Automated code review for pull requests using multiple specialized agents with confidence-based scoring to filter false positives.
# https://github.com/anthropics/claude-code/blob/main/plugins/code-review/README.md
claude plugin install code-review

# Code Simplifier
# Agent that simplifies and refines code for clarity, consistency, and maintainability while preserving functionality. Focuses on recently modified code.
claude plugin install code-simplifier

# Commit Commands
# Commands for git commit workflows including commit, push, and PR creation.
# https://github.com/anthropics/claude-code/blob/main/plugins/commit-commands/README.md
claude plugin install commit-commands

# Feature Dev
# Comprehensive feature development workflow with specialized agents for codebase exploration, architecture design, and quality review.
# https://github.com/anthropics/claude-code/blob/main/plugins/feature-dev/README.md
claude plugin install feature-dev

# Go LSP
# Go language server for code intelligence and refactoring.
claude plugin install gopls-lsp

# Plugin Development Toolkit
# Comprehensive toolkit for developing Claude Code plugins. Includes 7 expert skills covering hooks, MCP integration, commands, agents, and best practices. AI-assisted plugin creation and validation.
# https://github.com/anthropics/claude-code/blob/main/plugins/plugin-dev/README.md
claude plugin install plugin-dev

# PR Review Toolkit
# Comprehensive PR review agents specializing in comments, tests, error handling, type design, code quality, and code simplification.
# https://github.com/anthropics/claude-code/blob/main/plugins/pr-review-toolkit/README.md
claude plugin install pr-review-toolkit

# Pyright LSP
# Python language server (Pyright) for type checking and code intelligence.
claude plugin install pyright-lsp

# Rust Analyzer LSP
# Rust language server for code intelligence and analysis.
claude plugin install rust-analyzer-lsp

# Security Guidance
# Security reminder hook that warns about potential security issues when editing files, including command injection, XSS, and unsafe code patterns.
claude plugin install security-guidance

# TypeScript LSP
# TypeScript/JavaScript language server for enhanced code intelligence.
claude plugin install typescript-lsp
```
