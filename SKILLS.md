# 🧩 Agent Skills

[Agent skills](https://agentskills.io) extend AI capabilities with specialized knowledge, workflows, or tool integrations.

## 📚 Skill Repositories

- 🎓 [skills.sh](https://skills.sh)
- 📖 [skillsdirectory.com](https://www.skillsdirectory.com)
- 🏛️ [Anthropics Skills](https://github.com/anthropics/skills#readme)

## Best Practices

- https://github.com/mrgoonie/claudekit-skills/blob/main/REFACTOR.md

## ⚙️ Installing Skills

- Used with `npx skills add <repo> -y -g -s <skill-name>`.
- Tool [add-skill](https://github.com/vercel-labs/add-skill) installs the skill globally (-g) for all agents.

```sh
# find-skills - must be first to avoid the question of installing it
# Search for skills in skill repositories.
# https://github.com/vercel-labs/skills/blob/main/skills/find-skills/SKILL.md
npx skills add vercel-labs/skills -y -g -s find-skills

# agent-browser
# Headless browser automation CLI tool for AI agents.
# https://github.com/vercel-labs/agent-browser#readme
# https://github.com/vercel-labs/agent-browser/blob/main/skills/agent-browser/SKILL.md
# Prompt: Dark mode is broken, test it on http://localhost:3000 and fix it.
# npm install -g agent-browser
# agent-browser install
# agent-browser install --with-deps # on Linux, install system dependencies
npx skills add vercel-labs/agent-browser -y -g -s agent-browser

# ai-sdk
# Vercel AI SDK integration skill.
# https://github.com/vercel/ai/blob/main/skills/use-ai-sdk/SKILL.md
npx skills add vercel/ai -y -g -s ai-sdk

# better-auth: better-auth-best-practices, create-auth-skill
# Better Auth integration guides.
# https://github.com/better-auth/skills/blob/main/better-auth/best-practices/SKILL.md
# https://github.com/better-auth/skills/blob/main/better-auth/create-auth/SKILL.md
npx skills add better-auth/skills -y -g -s better-auth-best-practices -s create-auth-skill

# claude-opus-4-5-migration
# Migrate prompts and code to Opus 4.5.
# https://github.com/anthropics/claude-code/blob/main/plugins/claude-opus-4-5-migration/skills/claude-opus-4-5-migration/SKILL.md
npx skills add anthropics/claude-code -y -g -s claude-opus-4-5-migration

# context7: documentation-lookup
# Fallback for local docs skills from Repomix.
# Local docs skills does not cover all libraries.
# https://github.com/upstash/context7/tree/master/plugins/claude/context7
# https://github.com/upstash/context7/blob/master/plugins/claude/context7/skills/documentation-lookup/SKILL.md
npx skills add upstash/context7 -y -g -s documentation-lookup

# doc-coauthoring
# Structured workflow for guiding users through collaborative document creation.
# https://github.com/anthropics/skills/blob/main/skills/doc-coauthoring/SKILL.md
npx skills add anthropics/skills -y -g -s doc-coauthoring

# find-bugs
# Find bugs on current git branch.
# https://github.com/getsentry/skills/blob/main/plugins/sentry-skills/skills/find-bugs/SKILL.md
npx skills add getsentry/skills -y -g -s find-bugs

# frontend-design
# Create distinctive, production-grade frontend interfaces with high design quality.
# https://claude.com/blog/improving-frontend-design-through-skills
# https://jsonobject.com/how-a-400-token-plugin-transformed-claude-code-into-a-frontend-design-powerhouse
# https://github.com/anthropics/claude-cookbooks/blob/main/coding/prompting_for_frontend_aesthetics.ipynb
# https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md
# Prompts:
# Build a landing page for an AI security startup
# Design a settings panel with dark mode
npx skills add anthropics/skills -y -g -s frontend-design

# gh-fix-ci
# Fix CI failures on GitHub PRs.
# https://github.com/openai/skills/blob/main/skills/.curated/gh-fix-ci/SKILL.md
npx skills add openai/skills -y -g -s gh-fix-ci

# knowledge-saver
# Save knowledge from agent sessions.
# https://github.com/JosefJezek/knowledge-saver/blob/main/SKILL.md
npx skills add JosefJezek/knowledge-saver -y -g -s knowledge-saver

# octocode-research, octocode-documentaion-writer
# Research codebases using OctoCode MCP. Generate documentation from code.
# https://medium.com/@guybary/octocode-research-skill-b8248214b515
# https://www.linkedin.com/posts/bgauryy_octocode-vs-deepwiki-by-cognition-ai-research-activity-7384197129247993856-7lrU/
# https://github.com/bgauryy/octocode-mcp/tree/main/skills/octocode-research
# https://github.com/bgauryy/octocode-mcp/blob/main/skills/octocode-research/SKILL.md
# https://github.com/bgauryy/octocode-mcp/tree/main/skills/octocode-documentaion-writer
# https://github.com/bgauryy/octocode-mcp/blob/main/skills/octocode-documentaion-writer/SKILL.md
npx skills add bgauryy/octocode-mcp -y -g -s octocode-research -s octocode-documentaion-writer

# repomix-explorer
# Explore and analyze code repositories.
# https://github.com/yamadashy/repomix/blob/main/.claude/skills/repomix-explorer/SKILL.md
# https://repomix.com/guide/repomix-explorer-skill
# Prompts:
# Find all authentication-related code in this repository.
# What's the structure of this repo?
# Analyze the repository and provide an overview of its structure, key components, and any potential areas for improvement.
# I want to implement a similar feature to what I did in my other project. ~/projects/my-other-app
npx skills add yamadashy/repomix -y -g -s repomix-explorer

# resend: react-email
# Build and send HTML emails using React components.
# https://github.com/resend/react-email/blob/canary/skills/SKILL.md
npx skills add resend/react-email -y -g -s react-email

# skill-creator
# Create new agent skills from templates.
# https://github.com/anthropics/skills/blob/main/skills/skill-creator/SKILL.md
npx skills add anthropics/skills -y -g -s skill-creator

# stitch: design-md, react:components
# https://github.com/google-labs-code/stitch-skills/blob/main/skills/design-md
# https://github.com/google-labs-code/stitch-skills/blob/main/skills/design-md/SKILL.md
# https://github.com/google-labs-code/stitch-skills/blob/main/skills/react-components
# https://github.com/google-labs-code/stitch-skills/blob/main/skills/react-components/SKILL.md
npx skills add google-labs-code/stitch-skills -y -g -s design-md -s react:components

# vercel-react-best-practices
# Comprehensive performance optimization guide for React and Next.js applications.
# https://github.com/vercel-labs/agent-skills/blob/main/skills/react-best-practices/SKILL.md
# Prompt: Assess this repo against React best practices. Make a prioritized list of quick wins and top fixes.
npx skills add vercel-labs/agent-skills -y -g -s vercel-react-best-practices

# vite, vitest
# https://github.com/antfu/skills/blob/main/skills/vite/SKILL.md
# https://github.com/antfu/skills/blob/main/skills/vitest/SKILL.md
npx skills add antfu/skills -y -g -s vite -s vitest

# web-design-guidelines
# Review UI code for Web Interface Guidelines compliance.
# https://github.com/vercel-labs/agent-skills/blob/main/skills/web-design-guidelines/SKILL.md
npx skills add vercel-labs/agent-skills -y -g -s web-design-guidelines
```

### 📚 Docs as Agent Skills

[Repomix](https://github.com/yamadashy/repomix#readme) can convert documentation into agent skills for enhanced AI interaction.

- Used with `npx repomix --remote <repo> --include <path> --skill-generate <skill-name> --skill-output <output-path> --force`.
- Force regeneration with `--force` to update existing skills.

```sh
# AI SDK Docs
# https://github.com/vercel/ai/tree/main/content
npx repomix --remote vercel/ai --include content --skill-generate docs-ai-sdk --skill-output /tmp/skills/docs-ai-sdk --force
sed -i -e 's/Ai/AI SDK/g' /tmp/skills/docs-ai-sdk/SKILL.md
npx skills add /tmp/skills/docs-ai-sdk -y -g

# Alibaba Hooks Docs
# https://github.com/alibaba/hooks/tree/master/docs
npx repomix --remote alibaba/hooks --include docs --skill-generate docs-ahooks --skill-output /tmp/skills/docs-ahooks --force
sed -i -e 's/Hooks/ahooks/g' /tmp/skills/docs-ahooks/SKILL.md
npx skills add /tmp/skills/docs-ahooks -y -g

# Base UI Docs
# https://github.com/mui/base-ui/tree/master/docs
npx repomix --remote mui/base-ui --include docs --skill-generate docs-base-ui --skill-output /tmp/skills/docs-base-ui --force
npx skills add /tmp/skills/docs-base-ui -y -g

# Better Auth Docs
# https://github.com/better-auth/better-auth/tree/canary/docs
npx repomix --remote better-auth/better-auth --include docs --skill-generate docs-better-auth --skill-output /tmp/skills/docs-better-auth --force
npx skills add /tmp/skills/docs-better-auth -y -g

# Claude Code Action Docs
# https://github.com/anthropics/claude-code-action/tree/main/docs
npx repomix --remote anthropics/claude-code-action --include docs --skill-generate docs-claude-code-action --skill-output /tmp/skills/docs-claude-code-action --force
npx skills add /tmp/skills/docs-claude-code-action -y -g

# Cloudflare Docs
# https://github.com/cloudflare/cloudflare-docs/tree/production/src/content/docs
npx repomix --remote cloudflare/cloudflare-docs --include src/content/docs --skill-generate docs-cloudflare --skill-output /tmp/skills/docs-cloudflare --force
npx skills add /tmp/skills/docs-cloudflare -y -g

# Drizzle ORM Docs
# https://github.com/drizzle-team/drizzle-orm-docs/tree/main/src/content/docs
npx repomix --remote drizzle-team/drizzle-orm-docs --include src/content/docs --skill-generate docs-drizzle-orm --skill-output /tmp/skills/docs-drizzle-orm --force
npx skills add /tmp/skills/docs-drizzle-orm -y -g

# Motion React Examples
# https://github.com/motiondivision/motion/tree/main/dev/react/src/examples
npx repomix --remote motiondivision/motion --include dev/react/src/examples --skill-generate docs-motion-react-examples --skill-output /tmp/skills/docs-motion-react-examples --force
npx skills add /tmp/skills/docs-motion-react-examples -y -g

# React Docs
# https://github.com/reactjs/react.dev/tree/main/src/content
npx repomix --remote reactjs/react.dev --include src/content --skill-generate docs-react --skill-output /tmp/skills/docs-react --force
sed -i -e 's/React.Dev/React/g' /tmp/skills/docs-react/SKILL.md
npx skills add /tmp/skills/docs-react -y -g

# React Error Boundary Docs
# https://github.com/bvaughn/react-error-boundary/tree/main/public/generated
npx repomix --remote bvaughn/react-error-boundary --include public/generated --skill-generate docs-react-error-boundary --skill-output /tmp/skills/docs-react-error-boundary --force
npx skills add /tmp/skills/docs-react-error-boundary -y -g

# React Testing Library Docs
# https://github.com/testing-library/testing-library-docs/tree/main/docs/react-testing-library
npx repomix --remote testing-library/testing-library-docs --include docs/react-testing-library --skill-generate docs-react-testing-library --skill-output /tmp/skills/docs-react-testing-library --force
npx skills add /tmp/skills/docs-react-testing-library -y -g

# Rooks Docs
# https://github.com/imbhargav5/rooks/tree/main/apps/website/content/docs
npx repomix --remote imbhargav5/rooks --include apps/website/content/docs --skill-generate docs-rooks --skill-output /tmp/skills/docs-rooks --force
npx skills add /tmp/skills/docs-rooks -y -g

# Shadcn UI Docs
# https://github.com/shadcn-ui/ui/tree/main/apps/v4/content/docs
npx repomix --remote shadcn-ui/ui --include apps/v4/content/docs --skill-generate docs-shadcn-ui --skill-output /tmp/skills/docs-shadcn-ui --force
sed -i -e 's/Ui/Shadcn UI/g' /tmp/skills/docs-shadcn-ui/SKILL.md
npx skills add /tmp/skills/docs-shadcn-ui -y -g

# Storybook Docs
# https://github.com/storybookjs/storybook/tree/next/docs
npx repomix --remote storybookjs/storybook --include docs --skill-generate docs-storybook --skill-output /tmp/skills/docs-storybook --force
npx skills add /tmp/skills/docs-storybook -y -g

# Tailwind CSS Docs
# https://github.com/tailwindlabs/tailwindcss.com/tree/main/src/docs
npx repomix --remote tailwindlabs/tailwindcss.com --include src/docs --skill-generate docs-tailwind-css --skill-output /tmp/skills/docs-tailwind-css --force
sed -i -e 's/Tailwindcss.Com/Tailwind CSS/g' /tmp/skills/docs-tailwind-css/SKILL.md
npx skills add /tmp/skills/docs-tailwind-css -y -g

# Tailwind Variants Docs
# https://github.com/heroui-inc/tailwind-variants-docs/tree/main/pages/docs
npx repomix --remote heroui-inc/tailwind-variants-docs --include pages/docs --skill-generate docs-tailwind-variants --skill-output /tmp/skills/docs-tailwind-variants --force
npx skills add /tmp/skills/docs-tailwind-variants -y -g

# TanStack DB Docs
# https://github.com/TanStack/db/tree/main/docs
npx repomix --remote TanStack/db --include docs --skill-generate docs-tanstack-db --skill-output /tmp/skills/docs-tanstack-db --force
sed -i -e 's/Db/TanStack DB/g' /tmp/skills/docs-tanstack-db/SKILL.md
npx skills add /tmp/skills/docs-tanstack-db -y -g

# TanStack Form Docs
# https://github.com/TanStack/form/tree/main/docs
npx repomix --remote TanStack/form --include docs --skill-generate docs-tanstack-form --skill-output /tmp/skills/docs-tanstack-form --force
sed -i -e 's/Form/TanStack Form/g' /tmp/skills/docs-tanstack-form/SKILL.md
npx skills add /tmp/skills/docs-tanstack-form -y -g

# TanStack Pacer Docs
# https://github.com/TanStack/pacer/tree/main/docs
npx repomix --remote TanStack/pacer --include docs --skill-generate docs-tanstack-pacer --skill-output /tmp/skills/docs-tanstack-pacer --force
sed -i -e 's/Pacer/TanStack Pacer/g' /tmp/skills/docs-tanstack-pacer/SKILL.md
npx skills add /tmp/skills/docs-tanstack-pacer -y -g

# TanStack Query Docs
# https://github.com/TanStack/query/tree/main/docs
npx repomix --remote TanStack/query --include docs --skill-generate docs-tanstack-query --skill-output /tmp/skills/docs-tanstack-query --force
sed -i -e 's/Query/TanStack Query/g' /tmp/skills/docs-tanstack-query/SKILL.md
npx skills add /tmp/skills/docs-tanstack-query -y -g

# TanStack Ranger Docs
# https://github.com/TanStack/ranger/tree/main/docs
npx repomix --remote TanStack/ranger --include docs --skill-generate docs-tanstack-ranger --skill-output /tmp/skills/docs-tanstack-ranger --force
sed -i -e 's/Ranger/TanStack Ranger/g' /tmp/skills/docs-tanstack-ranger/SKILL.md
npx skills add /tmp/skills/docs-tanstack-ranger -y -g

# TanStack Router Docs
# https://github.com/TanStack/router/tree/main/docs/router
npx repomix --remote TanStack/router --include docs/router --skill-generate docs-tanstack-router --skill-output /tmp/skills/docs-tanstack-router --force
sed -i -e 's/Router/TanStack Router/g' /tmp/skills/docs-tanstack-router/SKILL.md
npx skills add /tmp/skills/docs-tanstack-router -y -g

# TanStack Start Docs
# https://github.com/TanStack/router/tree/main/docs/start
npx repomix --remote TanStack/router --include docs/start --skill-generate docs-tanstack-start --skill-output /tmp/skills/docs-tanstack-start --force
sed -i -e 's/Router/TanStack Start/g' /tmp/skills/docs-tanstack-start/SKILL.md
npx skills add /tmp/skills/docs-tanstack-start -y -g

# TanStack Table Docs
# https://github.com/TanStack/table/tree/main/docs
npx repomix --remote TanStack/table --include docs --skill-generate docs-tanstack-table --skill-output /tmp/skills/docs-tanstack-table --force
sed -i -e 's/Table/TanStack Table/g' /tmp/skills/docs-tanstack-table/SKILL.md
npx skills add /tmp/skills/docs-tanstack-table -y -g

# TanStack Virtual Docs
# https://github.com/TanStack/virtual/tree/main/docs
npx repomix --remote TanStack/virtual --include docs --skill-generate docs-tanstack-virtual --skill-output /tmp/skills/docs-tanstack-virtual --force
sed -i -e 's/Virtual/TanStack Virtual/g' /tmp/skills/docs-tanstack-virtual/SKILL.md
npx skills add /tmp/skills/docs-tanstack-virtual -y -g

# TW Animate CSS Docs
# https://github.com/Wombosvideo/tw-animate-css/tree/main/docs
npx repomix --remote Wombosvideo/tw-animate-css --include docs --skill-generate docs-tw-animate-css --skill-output /tmp/skills/docs-tw-animate-css --force
npx skills add /tmp/skills/docs-tw-animate-css -y -g

# TypeScript Docs
# https://github.com/microsoft/TypeScript-Website/tree/v2/packages/documentation/copy/en
npx repomix --remote microsoft/TypeScript-Website --include packages/documentation/copy/en --skill-generate docs-typescript --skill-output /tmp/skills/docs-typescript --force
sed -i -e 's/TypeScript Website/TypeScript/g' /tmp/skills/docs-typescript/SKILL.md
npx skills add /tmp/skills/docs-typescript -y -g

# Vite Docs
# https://github.com/vitejs/vite/tree/main/docs
npx repomix --remote vitejs/vite --include docs --skill-generate docs-vite --skill-output /tmp/skills/docs-vite --force
npx skills add /tmp/skills/docs-vite -y -g

# Vitest Docs
# https://github.com/vitest-dev/vitest/tree/main/docs
npx repomix --remote vitest-dev/vitest --include docs --skill-generate docs-vitest --skill-output /tmp/skills/docs-vitest --force
npx skills add /tmp/skills/docs-vitest -y -g

# Zod Docs
# https://github.com/colinhacks/zod/tree/main/packages/docs
npx repomix --remote colinhacks/zod --include packages/docs --skill-generate docs-zod --skill-output /tmp/skills/docs-zod --force
npx skills add /tmp/skills/docs-zod -y -g

# Zustand Docs
# https://github.com/pmndrs/zustand/tree/main/docs
npx repomix --remote pmndrs/zustand --include docs --skill-generate docs-zustand --skill-output /tmp/skills/docs-zustand --force
npx skills add /tmp/skills/docs-zustand -y -g
```
