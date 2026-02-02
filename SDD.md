# Spec-Driven Development (SDD)

> "Clear specifications lead to reliable code."

Spec-Driven Development (SDD) is a development methodology that emphasizes creating detailed specifications before writing code. It ensures that the final product meets the defined requirements and behaves as expected.

## Features of SDD

- specifications are the source of truth
- versioned memory for specs
- supports delta specs for updates
- integrates with version control systems
- promotes team consistency through shared standards
- user prompts for spec generation and updates are stored in project memory
- AI agents build code based on specifications
- questions and answers from chat are saved in project memory in md files

## Comparison Overview

| Criteria | OpenSpec | Spec-Kit | BMAD Method | Superpowers | specs.md | SpecSwarm | Conductor |
|----------|----------|----------|-------------|-------------|----------|-----------|-----------|
| **Context Load** | ⭐⭐⭐⭐ Low | ⭐⭐⭐ Medium | ⭐⭐ High | ⭐⭐⭐⭐⭐ Very Low | ⭐⭐⭐ Medium | ⭐⭐⭐ Medium | ⭐⭐⭐ Medium |
| **Spec Updates** | ✅ Excellent | ⚠️ Limited | ✅ Good | ⚠️ Limited | ✅ Good | ✅ Good | ✅ Good |
| **Memory Versioning** | ✅ Git-based | ❌ No | ✅ Yes | ❌ No | ✅ Yes | ✅ Yes | ✅ Git notes |
| **Workflow Speed** | ⭐⭐⭐⭐ Fast | ⭐⭐⭐ Medium | ⭐⭐ Slow | ⭐⭐⭐⭐⭐ Fastest | ⭐⭐⭐ Medium | ⭐⭐⭐⭐ Fast | ⭐⭐⭐ Medium |
| **Team Consistency** | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐⭐⭐ Good | ⭐⭐⭐⭐⭐ Excellent | ⭐⭐⭐ Medium | ⭐⭐⭐⭐ Good | ⭐⭐⭐⭐ Good | ⭐⭐⭐⭐ Good |
| **Source of Truth** | Specs → Code | Spec → Code | Docs + Code | Code + Skills | Memory Bank | Tech Stack + Specs | Conductor/ |

### Key Findings

**Lowest Context Load:** Superpowers - skills loaded on-demand, < 500 lines each

**Best for Spec Updates:** OpenSpec - delta specs + archive merge workflow

**Best Memory Versioning:** specs.md + BMAD - Memory Bank with frontmatter

**Fastest Workflow:** Superpowers > SpecSwarm > OpenSpec

**Best Team Consistency:** OpenSpec + BMAD - Constitution + shared standards

### Recommended by Scenario

| Scenario | Recommended Tool | Reason |
|----------|------------------|--------|
| **Quick Prototypes** | Superpowers | Minimal overhead, skills on-demand |
| **Enterprise Projects** | BMAD Method or specs.md (AI-DLC) | Full traceability, multi-agent |
| **Brownfield Updates** | OpenSpec | Delta specs, merge workflow |
| **Refactoring** | OpenSpec | Delta specs, brownfield-first, archive merge |
| **Team Consistency** | Spec-Kit or SpecSwarm | Constitution, tech stack enforcement |
| **Monorepo** | specs.md (FIRE) | Hierarchical standards |
| **Gemini CLI** | Conductor | Native support |

## Compared SDD Tools

- [OpenSpec](https://github.com/Fission-AI/OpenSpec#readme)
  - https://github.com/Fission-AI/OpenSpec/releases/tag/v1.0.0
- [Spec Kit](https://github.com/github/spec-kit#readme)
- [BMad](https://github.com/bmad-code-org/BMAD-METHOD)
- [specs.md](https://github.com/fabriqaai/specs.md)
- [SpecSwarm](https://github.com/MartyBonacci/specswarm)

## Prompt for comparison

```
Compare OpenSpec vs Gemini Conductor vs spec-kit vs specs.md vs Superpowers vs BMAD vs SpecSwarm:

- Which one puts the least load on the context window?
- Can they update existing specs?
- Do they version memory?
- Which is fastest in the workflow?
- Do they enable teams to be consistent in development?
- Who is the source of truth - code, docs, or repo?
- What is the difference between context-driven development and spec-driven development?
- Read internal guides from repos
- Use context7

repos:
- https://github.com/Fission-AI/OpenSpec
- https://github.com/github/spec-kit
- https://github.com/bmad-code-org/BMAD-METHOD
- https://github.com/obra/superpowers
- https://github.com/fabriqaai/specs.md
- https://github.com/MartyBonacci/specswarm
- https://github.com/gemini-cli-extensions/conductor
```
