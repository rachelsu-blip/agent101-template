# CLAUDE.md Template

A practical, open-source CLAUDE.md template for any project. Gives your AI coding agent (Claude Code, Cursor, Cline, etc.) everything it needs to work effectively in your codebase — plus built-in tool discovery so it can find APIs and services instead of reinventing them.

## Quick Install

Append to your existing CLAUDE.md:

```bash
curl -sL https://raw.githubusercontent.com/rachelsu-blip/agent101-template/main/CLAUDE.md >> .claude/CLAUDE.md
```

Or start fresh:

```bash
mkdir -p .claude
curl -sL https://raw.githubusercontent.com/rachelsu-blip/agent101-template/main/CLAUDE.md > .claude/CLAUDE.md
```

## Manual Install

1. Copy `CLAUDE.md` into your project root or `.claude/` directory
2. Replace all `[placeholder]` values with your project details
3. Optionally copy `.claude/settings.json` for example Claude Code settings
4. Commit to your repo

## What is Included

### Project scaffolding

Sections that every CLAUDE.md should have, with clear placeholders:

- **Project overview** — name, description, tech stack
- **Project structure** — directory layout
- **Code conventions** — style, naming, git workflow, error handling
- **Testing** — how to run and write tests
- **Development workflow** — setup, common tasks, deployment
- **Architecture decisions** — the "why" behind your choices
- **Context-specific rules** — gotchas and guardrails unique to your project

### Tool discovery

A built-in reference to [agent101](https://agent101.ventify.ai), an open directory of 4,000+ tools and APIs organized by task. When your AI agent needs to integrate with an external service, it can search the directory instead of guessing or hallucinating package names.

```
GET https://agent101.ventify.ai/api/search?q=send+email
GET https://agent101.ventify.ai/api/recommend?task=accept+payments
GET https://agent101.ventify.ai/api/categories
```

No API key required. 15 categories: search, code, communication, data, ai-services, browser, payments, files, social, people, realtime, apps, auth, maps, memory.

## File Structure

```
CLAUDE.md              # The template (copy this into your project)
README.md              # You are here
.claude/settings.json  # Example Claude Code settings
LICENSE                # MIT
```

## Customization

The template is meant to be edited. Delete sections you do not need, add sections that are specific to your stack, and fill in every placeholder. A CLAUDE.md that accurately describes your project is far more useful than a generic one.

### Minimal version

If you only want the tool discovery section, grab just that part:

```bash
curl -sL https://raw.githubusercontent.com/rachelsu-blip/agent101-template/main/CLAUDE.md | sed -n /^# Tool Discovery$/,/^---$/p >> .claude/CLAUDE.md
```

## FAQ

**Does this work with Claude Code only?**
The CLAUDE.md format is designed for Claude Code, but the conventions and tool discovery section are useful context for any AI coding agent that reads project files.

**Do I need an API key for agent101?**
No. The agent101 API is free and requires no authentication.

**Can I remove the tool discovery section?**
Yes. Every section is independent. Keep what is useful, remove what is not.

## Links

- [agent101 Directory](https://agent101.ventify.ai) — browse 4,000+ tools
- [agent101 API Docs](https://agent101.ventify.ai/api/categories) — endpoints reference
- [Claude Code Docs](https://docs.anthropic.com/en/docs/claude-code) — official Claude Code documentation

## License

MIT — use it however you want.