# My Workflow & Tools

My personal workflow and tools for AI-assisted development.

## Table of Contents

- [Spec-Driven Development Workflow](#spec-driven-development-workflow)
- [AI Models](#ai-models)
- [Claude Code](#claude-code)
- [Terminal tools](#terminal-tools)
- [Code editor and extensions](#code-editor-and-extensions)
- [AI Proxy](#ai-proxy)
- [AI Agent Skills](#ai-agent-skills)
- [Docs as Agent Skills](#docs-as-agent-skills)

## Spec-Driven Development Workflow

I use Spec Kit for structured, specification-driven development with AI assistance.

[Spec Kit](https://github.com/github/spec-kit#readme) is a tool for creating, managing, and validating software specifications.

<details>
<summary>Click to expand workflow details</summary>

### 1. Establish project principles

Launch your AI assistant in the project directory. The `/speckit.*` commands are available in the assistant.

Use the **`/speckit.constitution`** command to create your project's governing principles and development guidelines that will guide all subsequent development.

```bash
/speckit.constitution Create principles focused on code quality, testing standards, user experience consistency, and performance requirements
```

### 2. Create the spec

Use the **`/speckit.specify`** command to describe what you want to build. Focus on the **what** and **why**, not the tech stack.

```bash
/speckit.specify Build an application that can help me organize my photos in separate photo albums. Albums are grouped by date and can be re-organized by dragging and dropping on the main page. Albums are never in other nested albums. Within each album, photos are previewed in a tile-like interface.
```

### 3. Create a technical implementation plan

Use the **`/speckit.plan`** command to provide your tech stack and architecture choices.

```bash
/speckit.plan The application uses Vite with minimal number of libraries. Use vanilla HTML, CSS, and JavaScript as much as possible. Images are not uploaded anywhere and metadata is stored in a local SQLite database.
```

### 4. Break down into tasks

Use **`/speckit.tasks`** to create an actionable task list from your implementation plan.

```bash
/speckit.tasks
```

### 5. Execute implementation

Use **`/speckit.implement`** to execute all tasks and build your feature according to the plan.

```bash
/speckit.implement
```

</details>

## AI Models

- Claude Opus for specification-driven development.
- Claude Sonnet for general coding tasks.

## Claude Code

[Claude Code](https://github.com/anthropics/claude-code#readme) is CLI tool to interact with Claude models from the terminal.

### Plugins

- https://github.com/anthropics/claude-code/tree/main/plugins

## Terminal tools

- [Ghostty](https://github.com/ghostty/ghostty#readme)
- [Fish Shell](https://github.com/fish-shell/fish-shell#readme)
- [Starship](https://github.com/starship/starship#readme)
- [Bun](https://github.com/oven-sh/bun#readme)

## Code editor and extensions

- [VS Code](https://github.com/microsoft/vscode#readme)
  - [Copilot Chat](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat)
  - [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
    - [Run Your AI Coding Agent in Containers](https://www.youtube.com/watch?v=w3kI6XlZXZQ)
  - [GitHub Pull Requests](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
  - [GitHub Actions](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-github-actions)
  - [Voight](https://marketplace.visualstudio.com/items?itemName=SwaritPandey.voight)

## AI Proxy

Proxy server to manage requests and costs.

- [9Router](https://github.com/decolua/9router#readme)
- [Antigravity](https://antigravity.google) - Opus, Sonnet, Gemini

## AI Agent Skills

[Agent skills](https://agentskills.io) extend AI capabilities with specialized knowledge, workflows, or tool integrations.

- [skillsdirectory.com](https://www.skillsdirectory.com)

<details>
<summary>Click to expand list of agent skills</summary>

### [doc-coauthoring](https://github.com/anthropics/skills/blob/main/skills/doc-coauthoring/SKILL.md)

Guide users through a structured workflow for co-authoring documentation.
Use when user wants to write documentation, proposals, technical specs, decision docs, or similar structured content.
This workflow helps users efficiently transfer context, refine content through iteration, and verify the doc works for readers.
Trigger when user mentions writing docs, creating proposals, drafting specs, or similar documentation tasks.

```sh
bunx add-skill anthropics/skills -y -g -s doc-coauthoring
```

### [claude-opus-4-5-migration](https://github.com/anthropics/claude-code/blob/main/plugins/claude-opus-4-5-migration/skills/claude-opus-4-5-migration/SKILL.md)

Migrate prompts and code from Claude Sonnet 4.0, Sonnet 4.5, or Opus 4.1 to Opus 4.5.
Use when the user wants to update their codebase, prompts, or API calls to use Opus 4.5.
Handles model string updates and prompt adjustments for known Opus 4.5 behavioral differences.
Does NOT migrate Haiku 4.5.

```sh
bunx add-skill anthropics/claude-code -y -g -s claude-opus-4-5-migration
```

### [skill-creator](https://github.com/anthropics/skills/blob/main/skills/skill-creator/SKILL.md)

Guide for creating effective skills.
This skill should be used when users want to create a new skill (or update an existing skill) that extends Claude's capabilities with specialized knowledge, workflows, or tool integrations.

```sh
bunx add-skill anthropics/skills -y -g -s skill-creator
```

### [react-best-practices](https://github.com/vercel-labs/agent-skills/blob/main/skills/react-best-practices/SKILL.md)

React and Next.js performance optimization guidelines from Vercel Engineering.
This skill should be used when writing, reviewing, or refactoring React/Next.js code to ensure optimal performance patterns. Triggers on tasks involving React components, Next.js pages, data fetching, bundle optimization, or performance improvements.

```sh
bunx add-skill vercel-labs/agent-skills -y -g -s react-best-practices
```

### [web-design-guidelines](https://github.com/vercel-labs/agent-skills/blob/main/skills/web-design-guidelines/SKILL.md)

Review UI code for Web Interface Guidelines compliance.
Use when asked to "review my UI", "check accessibility", "audit design", "review UX", or "check my site against best practices".

```sh
bunx add-skill vercel-labs/agent-skills -y -g -s web-design-guidelines
```

### [agent-browser](https://github.com/vercel-labs/agent-browser#readme)

Headless browser automation CLI for AI agents. Fast Rust CLI with Node.js fallback.

```sh
bun pm trust -g agent-browser
bun add -g agent-browser
agent-browser install
bunx add-skill vercel-labs/agent-browser -y -g -s agent-browser
```

</details>

## Docs as Agent Skills

[Repomix](https://github.com/yamadashy/repomix#readme) can convert documentation into agent skills for enhanced AI interaction.

<details>
<summary>Click to expand list of agent skills</summary>

```sh
# Base UI Docs
# https://github.com/mui/base-ui/tree/master/docs
bunx repomix --remote mui/base-ui --include docs --skill-generate docs-base-ui

# Better Auth Docs
# https://github.com/better-auth/better-auth/tree/canary/docs
bunx repomix --remote better-auth/better-auth --include docs --skill-generate docs-better-auth

# Claude Code Action Docs
# https://github.com/anthropics/claude-code-action/tree/main/docs
bunx repomix --remote anthropics/claude-code-action --include docs --skill-generate docs-claude-code-action

# React Docs
# https://github.com/reactjs/react.dev/tree/main/src/content
bunx repomix --remote reactjs/react.dev --include src/content --skill-generate docs-react

# React Error Boundary Docs
# https://github.com/bvaughn/react-error-boundary/tree/main/public/generated
bunx repomix --remote bvaughn/react-error-boundary --include public/generated --skill-generate docs-react-error-boundary

# React Testing Library Docs
# https://github.com/testing-library/testing-library-docs/tree/main/docs/react-testing-library
bunx repomix --remote testing-library/testing-library-docs --include docs/react-testing-library --skill-generate docs-react-testing-library

# Shadcn UI Docs
# https://github.com/shadcn-ui/ui/tree/main/apps/v4/content/docs
bunx repomix --remote shadcn-ui/ui --include apps/v4/content/docs --skill-generate docs-shadcn-ui

# Storybook Docs
# https://github.com/storybookjs/storybook/tree/next/docs
bunx repomix --remote storybookjs/storybook --include docs --skill-generate docs-storybook

# Tailwind CSS Docs
# https://github.com/tailwindlabs/tailwindcss.com/tree/main/src/docs
bunx repomix --remote tailwindlabs/tailwindcss.com --include src/docs --skill-generate docs-tailwind-css

# Tailwind Variants Docs
# https://github.com/heroui-inc/tailwind-variants-docs/tree/main/pages/docs
bunx repomix --remote heroui-inc/tailwind-variants-docs --include pages/docs --skill-generate docs-tailwind-variants

# TanStack Form Docs
# https://github.com/TanStack/form/tree/main/docs
bunx repomix --remote TanStack/form --include docs --skill-generate docs-tanstack-form

# TanStack Query Docs
# https://github.com/TanStack/query/tree/main/docs
bunx repomix --remote TanStack/query --include docs --skill-generate docs-tanstack-query

# TanStack Router Docs
# https://github.com/TanStack/router/tree/main/docs/router
bunx repomix --remote TanStack/router --include docs/router --skill-generate docs-tanstack-router

# TypeScript Docs
# https://github.com/microsoft/TypeScript-Website/tree/v2/packages/documentation/copy/en
bunx repomix --remote microsoft/TypeScript-Website --include packages/documentation/copy/en --skill-generate docs-typescript

# Vite Docs
# https://github.com/vitejs/vite/tree/main/docs
bunx repomix --remote vitejs/vite --include docs --skill-generate docs-vite

# Vitest Docs
# https://github.com/vitest-dev/vitest/tree/main/docs
bunx repomix --remote vitest-dev/vitest --include docs --skill-generate docs-vitest

# Zod Docs
# https://github.com/colinhacks/zod/tree/main/packages/docs
bunx repomix --remote colinhacks/zod --include packages/docs --skill-generate docs-zod

# Zustand Docs
# https://github.com/pmndrs/zustand/tree/main/docs
bunx repomix --remote pmndrs/zustand --include docs --skill-generate docs-zustand
```

</details>
