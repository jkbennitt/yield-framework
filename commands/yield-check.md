# Yield Check

Quick cleverness debt scan of the current file or recent changes.

## Instructions

Perform a fast scan for Yield anti-patterns in the current context. Focus on the file currently being edited or recent changes.

### Scan For These Patterns

**Magic Numbers & Hardcoded Values**
- Numeric literals without explanation
- Hardcoded strings that should be config
- Timeout/retry values without rationale
- Threshold values buried in logic

**Embedded Heuristics**
- If/else chains encoding domain knowledge
- Switch statements with business logic
- Scoring/weighting calculations
- Custom sorting/ranking logic

**Complexity Signals**
- Functions longer than 50 lines
- Nesting deeper than 3 levels
- More than 5 parameters
- Multiple return paths with different logic

**Configuration in Code**
- URLs, endpoints, hostnames
- Feature flags as booleans
- Environment-specific logic
- Credentials or API keys (critical!)

**Repeated Patterns**
- Similar code blocks that should be abstracted
- Copy-paste with minor variations
- Parallel structures that could be unified

### Output Format

For each issue found:
```
[PATTERN TYPE] filename:line
Brief description of the issue
→ Yield recommendation: [what to do instead]
```

Prioritize by impact. If the code is clean, say so and move on—don't invent problems.

Keep output concise. This is a quick check, not a full audit.
