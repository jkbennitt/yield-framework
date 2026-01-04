# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repository Is

This is a **Claude Code plugin** that implements the Yield Framework—a philosophy for building software that compounds by identifying what scales (compute, data, iteration) and minimizing embedded cleverness that rots over time.

The plugin is not executable code but rather a collection of:
- **Commands** (markdown files in `commands/`) that define slash commands
- **Skills** (markdown in `skills/`) that teach Claude to apply Yield thinking
- **Agents** (markdown in `agents/`) that define specialized analysis agents
- **Hooks** (JSON configuration in `hooks/`) that trigger automatic behaviors
- **Plugin metadata** (JSON in `.claude-plugin/`)

## Architecture

### Plugin Structure

```
.claude-plugin/
  plugin.json         # Plugin manifest (name, version, entry points)
  marketplace.json    # Marketplace metadata

commands/
  yield.md           # Full Yield audit command
  yield-new.md       # New project architecture command
  yield-check.md     # Quick cleverness debt scan

skills/
  SKILL.md           # Teaches Claude to think in Yield terms

agents/
  yield-auditor.md   # Specialized agent for deep analysis

hooks/
  hooks.json         # PostToolUse hook for automatic detection
```

### How It Works

1. **Commands are instructions**: Each `.md` file in `commands/` becomes a slash command (e.g., `/yield`). The markdown content is the instruction prompt given to Claude.

2. **Skills modify behavior**: `SKILL.md` teaches Claude the five Yield principles and when to apply them. It activates automatically during architecture discussions.

3. **Hooks trigger automatically**: The `PostToolUse` hook in `hooks.json` runs after every file edit, scanning for cleverness debt patterns.

4. **Agents are specialized personas**: `yield-auditor.md` defines a focused agent personality for deep codebase analysis.

### The Five Yield Principles (Core Framework)

1. **Identify the compounding asset** — What gets better with more compute, data, or iteration?
2. **Minimize embedded cleverness** — Hand-crafted heuristics encode assumptions that rot
3. **Build what builds** — Invest in leverage (tooling, pipelines), not just artifacts
4. **Optimize for iteration speed** — Search beats planning; reduce cycle time ruthlessly
5. **Defer decisions to systems that scale** — Configure, don't hardcode

### Cleverness Debt Patterns (What to Detect)

The plugin scans for:
- Magic numbers and hardcoded thresholds
- Domain-specific heuristics in business logic
- Deeply nested conditionals (cyclomatic complexity)
- Configuration buried in code
- Repeated patterns that should be abstracted
- Hardcoded URLs, credentials, environment assumptions
- Clever algorithms where simple + scalable would work

## Working with This Repository

### Making Changes to Commands

Edit the markdown files in `commands/` directly. The content is the instruction prompt. Keep instructions:
- **Concrete and actionable** (not vague principles)
- **Output format explicit** (show exactly what the response should look like)
- **Scannable** (use headers, bullets, examples)

### Modifying Plugin Metadata

- `plugin.json` — Update version, name, or entry points here
- `marketplace.json` — Marketplace listing metadata (description, tags)

Both files must stay in sync for version numbers.

### Hook Configuration

The hook in `hooks/hooks.json` triggers after every tool use. The prompt is intentionally brief to avoid noise. If modifying:
- Keep it under 2 sentences
- Focus on significant violations only
- Use the `⚡ Yield:` prefix for consistency

### Adding New Commands

1. Create `commands/your-command.md` with instruction content
2. Commands automatically become available as `/your-command`
3. No need to register in `plugin.json` (auto-discovered from directory)

### Testing Changes

Claude Code plugins are declarative—there's no build step or test suite. To verify changes:
1. Edit the files
2. Reload the plugin: `/plugin reload yield-framework`
3. Test the command: `/yield-check` or `/yield`

## Plugin Philosophy

This plugin **practices what it preaches**:
- All configuration externalized (JSON, not code)
- No magic numbers or hardcoded logic
- Markdown as instruction specification (declarative, not imperative)
- Minimal cleverness—just structured prompts

When extending this plugin, maintain this architecture. Resist the urge to add executable code, custom parsers, or complex logic. The power is in clear instructions to Claude, not in clever tooling.
