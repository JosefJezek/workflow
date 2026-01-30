# Research-Driven Development (RDD)

> "Code is Truth, but Context is the Map."

The [Research-Driven Development](https://github.com/bgauryy/octocode-mcp/blob/main/MANIFEST.md) (RDD) methodology emphasizes the importance of thorough research and context gathering before diving into coding tasks.

## Octocode

[Octocode](https://github.com/bgauryy/octocode-mcp#readme) leverages RDD to ensure that AI-assisted development is grounded in a deep understanding of the problem domain, user needs, and existing solutions.

### Documentation Writer Skill

The skill is alternative to [DeepWiki](https://deepwiki.com) or [Code Wiki](https://codewiki.google) for generating documentation from codebases.

- https://github.com/bgauryy/octocode-mcp/tree/main/skills/octocode-documentaion-writer
- https://www.linkedin.com/posts/bgauryy_octocode-vs-deepwiki-by-cognition-ai-research-activity-7384197129247993856-7lrU/
- https://github.com/AsyncFuncAI/deepwiki-open

```sh
/octocode-documentaion-writer
```

### Research Skill

The Research Skill enables developers to conduct in-depth research on codebases, libraries, and frameworks directly within their development environment.

The skill auto-selects the right workflow based on your question:

| Your Intent | Auto-Selected Prompt | What Happens |
|-------------|---------------------|--------------|
| *"How does React useState work?"* | `research` | GitHub repo exploration, source code analysis |
| *"Trace the auth flow in our app"* | `research_local` | LSP-powered semantic analysis, call hierarchies |
| *"Review PR #123"* | `reviewPR` | Diff analysis, code review, change impact |
| *"Plan adding caching to the API"* | `plan` | Architecture design, implementation steps |

- https://github.com/bgauryy/octocode-mcp/tree/main/skills/octocode-research
- https://medium.com/@guybary/octocode-research-skill-b8248214b515

```sh
/octocode-research How does React useState work?
```

## Repomix

[Repomix](https://github.com/yamadashy/repomix#readme) is a powerful tool that packs your entire repository into a single, AI-friendly file.

It is perfect for when you need to feed your codebase to Large Language Models (LLMs) with 1M token context window for analysis, refactoring, or enhancement.

### Explorer Skill

The Explorer Skill allows you to analyze and explore code repositories effectively using single-file representation.

- https://github.com/yamadashy/repomix?tab=readme-ov-file#repomix-explorer-skill-agent-skills
- https://github.com/yamadashy/repomix/blob/main/.claude/skills/repomix-explorer/SKILL.md

```sh
/repomix-explorer Analyze the code quality of this repository and suggest improvements.
```

### Skill Generator

The Skill Generator enables you to create custom agent skills based on your codebase, enhancing AI-assisted development workflows.

- https://github.com/yamadashy/repomix/tree/main?tab=readme-ov-file#agent-skills-generation-1

```sh
npx repomix src/ --skill-generate repomix-codebase-reference-src
```
