# Yield Audit

Perform a comprehensive Yield framework analysis on the current project or specified files.

## Instructions

Analyze this codebase through the Yield framework lens:

### 1. Compounding Assets Audit
Identify what in this system actually gets better with more compute, data, or iteration. Also note what was *intended* to compound but doesn't, and what accidentally compounds that should be leaned into.

### 2. Cleverness Debt Inventory
Scan for and list:
- Magic numbers and hardcoded thresholds
- Domain-specific heuristics and "smart" shortcuts
- Deeply nested conditionals (cyclomatic complexity > 10)
- Configuration buried in code instead of externalized
- Hand-crafted optimizations that encode assumptions
- Clever algorithms where simple + general would work

For each item found, note: what assumption does it encode, and how might that assumption age?

### 3. Leverage Inventory
Categorize the codebase into three buckets:
- **LEVERAGE**: Tooling, pipelines, abstractions that multiply effort
- **ARTIFACT**: End products that deliver value but don't compound
- **SCAFFOLDING**: Neither leverage nor artifact—should probably be deleted or replaced

### 4. Iteration Friction Analysis
Identify:
- Current feedback cycle time (estimate)
- Top 3 friction points slowing iteration
- Quick wins that would dramatically speed up the loop

### 5. Hardcoded Judgment Scan
Find where human decisions are baked into code that could be:
- Moved to configuration
- Made learned/adaptive
- Replaced with more general solutions

### 6. Scaling Ceiling
If this system got 100x more usage/data/compute, what breaks first? What would we wish we'd built differently?

## Output Format

Provide a prioritized action plan:
- **AMPLIFY**: What's working and should be invested in further
- **DELETE**: What's pure liability and should be removed
- **REPLACE**: What should be swapped for something more general
- **DEFER**: What's fine for now but flagged for future leverage

Be specific. Name files, functions, and line numbers where possible.
