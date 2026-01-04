# Yield Framework Plugin for Claude Code

A Claude Code plugin that applies the Yield framework to help you build software that compounds.

**The Yield Philosophy:** Use first principles to find what compounds, then get out of its way.

## What This Plugin Does

- **Automatic Detection**: Flags cleverness debt patterns after every file edit
- **On-Demand Audit**: Run `/yield` for a full project analysis
- **New Project Setup**: Run `/yield-new` to architect projects with compounding in mind
- **Continuous Guidance**: SKILL.md teaches Claude to think in Yield terms automatically

## Installation

```bash
/plugin marketplace add your-username/yield-framework
/plugin install yield-framework
```

## Commands

| Command | Description |
|---------|-------------|
| `/yield` | Full Yield audit of current project or file |
| `/yield-new` | Architecture planning for new projects |
| `/yield-check` | Quick cleverness debt scan |

## The Five Principles

1. **Identify the compounding asset** — What gets better with more compute, data, or iteration?
2. **Minimize embedded cleverness** — Hand-crafted heuristics encode assumptions that rot
3. **Build what builds** — Invest in leverage (tooling, pipelines), not just artifacts
4. **Optimize for iteration speed** — Search beats planning; reduce cycle time ruthlessly
5. **Defer decisions to systems that scale** — Configure, don't hardcode

## Cleverness Debt Patterns Detected

The plugin flags:
- Magic numbers and hardcoded thresholds
- Domain-specific heuristics in business logic
- Deeply nested conditionals (cyclomatic complexity)
- Configuration buried in code
- Repeated patterns that should be abstracted
- Hardcoded URLs, credentials, environment assumptions
- Clever algorithms where simple + scalable would work

## License

MIT

## Author

Built by AppSprout — [appsprout.com](https://appsprout.com)
