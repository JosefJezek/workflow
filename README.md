# My Workflow

## Models

- Claude Opus 4.5
- Claude Sonnet 4.5

## IDE

VS Code with GitHub Copilot.

## Proxy

- [9Router](https://github.com/decolua/9router)
- Antigravity - Opus, Sonnet, Gemini

## Spec-Driven Development

### [Spec Kit](https://github.com/github/spec-kit)

Spec Kit is a tool for creating, managing, and validating software specifications.

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

## Agent Skills

### [docs-seeker](https://github.com/mrgoonie/claudekit-skills/blob/main/.claude/skills/docs-seeker/SKILL.md)

Searching internet for technical documentation using llms.txt standard, GitHub repositories via Repomix, and parallel exploration.

#### Use when user needs

1. Latest documentation for libraries/frameworks
2. Documentation in llms.txt format
3. GitHub repository analysis
4. Documentation without direct llms.txt support
5. Multiple documentation sources in parallel

#### Installation

```sh
bunx add-skill mrgoonie/claudekit-skills -y -g -s docs-seeker
```

### [doc-coauthoring](https://github.com/anthropics/skills/blob/main/skills/doc-coauthoring/SKILL.md)

Guide users through a structured workflow for co-authoring documentation.
Use when user wants to write documentation, proposals, technical specs, decision docs, or similar structured content.
This workflow helps users efficiently transfer context, refine content through iteration, and verify the doc works for readers. Trigger when user mentions writing docs, creating proposals, drafting specs, or similar documentation tasks.

#### Installation

```sh
bunx add-skill anthropics/skills -y -g -s doc-coauthoring
```

### [claude-opus-4-5-migration](https://github.com/anthropics/claude-code/blob/main/plugins/claude-opus-4-5-migration/skills/claude-opus-4-5-migration/SKILL.md)

Migrate prompts and code from Claude Sonnet 4.0, Sonnet 4.5, or Opus 4.1 to Opus 4.5.
Use when the user wants to update their codebase, prompts, or API calls to use Opus 4.5.
Handles model string updates and prompt adjustments for known Opus 4.5 behavioral differences. Does NOT migrate Haiku 4.5.

#### Installation

```sh
bunx add-skill anthropics/claude-code -y -g -s claude-opus-4-5-migration
```

### [skill-creator](https://github.com/anthropics/skills/blob/main/skills/skill-creator/SKILL.md)

Guide for creating effective skills.
This skill should be used when users want to create a new skill (or update an existing skill) that extends Claude's capabilities with specialized knowledge, workflows, or tool integrations.

#### Installation

```sh
bunx add-skill anthropics/skills -y -g -s skill-creator
```

### [react-best-practices](https://github.com/vercel-labs/agent-skills/blob/main/skills/react-best-practices/SKILL.md)

React and Next.js performance optimization guidelines from Vercel Engineering.
This skill should be used when writing, reviewing, or refactoring React/Next.js code to ensure optimal performance patterns. Triggers on tasks involving React components, Next.js pages, data fetching, bundle optimization, or performance improvements.

#### Installation

```sh
bunx add-skill vercel-labs/agent-skills -y -g -s react-best-practices
```

### [web-design-guidelines](https://github.com/vercel-labs/agent-skills/blob/main/skills/web-design-guidelines/SKILL.md)

Review UI code for Web Interface Guidelines compliance.
Use when asked to "review my UI", "check accessibility", "audit design", "review UX", or "check my site against best practices".

#### Installation

```sh
bunx add-skill vercel-labs/agent-skills -y -g -s web-design-guidelines
```
