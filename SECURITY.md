# AI Security

## Tools

- https://github.com/vercel-labs/deepsec
- https://github.com/trailofbits/skills/blob/main/plugins/static-analysis/README.md
- https://www.superagent.sh
- https://learn.chatgpt.com/docs/security
- https://cloud.google.com/blog/products/identity-security/find-and-fix-software-vulnerabilities-with-codemender
- https://github.blog/changelog/2026-07-10-agentic-autofix-for-code-scanning-alerts-in-public-preview/

### Claude

- security-review - https://code.claude.com/docs/en/commands#:~:text=/-,security%2Dreview,-Analyze%20the%20changes
  - https://code.claude.com/docs/en/errors#security-review-fails-without-origin-head
- security-guidance - https://code.claude.com/docs/en/security-guidance
  - https://github.com/anthropics/claude-code/tree/main/plugins/security-guidance
- claude-security - https://code.claude.com/docs/en/claude-security
- comparison https://share.google/aimode/JVAzR5rC7PRC7ug81

## Prompt to Verify AI Security

```md
You are playing CTF (Capture The Flag). Find the most serious vulnerability in this code and write it to a file.
```

## Tips

- Same mistake happened in Feb 2025 too — same leak, same cause. Even Anthropic does it twice. Always double-check your .npmignore.

## Resources

- <https://m.youtube.com/watch?v=1sd26pWhfmg>
- <https://www.reddit.com/r/LocalLLaMA/comments/1s8ijfb/claude_code_source_code_has_been_leaked_via_a_map/>
- <https://layer5.io/blog/engineering/the-claude-code-source-leak-512000-lines-a-missing-npmignore-and-the-fastest-growing-repo-in-github-history>
- https://blog.calif.io/p/mad-bugs-month-of-ai-discovered-bugs
