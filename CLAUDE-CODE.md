# 💬 Claude Code

[Claude Code](https://github.com/anthropics/claude-code#readme) is a CLI tool to interact with Claude models from the terminal.

> I use Claude Code tool, because it provides powerful interface to leverage Claude models effectively for AI-assisted development.

## Settings

- Edit settings file `~/.claude/settings.json` to configure default model, plugins, and other preferences.

### Environment Variables

- https://code.claude.com/docs/en/settings#environment-variables

```yaml
"env": {
    # Disable bug command to prevent accidental triggering and improve privacy. Use with caution as it may impact performance optimizations and support.
    "DISABLE_BUG_COMMAND": "1",

    # Disable error reporting to prevent data collection and improve privacy. Use with caution as it may impact performance optimizations and support.
    "DISABLE_ERROR_REPORTING": "1",

    # Disable telemetry to prevent data collection and improve privacy. Use with caution as it may impact performance optimizations and support.
    "DISABLE_TELEMETRY": "1",

    # Enable LSP tools for better code intelligence and refactoring capabilities.
    "ENABLE_LSP_TOOLS": "1",

    # Maintain project working directory across commands to allow for better context and state management.
    "CLAUDE_BASH_MAINTAIN_PROJECT_WORKING_DIR": "1",

    # Set maximum output tokens for MCP responses to 50,000 to allow for more detailed and comprehensive responses from MCP servers.
    # https://code.claude.com/docs/en/mcp#mcp-output-limits-and-warnings
    "MAX_MCP_OUTPUT_TOKENS": "50000",

    # Set default models for different agent types to the 1M context versions for better performance on larger codebases.
    # Requires enabling extra usage on your subscription plan.
    # The 1M context only increases in price went context goes past 200K but the model performs better knowing the headroom it has.
    # https://code.claude.com/docs/en/model-config#environment-variables
    # https://code.claude.com/docs/en/model-config#extended-context-with-1m
    # https://x.com/nummanali/status/2023828631793909855
    # https://x.com/nummanali/status/2023917312793854336
    "ANTHROPIC_DEFAULT_OPUS_MODEL": "claude-opus-4-6[1m]",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "claude-sonnet-4-6[1m]",
    "ANTHROPIC_DEFAULT_HAIKU_MODEL": "claude-sonnet-4-6[1m]",
    "CLAUDE_CODE_SUBAGENT_MODEL": "claude-sonnet-4-6[1m]",

    # Set effort level to "high". Use with caution as it may increase latency and cost.
    # https://code.claude.com/docs/en/model-config#adjust-effort-level
    "CLAUDE_CODE_EFFORT_LEVEL": "high",
  }
```

### Permissions

```yaml
"permissions": {
    # Enable bypass permissions mode to allow all commands without explicit permissions. Use with caution.
    # https://code.claude.com/docs/en/permissions#permission-modes
    "defaultMode": "bypassPermissions",
  }
```

### Others

```yaml
# Hide all attribution.
# https://code.claude.com/docs/en/settings#attribution-settings
"attribution": { "commit": "", "pr": "" }
```

## Plan Mode

- https://github.com/FlorianBruniaux/claude-code-ultimate-guide/blob/main/guide/workflows/plan-driven.md
- [Plan Mode Deep Dive: Why External Spec Tools Are Redundant](https://www.youtube.com/watch?v=7j_d9jtrXVM)

## Tasks

- [Claude Code Just Got a Brain Upgrade Inspired By Beads](https://www.youtube.com/watch?v=-xOAYPjhigY)

## Setup

```sh
# Manage IDE integrations and show status
/ide
```

## Best Practices

- 📖 [Best Practices for Claude Code](https://code.claude.com/docs/en/best-practices)
- 💡 [Prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-4-best-practices)
- ✍️ [Skill authoring best practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices)
- 📚 [Claude Cookbooks](https://github.com/anthropics/claude-cookbooks#readme)
- 🔧 [Use Claude Code in VS Code](https://code.claude.com/docs/en/vs-code)
- 💭 [Boris Cherny Tips](https://x.com/bcherny/status/2007179832300581177)
- 🎯 [Claude Code Tips](https://github.com/ykdojo/claude-code-tips)

## 🛠️ Tools

- [Claude Code Usage Analyzer](https://github.com/ryoppippi/ccusage#readme)
- [Claude Code Viewer](https://github.com/d-kimuson/claude-code-viewer#readme)
- [Claude Task Viewer](https://github.com/L1AD/claude-task-viewer#readme)
- [claude-tasks-viewer](https://github.com/burke/claude-tasks-viewer#readme)
- [vibe-kanban](https://github.com/BloopAI/vibe-kanban#readme)
- [Auto Claude](https://github.com/AndyMik90/Auto-Claude#readme)

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
Save script to ~/.claude/statusline.sh and make it executable.
```

[source](https://x.com/claudeai/status/1999209597035331739)

## 🔌 Plugins

- 🎨 [Official Claude Code plugins repository](https://github.com/anthropics/claude-code/tree/main/plugins)

```sh
# List available plugins in JSON format.
# The repo does not contain a complete list of plugins.
claude plugin list --available --json > cc-plugins.json
```

### Installation

```sh
### Oficial Claude Code Plugins ###

# Claude Code Setup
# Analyze codebases and recommend tailored Claude Code automations such as hooks, skills, MCP servers, and subagents.
claude plugin install claude-code-setup

# CLAUDE.md Management
# Tools to maintain and improve CLAUDE.md files - audit quality, capture session learnings, and keep project memory current.
claude plugin install claude-md-management

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

# Hookify
# Easily create custom hooks to prevent unwanted behaviors by analyzing conversation patterns or from explicit instructions. Define rules via simple markdown files.
# https://github.com/anthropics/claude-plugins-official/tree/main/plugins/hookify
claude plugin install hookify

# Plugin Development Toolkit
# Comprehensive toolkit for developing Claude Code plugins. Includes 7 expert skills covering hooks, MCP integration, commands, agents, and best practices. AI-assisted plugin creation and validation.
# https://github.com/anthropics/claude-code/blob/main/plugins/plugin-dev/README.md
claude plugin install plugin-dev

# PR Review Toolkit
# Comprehensive PR review agents specializing in comments, tests, error handling, type design, code quality, and code simplification.
# https://github.com/anthropics/claude-code/blob/main/plugins/pr-review-toolkit/README.md
claude plugin install pr-review-toolkit

# Security Guidance
# Security reminder hook that warns about potential security issues when editing files, including command injection, XSS, and unsafe code patterns.
claude plugin install security-guidance

### Oficial LSP Plugins ###
# https://code.claude.com/docs/en/plugins-reference#lsp-servers

# Go LSP
# Go language server for code intelligence and refactoring.
# Install Go: https://go.dev/wiki/Ubuntu
# https://go.dev/gopls/
# https://marketplace.visualstudio.com/items?itemName=golang.go
go install golang.org/x/tools/gopls@latest
claude plugin install gopls-lsp

# Pyright LSP
# Python language server (Pyright) for type checking and code intelligence.
npm install -g pyright
claude plugin install pyright-lsp

# Rust Analyzer LSP
# Rust language server for code intelligence and analysis.
# Install Rust: https://rust-lang.org/tools/install/
# https://rust-analyzer.github.io/book/rust_analyzer_binary.html
# https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer
rustup component add rust-analyzer
claude plugin install rust-analyzer-lsp

# TypeScript LSP
# TypeScript/JavaScript language server for enhanced code intelligence.
npm install -g typescript-language-server typescript
claude plugin install typescript-lsp
```
