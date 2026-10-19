# AI Prompts

- Add a detailed description to the plugin on why it is needed.
- Write the plan as detailed as if you were writing it for a junior programmer, because it will be executed by the local model.
- /loop 10m babysit my open PRs – fix CI, address comments, rebase
- check if the change made any docs stale
- Nightly: find tests that flaked >2x this week, root-cause or delete
- Take a look at my website's homepage and tell me what to improve in terms of CRO.
- I want to write an article about marketing MCP servers. Search the English website and give me at least 20 tips on the best ones.
- Look at Google Search Console data from the last 6 months and identify quick wins – things you can easily optimize for higher impressions and clicks. Create a checklist of tasks sorted by priority.
- No silent fallbacks! - AGENTS.md
- /schedule every day at 5am: answer to "Say only "Hi"." - Claude Code - Limit warmup 5h
-  can you describe and elaborate
-  Summarize the work done in each file with functions.
-  Read the issue body again, check for any gaps or inconsistencies, simplify the description.
-  Add a comment in Czech to the gh issue, one sentence for a layman describing what the bug was.
-  /skill-creator create a skill from this session and save it to the repo, focus on optimizing the number of tokens using skill scripts, SKILL.md under ~160 lines
-  Analyze the feature and UI parity gaps between app v1 and v2 in gh PR 1, close them, then re-run the analysis and create a table of the remaining gaps, one row per gap, with columns for the master behaviour, its status in the PR, whether a new mechanism replaces it, and severity.
-  Use git bisect to find what broke.
-  Analyze the provided code or system and detail: 1) all potential blocking points or sources of latency, 2) how to rigorously test these areas for concurrency and stress, and 3) the best architectural and asynchronous practices to implement them correctly.
-  "Identify all wait states" > "Verify test coverage" > "Validate implementation"

## Commit

```
Create a pre-commit hook that prevents files over 5,000 tokens. Tokens = bytes/4.
Run only on staged files. Ignore files which are not authored by agents, like lockfiles or codegen.
Provide explicit instructions on how to split files in the error message.
```

https://x.com/mattpocockuk/status/2111708560715292675

## Issue

```
## TL;DR

- First thing in the issue body: `## TL;DR` with 1-3 bullets, nothing else in that section.
- ELI10, one sentence per bullet, max 20 words.
- Order: what goes wrong, why it matters, what we do or ask. Skip empty ones, keep the order.
- User's or tester's view, not the code's. Cause goes below.
- Waiting on a decision: last bullet is the question, addressed to the decider by name.
- No backticks, links or context-dependent numbers. One plain size number is fine.
- Write it last, from the finished body.
- Above the template sections, which stay complete. Plain-text body without a heading: add `## Report` above it.
- Issue bodies only, not comments.
- Update it when an edit changes the meaning. No emojis, no attribution.
```

## Loops

- https://www.cerebras.ai/blog/never-loop-without-verifiers
- https://x.com/jasonzhou1993/status/2069002271216787464
- https://x.com/BHolmesDev/status/2072106364298723592
- https://x.com/ClaudeDevs/status/2074208949205881033
- https://x.com/PeyMonee/status/2069864394180452817
- https://x.com/mvanhorn/article/2063865685558903149
- https://www.warp.dev/blog/building-a-skill-optimization-loop
- https://www.warp.dev/blog/agents-need-feedback-loops-not-perfect-prompts
- https://www.warp.dev/blog/self-improvement-loop-for-skills
- https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-13-loop-engineering/
- https://github.com/karpathy/autoresearch

## AGENTS.md

- https://x.com/sinanonur/status/2072617768327774295
