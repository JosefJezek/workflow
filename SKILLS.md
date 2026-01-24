# 🧩 Agent Skills

[Agent skills](https://agentskills.io) extend AI capabilities with specialized knowledge, workflows, or tool integrations.

## 📚 Skill Repositories

- 🎓 [skills.sh](https://skills.sh)
- 📖 [skillsdirectory.com](https://www.skillsdirectory.com)
- 🏛️ [Anthropics Skills](https://github.com/anthropics/skills#readme)

## ⚙️ Installing Skills

- Used with `bunx --bun skills add <repo> -y -g -s <skill-name>`.
- Tool [add-skill](https://github.com/vercel-labs/add-skill) installs the skill globally (-g) for all agents.

```sh
# agent-browser
# Headless browser automation CLI tool for AI agents.
# https://github.com/vercel-labs/agent-browser#readme
# Prompt: Dark mode is broken, test it on http://localhost:3000 and fix it.
bun pm trust -g agent-browser
bun add -g agent-browser
agent-browser install
bunx --bun skills add vercel-labs/agent-browser -y -g -s agent-browser

# better-auth: better-auth-best-practices, create-auth-skill
# Better Auth integration guides.
# https://github.com/better-auth/skills/blob/main/better-auth/best-practices/SKILL.md
# https://github.com/better-auth/skills/blob/main/better-auth/create-auth/SKILL.md
bunx --bun skills add better-auth/skills -y -g -s better-auth-best-practices -s create-auth-skill

# claude-opus-4-5-migration
# Migrate prompts and code to Opus 4.5.
# https://github.com/anthropics/claude-code/blob/main/plugins/claude-opus-4-5-migration/skills/claude-opus-4-5-migration/SKILL.md
bunx --bun skills add anthropics/claude-code -y -g -s claude-opus-4-5-migration

# context7: documentation-lookup
# Fallback for local docs skills from Repomix.
# Local docs skills does not cover all libraries.
# https://github.com/upstash/context7/tree/master/plugins/claude/context7
# https://github.com/upstash/context7/blob/master/plugins/claude/context7/skills/documentation-lookup/SKILL.md
bunx --bun skills add upstash/context7 -y -g -s documentation-lookup

# doc-coauthoring
# Structured workflow for guiding users through collaborative document creation.
# https://github.com/anthropics/skills/blob/main/skills/doc-coauthoring/SKILL.md
bunx --bun skills add anthropics/skills -y -g -s doc-coauthoring

# find-bugs
# Find bugs on current git branch.
# https://github.com/getsentry/skills/blob/main/plugins/sentry-skills/skills/find-bugs/SKILL.md
bunx --bun skills add getsentry/skills -y -g -s find-bugs

# frontend-design
# Create distinctive, production-grade frontend interfaces with high design quality.
# https://claude.com/blog/improving-frontend-design-through-skills
# https://jsonobject.com/how-a-400-token-plugin-transformed-claude-code-into-a-frontend-design-powerhouse
# https://github.com/anthropics/claude-cookbooks/blob/main/coding/prompting_for_frontend_aesthetics.ipynb
# https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md
# Prompts:
# Build a landing page for an AI security startup
# Design a settings panel with dark mode
bunx --bun skills add anthropics/skills -y -g -s frontend-design

# gh-fix-ci
# Fix CI failures on GitHub PRs.
# https://github.com/openai/skills/blob/main/skills/.curated/gh-fix-ci/SKILL.md
bunx --bun skills add openai/skills -y -g -s gh-fix-ci

# repomix-explorer
# Explore and analyze code repositories.
# https://github.com/yamadashy/repomix/blob/main/.claude/skills/repomix-explorer/SKILL.md
# https://repomix.com/guide/repomix-explorer-skill
# Prompts:
# Find all authentication-related code in this repository.
# What's the structure of this repo?
# Analyze the repository and provide an overview of its structure, key components, and any potential areas for improvement.
# I want to implement a similar feature to what I did in my other project. ~/projects/my-other-app
bunx --bun skills add yamadashy/repomix -y -g -s repomix-explorer

# resend: react-email
# Build and send HTML emails using React components.
# https://github.com/resend/react-email/blob/canary/skills/SKILL.md
bunx --bun skills add resend/react-email -y -g -s react-email

# skill-creator
# Create new agent skills from templates.
# https://github.com/anthropics/skills/blob/main/skills/skill-creator/SKILL.md
bunx --bun skills add anthropics/skills -y -g -s skill-creator

# stitch: design-md, react:components
# https://github.com/google-labs-code/stitch-skills/blob/main/skills/design-md
# https://github.com/google-labs-code/stitch-skills/blob/main/skills/react-components
bunx --bun skills add google-labs-code/stitch-skills -y -g -s design-md -s react:components

# vercel-react-best-practices
# Comprehensive performance optimization guide for React and Next.js applications.
# https://github.com/vercel-labs/agent-skills/blob/main/skills/react-best-practices/SKILL.md
# Prompt: Assess this repo against React best practices. Make a prioritized list of quick wins and top fixes.
bunx --bun skills add vercel-labs/agent-skills -y -g -s vercel-react-best-practices

# web-design-guidelines
# Review UI code for Web Interface Guidelines compliance.
# https://github.com/vercel-labs/agent-skills/blob/main/skills/web-design-guidelines/SKILL.md
bunx --bun skills add vercel-labs/agent-skills -y -g -s web-design-guidelines
```
