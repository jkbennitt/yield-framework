# Yield New Project

Help architect a new project using Yield framework principles to maximize compounding from day one.

## Instructions

Guide the user through setting up a new project with the Yield framework. Ask them to describe their project, then help them think through:

### 1. What Compounds Here?
Given this domain, what aspects of the system will get better with more compute, data, or iteration? These are the core investments.

Examples to probe:
- Data that improves predictions over time
- User behavior that trains recommendations
- Content that builds SEO/discovery
- Tooling that accelerates future development

### 2. What's the Substrate?
What tooling, pipelines, or infrastructure will produce the most leverage? What should be built that builds other things?

Help them identify:
- CI/CD and deployment automation
- Testing infrastructure
- Data pipelines
- Developer experience tooling
- Abstraction layers that will be used repeatedly

### 3. Cleverness Traps
Identify the likely traps—places they'll be tempted to hand-craft heuristics or encode domain knowledge that will rot.

Common traps:
- Custom scoring/ranking algorithms
- Hardcoded business rules
- Domain-specific optimizations
- "Smart" caching strategies
- Hand-tuned thresholds

### 4. Minimum Viable Iteration Loop
What's the fastest possible feedback cycle they can establish on day one? What would make iteration 10x faster than the obvious approach?

Consider:
- Hot reload / instant preview
- Automated testing on save
- Feature flags for instant rollback
- Synthetic data for development
- Local-first architecture

### 5. Deferred Decisions
What choices can be pushed to runtime, configuration, or learned systems instead of hardcoding now?

Examples:
- Thresholds and weights → config files
- Feature toggles → feature flag service
- Business rules → rules engine
- Recommendations → ML model
- Copy/content → CMS

### 6. What NOT to Build
What's the smallest possible artifact that still validates whether the compounding asset works?

Help them ruthlessly cut:
- Admin dashboards (use existing tools)
- Custom auth (use a service)
- Analytics (use off-the-shelf)
- Features that don't test the core hypothesis

## Output Format

Provide a concrete starting architecture that:
1. Names the compounding asset explicitly
2. Lists the substrate to build first
3. Flags cleverness traps to avoid
4. Defines the iteration loop
5. Lists decisions to defer
6. Defines the MVP scope

Be opinionated. Push back on complexity.
