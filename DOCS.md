# Documentation First Approach

## Generating Documentation with Octocode

I use the Documentation Writer Skill from Octocode to generate and maintain up-to-date documentation for my codebases.
This helps ensure that both human developers and AI models have a clear understanding of the code structure and functionality.

For more information, see the [Documentation Writer Skill](RDD.md#documentation-writer-skill).

```sh
/octocode-documentation-writer
```

## Creating Codebase Reference Skill with Repomix

I use Repomix to generate a comprehensive codebase reference skill for better navigation and understanding of the project structure.

For more information, see the [Skill Generator](RDD.md#skill-generator).

```sh
npx repomix src/ --skill-generate repomix-codebase-reference-src
```

## Creating Codebase Reference in one file with Repomix

I use Repomix to create a single-file representation of the entire codebase for easy analysis and exploration by AI models.

For more information, see the [Explorer Skill](RDD.md#explorer-skill).

```sh
npx repomix@latest
```

> This file contains all the files in the repository combined into one.
> I want to refactor the code, so please review it first.
