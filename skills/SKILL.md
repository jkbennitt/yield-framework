# Yield Framework Skill

## Description
The Yield framework helps build software that compounds. It synthesizes the Bitter Lesson (general methods leveraging computation beat hand-crafted cleverness) with first principles thinking (identify what scales, then get out of its way).

## When to Activate
Activate Yield thinking when:
- Designing new systems or architecture
- Making build vs. configure decisions
- Reviewing code for quality
- Discussing technical debt or refactoring
- Choosing between "clever" and "simple" solutions
- Planning iteration/feedback loops
- Evaluating what to build vs. skip

## The Five Principles

1. **Identify the compounding asset**: What gets better with more compute, data, or iteration? Invest there. Everything else is technical debt in disguise.

2. **Minimize embedded cleverness**: Hand-crafted heuristics, domain-specific optimizations, and "smart" shortcuts encode assumptions that rot. Build systems that learn or that are trivially replaceable.

3. **Build what builds**: Tooling, pipelines, and iteration loops produce value. Artifacts just consume it. Invest in leverage, not solutions.

4. **Optimize for iteration speed, not plan quality**: Search beats planning. The fastest path to a good system is rapid feedback, not upfront design. Reduce cycle time ruthlessly.

5. **Defer decisions to systems that scale**: When choosing between encoding human judgment vs. letting a general system figure it out, bias heavily toward the latter. Your judgment is a snapshot. The system keeps learning.

## Cleverness Debt Patterns
Flag when you see:
- Magic numbers and hardcoded thresholds
- Domain-specific heuristics in business logic
- Deeply nested conditionals (high cyclomatic complexity)
- Configuration buried in code
- Repeated patterns that should be abstracted
- Clever algorithms where simple + scalable would work
- Hardcoded assumptions about environment, scale, or domain

## How to Apply
When giving advice, bias toward:
- Configuration over code
- General over specific
- Learned over hand-crafted
- Simple over clever
- Fast iteration over perfect planning
- Leverage over artifact

## Output Style
When applying Yield thinking:
- Be direct about what compounds and what doesn't
- Name specific anti-patterns when you see them
- Suggest the simpler, more general alternative
- Don't be preachy—one observation, one suggestion
- Use "⚡ Yield:" prefix for inline observations
