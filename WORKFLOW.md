# 🎯 Workflow

My personal development workflows for AI-assisted development.

## 📑 Table of Contents

## Greenfield Projects

## Brownfield Projects

For existing brownfield projects, I primarily use the Context-Driven Development Workflow to enhance and maintain the codebase effectively.

### Documentation First Approach

#### Generating Documentation with Octocode

I use the Documentation Writer Skill from Octocode to generate and maintain up-to-date documentation for my codebases.
This helps ensure that both human developers and AI models have a clear understanding of the code structure and functionality.

For more information, see the [Documentation Writer Skill](RDD.md#documentation-writer-skill).

```sh
/octocode-documentaion-writer
```

#### Creating Codebase Reference Skill with Repomix

I use Repomix to generate a comprehensive codebase reference skill for better navigation and understanding of the project structure.

For more information, see the [Skill Generator](RDD.md#skill-generator).

```sh
npx repomix src/ --skill-generate repomix-codebase-reference-src
```

#### Creating Codebase Reference in one file with Repomix

I use Repomix to create a single-file representation of the entire codebase for easy analysis and exploration by AI models.

For more information, see the [Explorer Skill](RDD.md#explorer-skill).

```sh
npx repomix@latest
```

> This file contains all the files in the repository combined into one.
> I want to refactor the code, so please review it first.

## 🎯 Context-Driven Development Workflow

I fetch source code using [opensrc](https://github.com/vercel-labs/opensrc#readme) for npm packages to give coding agents deeper context than types alone.

```sh
# Install opensrc globally
npm install -g opensrc

# Fetch source code for packages used in the project
opensrc react react-dom zod
```

For more information, see [Context-Driven Development (CDD)](CDD.md).

## 📋 Spec-Driven Development Workflow

I use Spec Kit for structured, specification-driven development with AI assistance.

[Spec Kit](https://github.com/github/spec-kit#readme) is a tool for creating, managing, and validating software specifications.

For more information, see [Spec-Driven Development (SDD)](SDD.md).

### 🧪 Test-Driven Development (TDD)

I combine Spec Kit with TDD to ensure code quality and correctness.

For more information, see [Test-Driven Development (TDD)](TDD.md).

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

### constitution.md vs AGENTS.md

- File `.specify/memory/constitution.md` is used to define the project's principles and guidelines that govern the development process.

### 📝 Workflow Steps

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

## Claude Code Insights

The /insights command in Claude Code generates a comprehensive HTML report analyzing your usage patterns across all your Claude Code sessions.
It’s designed to help you understand how you interact with Claude, what’s working well, where friction occurs, and how to improve your workflows.

- https://www.zolkos.com/2026/02/04/deep-dive-how-claude-codes-insights-command-works.html

```sh
/insights
```
