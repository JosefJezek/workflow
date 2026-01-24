# 🚀 My Workflow & Tools

My personal workflow and tools for AI-assisted development.

## 📑 Table of Contents

- [📋 Spec-Driven Development Workflow](#-spec-driven-development-workflow)
- [🤖 AI Models](#-ai-models)
- [💬 Claude Code](#-claude-code)
- [⚡ Terminal tools](#-terminal-tools)
- [✏️ Code editor](#️-code-editor)
- [🔀 AI Proxy](#-ai-proxy)
- [🧩 AI Agent Skills](#-ai-agent-skills)
- [📚 Docs as Agent Skills](#-docs-as-agent-skills)
- [✅ Best Practices References](#best-practices-references)

## Context-Driven Development with AI

- I use context-driven development to leverage AI models effectively.
- I provide AI models with relevant context from the codebase to improve their understanding and output quality.
- This approach helps AI models generate more accurate and context-aware code suggestions, reducing errors and improving overall code quality.

## 📋 Spec-Driven Development Workflow

I use Spec Kit for structured, specification-driven development with AI assistance.

[Spec Kit](https://github.com/github/spec-kit#readme) is a tool for creating, managing, and validating software specifications.

[Specification-Driven Development](https://github.com/github/spec-kit/blob/main/spec-driven.md) (SDD) is a development methodology that emphasizes creating detailed specifications before writing code. It ensures that the final product meets the defined requirements and behaves as expected.

### 🧪 Test-Driven Development (TDD)

I combine Spec Kit with TDD to ensure code quality and correctness.

### 🔄 Spec files can be updated

To update the spec file, you need to create a new git branch with the same prefix as the spec file folder.
For example, to update `specs/001-login-page/spec.md`, create a branch named `001-fix-submit-button`.

```sh
git checkout -b 001-fix-submit-button
/speckit.clarify Update the login page to fix the alignment issue of the submit button.
/speckit.plan Test cases should be updated accordingly to cover the new changes.
/speckit.tasks
/speckit.implement
```

### 📝 Workflow Steps

<details>
<summary>Click to expand workflow details</summary>

#### 1️⃣ Establish project principles

Use the **`/speckit.constitution`** command to create your project's governing principles and development guidelines that will **guide all subsequent development**.

TDD is optional in Spec Kit, but I enforce it strictly in my projects.

```bash
/speckit.constitution
Create principles focused on code quality, testing standards,
user experience consistency, and performance requirements.
This React project follows a "Library-First" approach where all features 
are implemented as standalone, reusable components and hooks first.
We prefer functional components with hooks over class components.
We use Test-Driven Development strictly with React Testing Library.
Breaking code into smaller modules is crucial - keep files around 250 lines.
Prioritize accessibility (a11y), semantic HTML, and keyboard navigation.
Components should be pure and side-effect free where possible.
Use TypeScript in strict mode for type safety and better developer experience.
```

#### 2️⃣ Create the spec file

Use the **`/speckit.specify`** command to describe what you want to build.
Focus on the **what** and **why**, not the tech stack.

The command will create new git branches for each spec file.

**Do not focus on the tech stack at this point.**

```bash
/speckit.specify Build an application that can help me organize my photos in separate photo albums. Albums are grouped by date and can be re-organized by dragging and dropping on the main page. Albums are never in other nested albums. Within each album, photos are previewed in a tile-like interface.
```

##### Clarify any ambiguities or missing details in the spec using the **`/speckit.clarify`** command

```bash
/speckit.clarify Focus on user-friendly design and intuitive drag-and-drop functionality. Ensure that the application is responsive and works well on both desktop and mobile devices.

/speckit.clarify Add support for common image formats like JPEG, PNG, and GIF. Include basic photo editing features such as cropping and rotating within the album view.
```

##### Validate the specification checklist using the `/speckit.checklist` command

```bash
/speckit.checklist
```

#### 3️⃣ Create a technical implementation plan

Use the **`/speckit.plan`** command to provide your tech stack and architecture choices.

```bash
/speckit.plan The application uses Vite with a minimal number of libraries. Use vanilla HTML, CSS, and JavaScript as much as possible. Images are not uploaded anywhere and metadata is stored in a local SQLite database.
```

#### 4️⃣ Break down into tasks

Use **`/speckit.tasks`** to create an actionable task list from your implementation plan.

```bash
/speckit.tasks
```

##### Optionally, validate the plan with `/speckit.analyze`:

```bash
/speckit.analyze
```

#### 5️⃣ Execute implementation

Use **`/speckit.implement`** to execute all tasks and build your feature according to the plan.

```bash
/speckit.implement
```

</details>

## 🤖 AI Models

- 🎯 Claude Opus for specification-driven development.
- ⚡ Claude Sonnet for general coding tasks.

### 📊 Comparisons

- [Claude Opus 4.5 vs GPT 5.2 High vs Gemini 3 Pro](https://dev.to/tensorlake/claude-opus-45-vs-gpt-52-high-vs-gemini-3-pro-production-coding-test-25of)

<details>
<summary>Click to expand more comparisons</summary>

- Sorry but in like 90% of cases GLM 4.7 (thinking!) is not even close to Opus 4.5. We are using both across multiple GH orgs tons of repos mostly larger JS and PHP codebases. The way Opus does things is just on a totally different level it actually seems aware of the consequences of every single change and catches stuff GLM skips entirely. Please dont just rely on benchmark data when saying they are on the same level for coding because thats simply not true.
- Agreed. Over 3 hours today, Opus 4.5 helped me ship a feature I've spent 100+ hours on over the past 6 months (to no avail). The closest any other model got was GPT 5.2 and only today did I realize how terribly far off it was to the real solution. Today Opus 4.5 and I did it in 3 hours. It's the only model that seems to truly think.
- That is absolutely true. All these clickbaits are just a waste of time. Nothing comes close to Opus 4.5 if you are a developer/ vibe-coder. I believed this nonsense once and configured GLM 4.7 in Claude Code CLI. Tried it for 2 days. Terrible! Even Codex 5.2 is far far behind Opus 4.5. All these clickbait videos need to stop!!!

</details>

## 💬 Claude Code

[Claude Code](https://github.com/anthropics/claude-code#readme) is a CLI tool to interact with Claude models from the terminal.

- 📖 [Best Practices for Claude Code](https://code.claude.com/docs/en/best-practices)
- 💡 [Prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-4-best-practices)
- ✍️ [Skill authoring best practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices)
- 📚 [Claude Cookbooks](https://github.com/anthropics/claude-cookbooks#readme)
- 🔧 [Use Claude Code in VS Code](https://code.claude.com/docs/en/vs-code)
- 💭 [Boris Cherny Tips](https://x.com/bcherny/status/2007179832300581177)
- 🎯 [Claude Code Tips](https://github.com/ykdojo/claude-code-tips)

### 🛠️ Tools

- 📊 [Claude Code Usage Analyzer](https://github.com/ryoppippi/ccusage#readme)
- [Claude Task Viewer](https://github.com/L1AD/claude-task-viewer#readme)
- [claude-tasks-viewer](https://github.com/burke/claude-tasks-viewer#readme)

### Tasks

`CLAUDE_CODE_TASK_LIST_ID=test claude`

- [Tasks are a new primitive that help Claude Code track projects](https://x.com/bcherny/status/2014485078815211652)

### 📟 Status line

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

### 🔌 Plugins

- 🎨 [Official Claude Code plugins](https://github.com/anthropics/claude-code/tree/main/plugins)

```sh
claude plugin list --available --json > cc-plugins.json
```

<details>
<summary>Click to expand list of plugins</summary>

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

</details>

## ⚡ Terminal tools

- 👻 [Ghostty](https://github.com/ghostty/ghostty#readme)
- 🐠 [Fish Shell](https://github.com/fish-shell/fish-shell#readme)
- 🚀 [Starship](https://github.com/starship/starship#readme)
- 🍞 [Bun](https://github.com/oven-sh/bun#readme)

## ✏️ Code editor

[VS Code](https://github.com/microsoft/vscode#readme) with [Dev Containers](https://code.visualstudio.com/docs/devcontainers/containers) for consistent development environments.

- 🎥 [Run Your AI Coding Agent in Containers](https://www.youtube.com/watch?v=w3kI6XlZXZQ)

### 🧩 Extensions

- 🤖 [Copilot Chat](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat)
- 📦 [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
- 🔄 [GitHub Pull Requests](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
- ⚙️ [GitHub Actions](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-github-actions)
- 🎯 [Voight](https://marketplace.visualstudio.com/items?itemName=SwaritPandey.voight)

## 🔀 AI Proxy

Proxy server to manage requests and costs.

- 🔌 [9Router](https://github.com/decolua/9router#readme)
- 🌌 [Antigravity](https://antigravity.google) - Opus, Sonnet, Gemini

## 🧩 AI Agent Skills

See [SKILLS.md](SKILLS.md) for a comprehensive list of agent skills, documentation skills, and installation commands.

## Best Practices References

- https://www.vibekanban.com/vibe-guide
- https://repomix.com/guide/tips/best-practices
- https://claudekit.cc/blog/vc-07-claude-code-common-mistakes-production-ready-project
- https://github.com/mrgoonie/claudekit-skills/blob/main/REFACTOR.md
