# AI Orchestration Platforms

## Claude Code Agent Teams

- https://code.claude.com/docs/en/agent-teams
- https://gist.github.com/kieranklaassen/d2b35569be2c7f1412c64861a219d51f
- Anthropic keeps ripping off Claude Flow
  - https://gist.github.com/kieranklaassen/d2b35569be2c7f1412c64861a219d51f?permalink_comment_id=5954418#gistcomment-5954418

### Prompts

```
Create an agent team to refactor the payment module. Spawn three teammates:
one for the API layer, one for the database migrations, one for test coverage.
Have them coordinate through the shared task list.
```

OR

```
Create an agent team to review our authentication system. Spawn three teammates:
- Security reviewer: audit for vulnerabilities, check token handling
- Performance analyst: profile response times, identify bottlenecks
- Test coverage checker: verify edge cases, find untested paths
Have them share findings and coordinate through the task list.
```

When work is done, shut down teammates and clean up:

```
Ask all teammates to shut down, then clean up the team.
```

https://claudefa.st/blog/guide/agents/agent-teams

### Comparison

- https://github.com/ShawhinT/subagents-vs-teams
- https://github.com/kar-ganap/ate-series

### GUI

- https://github.com/human-corey/AntAI

### Plugins

- https://github.com/zircote/claude-team-orchestration

### Skills

- https://github.com/alinaqi/claude-bootstrap/blob/main/skills/agent-teams/SKILL.md
- https://github.com/modu-ai/cc-plugins/blob/main/.claude/skills/moai/moai-workflow-team/SKILL.md
- https://github.com/CaptainCrouton89/crouton-kit/blob/main/plugins/.claude/skills/agent-team/SKILL.md
- https://github.com/lgbarn/shipyard/blob/main/skills/parallel-dispatch/SKILL.md
- https://github.com/darkroomengineering/cc-settings/blob/main/skills/teams/SKILL.md
- https://lobehub.com/skills?q=CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS

## RuFlo (Claude Flow)

- https://github.com/ruvnet/ruflo
- https://www.reddit.com/r/aipromptprogramming/comments/1rgmrz3/so_long_claude_flow_hello_ruflo_v350_is_out_of/?tl=cs

## oh-my-claudecode

- https://github.com/yeachan-heo/oh-my-claudecode
