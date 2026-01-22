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
- [Best Practices References](#best-practices-references)

## Spec-Driven Development Workflow

I use Spec Kit for structured, specification-driven development with AI assistance.

[Spec Kit](https://github.com/github/spec-kit#readme) is a tool for creating, managing, and validating software specifications.

[Specification-Driven Development](https://github.com/github/spec-kit/blob/main/spec-driven.md) (SDD) is a development methodology that emphasizes creating detailed specifications before writing code. It ensures that the final product meets the defined requirements and behaves as expected.

### Test-Driven Development (TDD)

I combine Spec Kit with TDD to ensure code quality and correctness.

### Spec files can be updated

To update the spec file, you need to create a new git branch with the same prefix as the spec file folder.
For example, to update `specs/001-login-page/spec.md`, create a branch named `001-fix-bug`.

```sh
git checkout -b 001-fix-bug
/speckit.clarify Update the login page to fix the alignment issue of the submit button.
/speckit.plan Try to keep the same tech stack and architecture as before. Test cases should be updated accordingly to cover the new changes.
/speckit.tasks
/speckit.implement
```

### Workflow Steps

<details>
<summary>Click to expand workflow details</summary>

#### 1. Establish project principles

Use the **`/speckit.constitution`** command to create your project's governing principles and development guidelines that will guide all subsequent development.

TDD is optional in Spec Kit, but I enforce it strictly in my projects.

```bash
/speckit.constitution We use TDD strictly. Create principles focused on code quality, testing standards, user experience consistency, and performance requirements. This project follows a "Library-First" approach. All features must be implemented as standalone libraries first. We prefer functional programming patterns.
```

#### 2. Create the spec file

Use the **`/speckit.specify`** command to describe what you want to build. Focus on the **what** and **why**, not the tech stack.

The command will create new git branches for each spec file.

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

#### 3. Create a technical implementation plan

Use the **`/speckit.plan`** command to provide your tech stack and architecture choices.

```bash
/speckit.plan The application uses Vite with a minimal number of libraries. Use vanilla HTML, CSS, and JavaScript as much as possible. Images are not uploaded anywhere and metadata is stored in a local SQLite database.
```

#### 4. Break down into tasks

Use **`/speckit.tasks`** to create an actionable task list from your implementation plan.

```bash
/speckit.tasks
```

##### Optionally, validate the plan with `/speckit.analyze`:

```bash
/speckit.analyze
```

#### 5. Execute implementation

Use **`/speckit.implement`** to execute all tasks and build your feature according to the plan.

```bash
/speckit.implement
```

</details>

## AI Models

- Claude Opus for specification-driven development.
- Claude Sonnet for general coding tasks.

### Comparisons

- [Claude Opus 4.5 vs GPT 5.2 High vs Gemini 3 Pro](https://dev.to/tensorlake/claude-opus-45-vs-gpt-52-high-vs-gemini-3-pro-production-coding-test-25of)

## Claude Code

[Claude Code](https://github.com/anthropics/claude-code#readme) is a CLI tool to interact with Claude models from the terminal.

### Plugins

- https://github.com/anthropics/claude-code/tree/main/plugins

## Terminal tools

- [Ghostty](https://github.com/ghostty/ghostty#readme)
- [Fish Shell](https://github.com/fish-shell/fish-shell#readme)
- [Starship](https://github.com/starship/starship#readme)
- [Bun](https://github.com/oven-sh/bun#readme)

## Code editor

[VS Code](https://github.com/microsoft/vscode#readme) with [Dev Containers](https://code.visualstudio.com/docs/devcontainers/containers) for consistent development environments.

- [Run Your AI Coding Agent in Containers](https://www.youtube.com/watch?v=w3kI6XlZXZQ)

### Extensions

- [Copilot Chat](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat)
- [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
- [GitHub Pull Requests](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
- [GitHub Actions](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-github-actions)
- [Voight](https://marketplace.visualstudio.com/items?itemName=SwaritPandey.voight)

## AI Proxy

Proxy server to manage requests and costs.

- [9Router](https://github.com/decolua/9router#readme)
- [Antigravity](https://antigravity.google) - Opus, Sonnet, Gemini

## AI Agent Skills

[Agent skills](https://agentskills.io) extend AI capabilities with specialized knowledge, workflows, or tool integrations.

- [skills.sh](https://skills.sh)
- [skillsdirectory.com](https://www.skillsdirectory.com)

<details>
<summary>Click to expand list of agent skills</summary>

```sh
# agent-browser
# https://github.com/vercel-labs/agent-browser#readme
# Prompt: Dark mode is broken, test it on http://localhost:3000 and fix it.
bun pm trust -g agent-browser
bun add -g agent-browser
agent-browser install
bunx add-skill vercel-labs/agent-browser -y -g -s agent-browser

# better-auth-best-practices
# https://github.com/better-auth/skills/blob/main/better-auth/best-practices/SKILL.md
# create-auth-skill
# https://github.com/better-auth/skills/blob/main/better-auth/create-auth/SKILL.md
bunx add-skill better-auth/skills -y -g -s better-auth-best-practices -s create-auth-skill

# claude-opus-4-5-migration
# https://github.com/anthropics/claude-code/blob/main/plugins/claude-opus-4-5-migration/skills/claude-opus-4-5-migration/SKILL.md
bunx add-skill anthropics/claude-code -y -g -s claude-opus-4-5-migration

# doc-coauthoring
# https://github.com/anthropics/skills/blob/main/skills/doc-coauthoring/SKILL.md
bunx add-skill anthropics/skills -y -g -s doc-coauthoring

# repomix-explorer
# https://github.com/yamadashy/repomix/blob/main/.claude/skills/repomix-explorer/SKILL.md
# https://repomix.com/guide/repomix-explorer-skill
# Prompts:
# Find all authentication-related code in this repository.
# Analyze the repository and provide an overview of its structure, key components, and any potential areas for improvement.
# I want to implement a similar feature to what I did in my other project. ~/projects/my-other-app
bunx add-skill yamadashy/repomix -y -g -s repomix-explorer

# skill-creator
# https://github.com/anthropics/skills/blob/main/skills/skill-creator/SKILL.md
bunx add-skill anthropics/skills -y -g -s skill-creator

# vercel-react-best-practices
# https://github.com/vercel-labs/agent-skills/blob/main/skills/react-best-practices/SKILL.md
# Prompt: Assess this repo against React best practices. Make a prioritized list of quick wins and top fixes.
bunx add-skill vercel-labs/agent-skills -y -g -s vercel-react-best-practices

# web-design-guidelines
# https://github.com/vercel-labs/agent-skills/blob/main/skills/web-design-guidelines/SKILL.md
bunx add-skill vercel-labs/agent-skills -y -g -s web-design-guidelines
```

</details>

## Docs as Agent Skills

[Repomix](https://github.com/yamadashy/repomix#readme) can convert documentation into agent skills for enhanced AI interaction.

<details>
<summary>Click to expand list of agent skills</summary>

```sh
# AI SDK Docs
# https://github.com/vercel/ai/tree/main/content
bunx repomix --remote vercel/ai --include content --skill-generate docs-ai-sdk

# Alibaba Hooks Docs
# https://github.com/alibaba/hooks/tree/master/docs
bunx repomix --remote alibaba/hooks --include docs --skill-generate docs-ahooks

# Base UI Docs
# https://github.com/mui/base-ui/tree/master/docs
bunx repomix --remote mui/base-ui --include docs --skill-generate docs-base-ui

# Better Auth Docs
# https://github.com/better-auth/better-auth/tree/canary/docs
bunx repomix --remote better-auth/better-auth --include docs --skill-generate docs-better-auth

# Claude Code Action Docs
# https://github.com/anthropics/claude-code-action/tree/main/docs
bunx repomix --remote anthropics/claude-code-action --include docs --skill-generate docs-claude-code-action

# Cloudflare Docs
# https://github.com/cloudflare/cloudflare-docs/tree/production/src/content/docs
bunx repomix --remote cloudflare/cloudflare-docs --include src/content/docs --skill-generate docs-cloudflare

# Drizzle ORM Docs
# https://github.com/drizzle-team/drizzle-orm-docs/tree/main/src/content/docs
bunx repomix --remote drizzle-team/drizzle-orm-docs --include src/content/docs --skill-generate docs-drizzle-orm

# Motion React Examples
# https://github.com/motiondivision/motion/tree/main/dev/react/src/examples
bunx repomix --remote motiondivision/motion --include dev/react/src/examples --skill-generate docs-motion-react-examples

# React Docs
# https://github.com/reactjs/react.dev/tree/main/src/content
bunx repomix --remote reactjs/react.dev --include src/content --skill-generate docs-react

# React Error Boundary Docs
# https://github.com/bvaughn/react-error-boundary/tree/main/public/generated
bunx repomix --remote bvaughn/react-error-boundary --include public/generated --skill-generate docs-react-error-boundary

# React Testing Library Docs
# https://github.com/testing-library/testing-library-docs/tree/main/docs/react-testing-library
bunx repomix --remote testing-library/testing-library-docs --include docs/react-testing-library --skill-generate docs-react-testing-library

# Rooks Docs
# https://github.com/imbhargav5/rooks/tree/main/apps/website/content/docs
bunx repomix --remote imbhargav5/rooks --include apps/website/content/docs --skill-generate docs-rooks

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

# TanStack DB Docs
# https://github.com/TanStack/db/tree/main/docs
bunx repomix --remote TanStack/db --include docs --skill-generate docs-tanstack-db

# TanStack Form Docs
# https://github.com/TanStack/form/tree/main/docs
bunx repomix --remote TanStack/form --include docs --skill-generate docs-tanstack-form

# TanStack Pacer Docs
# https://github.com/TanStack/pacer/tree/main/docs
bunx repomix --remote TanStack/pacer --include docs --skill-generate docs-tanstack-pacer

# TanStack Query Docs
# https://github.com/TanStack/query/tree/main/docs
bunx repomix --remote TanStack/query --include docs --skill-generate docs-tanstack-query

# TanStack Ranger Docs
# https://github.com/TanStack/ranger/tree/main/docs
bunx repomix --remote TanStack/ranger --include docs --skill-generate docs-tanstack-ranger

# TanStack Router Docs
# https://github.com/TanStack/router/tree/main/docs/router
bunx repomix --remote TanStack/router --include docs/router --skill-generate docs-tanstack-router

# TanStack Start Docs
# https://github.com/TanStack/router/tree/main/docs/start
bunx repomix --remote TanStack/router --include docs/start --skill-generate docs-tanstack-start

# TanStack Table Docs
# https://github.com/TanStack/table/tree/main/docs
bunx repomix --remote TanStack/table --include docs --skill-generate docs-tanstack-table

# TanStack Virtual Docs
# https://github.com/TanStack/virtual/tree/main/docs
bunx repomix --remote TanStack/virtual --include docs --skill-generate docs-tanstack-virtual

# TW Animate CSS Docs
# https://github.com/Wombosvideo/tw-animate-css/tree/main/docs
bunx repomix --remote Wombosvideo/tw-animate-css --include docs --skill-generate docs-tw-animate-css

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

## Best Practices References

- https://www.vibekanban.com/vibe-guide
- https://repomix.com/guide/tips/best-practices
- https://github.com/ykdojo/claude-code-tips
- https://claudekit.cc/blog/vc-07-claude-code-common-mistakes-production-ready-project
- https://x.com/bcherny/status/2007179832300581177
- https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices
- https://github.com/mrgoonie/claudekit-skills/blob/main/REFACTOR.md
