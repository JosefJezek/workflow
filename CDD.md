# Context-Driven Development (CDD)

> "Understanding the context is key to effective AI-assisted development."

Context-Driven Development (CDD) focuses on providing AI models with relevant context from the codebase to improve their understanding and output quality.

This approach helps AI models generate more accurate and context-aware code suggestions, reducing errors and improving overall code quality.

The context-driven development leads to higher quality outcomes for complex projects.
By treating your documentation as the source of truth, you empower Agent to act as a true extension of your engineering team.

It unlocks context-driven development by shifting the context of your project out of the chat window and directly into your codebase. By treating context as a managed artifact alongside your code, you transform your repository into a single source of truth that drives every agent interaction with deep, persistent project awareness.

- https://developers.googleblog.com/conductor-introducing-context-driven-development-for-gemini-cli/

## Fatures

- Memory system to retain context across sessions
- Context extraction from code, documentation, and other project artifacts
- Integration with version control systems to track context changes
- File based context management for precise control and versioning

## Passive Context Loading

- https://vercel.com/blog/agents-md-outperforms-skills-in-our-agent-evals
- https://github.com/vercel/next.js/pull/88961

## CDD vs SDD

### Context-Driven Development (CDD)
- **Focus:** Understanding existing codebase through context
- **Direction:** Reactive - analyzes what already exists
- **Source of Truth:** Repository (code + docs + artifacts)
- **AI Role:** Extract and understand context to provide better suggestions
- **Use Case:** Working with existing code, refactoring, bug fixes
- **Question:** "What is the current state?"

### Spec-Driven Development (SDD)
- **Focus:** Defining specifications before writing code
- **Direction:** Proactive - defines what should be built
- **Source of Truth:** Specifications (may vary by tool)
- **AI Role:** Build code that matches specifications
- **Use Case:** New features, greenfield projects, requirements-driven development
- **Question:** "What should be built?"

### Key Differences

| Aspect | CDD | SDD |
|--------|-----|-----|
| **Starting Point** | Existing codebase | Specifications |
| **Process** | Context → Understanding → Code | Specs → Code → Validation |
| **Context Load** | High (entire codebase context) | Low to Medium (relevant specs) |
| **Best For** | Legacy code, brownfield | Greenfield, new features |
| **Memory** | Session-based, extracted | Versioned, explicit |
| **AI Input** | "Here's the code, understand it" | "Here's what to build" |

### Complementary Approaches

CDD and SDD work best together:

1. **For New Features:**
   - Use **SDD** to define specifications
   - Use **CDD** to understand existing architecture context
   - Result: New code that matches specs AND fits existing patterns

2. **For Refactoring:**
   - Use **CDD** to understand current implementation
   - Use **SDD** (delta specs) to define desired changes
   - Result: Targeted refactoring with full context awareness

3. **For Team Development:**
   - Use **SDD** for consistent requirements and standards
   - Use **CDD** for shared understanding of codebase
   - Result: Team alignment on both "what to build" and "how it works"

**Example Workflow:**
```
1. CDD: Load context about existing authentication system
2. SDD: Write spec for new OAuth2 integration
3. CDD: Understand current auth patterns and conventions
4. Build: AI implements OAuth2 using specs + context
5. SDD: Update spec with implementation details
6. CDD: Context now includes OAuth2 for future features
```

## Tools

- https://github.com/steveyegge/beads
  - https://www.reddit.com/r/vibecoding/comments/1p9tnm3/is_beads_worth_a_try/

### Conductor

- https://github.com/gemini-cli-extensions/conductor
- https://github.com/hlhr202/Conductor-for-all
- https://github.com/rbarcante/claude-conductor
- https://github.com/jnorthrup/conductor2

## Resources

- https://cdd.dev/essay/cdd-manifesto/
