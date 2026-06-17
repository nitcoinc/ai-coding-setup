# AI Coding Setup

> Drop-in workflow prompts and agent rules for Claude Code, Codex, OpenCode, and Pi.dev. Lean aliases, current docs, browser validation, semantic code search, and CLI-first memory.

This repo is a team starter kit for agentic coding. It intentionally avoids overlapping methodology stacks and local skill sprawl. The core idea is simple: one workflow library, the same aliases across tools, and clear rules for when to spec, implement, review, fresh-check, and release.

## What's In This Repo

| Path | Purpose |
|---|---|
| `workflows/` | Canonical workflow prompts such as `/feature`, `/spec`, `/ui`, `/security`, `/freshcheck`, and `/implement`. |
| `claude-code/` | Claude Code drop-in: `CLAUDE.md`, `.mcp.json`, hooks, slash commands. |
| `codex/` | Codex drop-in: `AGENTS.md`, `config.toml`, global prompt files. |
| `opencode/` | OpenCode drop-in: `AGENTS.md`, `opencode.json`, command files. |
| `pi-dev/` | Pi.dev prompt templates adapted from `workflows/`. |
| `docs/WORKFLOW-STACK.md` | The lean stack decision and tool roles. |
| `docs/PROMPTING-TECHNIQUES.md` | Spec-driven and bulletproof implementation prompting guide. |
| `docs/TECHNICAL-STANDARDS.md` | pnpm, monorepo, Docker, GitHub Actions, and FastAPI standards. |
| `docs/DEPENDENCY-SECURITY.md` | Stable dependency updates, release-age protection, and scanners. |
| `templates/` | Optional app templates for frontend/backend projects. |

## Workflow Aliases

Use aliases instead of vague prompts:

- `/onboard` — understand an unfamiliar repo.
- `/spec` — produce a spec before serious work.
- `/feature` — build functionality safely.
- `/implement` — execute an approved spec slice by slice.
- `/incident` — debug and fix without guessing.
- `/performance` — investigate slowness with evidence.
- `/ui` — design and verify frontend work.
- `/security` — review security, auth, secrets, dependencies.
- `/dependency-update` — update packages safely.
- `/release` — prepare deployment.
- `/refactor` — improve structure without behavior changes.
- `/review` — review code by severity.
- `/testplan` — design test coverage.
- `/freshcheck` — research current external facts.
- `/pressuretest` — challenge plans before implementation.
- `/goodpractices` — find high-leverage repo improvements.

## Tool Roles

- Context7 MCP: current library/framework docs during implementation.
- Playwright MCP: browser, UI, accessibility, and e2e validation.
- Mem0 CLI: durable memory for decisions and preferences.
- CocoIndex Code (`ccc`): semantic repo search.

Do not install duplicate memory MCPs, duplicate docs MCPs, Dox, Superpowers, or full unfiltered third-party skill libraries by default.

## Install Shape

1. Install prerequisites: Python 3.11+, `uv`, Node.js 20+, `pnpm`, `git`, and your agent CLI.
2. Install optional CLIs: `uv tool install cocoindex-code` and `uv tool install mem0ai`.
3. Copy the agent folder into your target project.
4. For Codex, also merge `codex/config.toml` into `~/.codex/config.toml` and copy `codex/prompts/*` to `~/.codex/prompts/`.
5. For Pi.dev, import `pi-dev/prompts/` as reusable prompt templates.

## Default Workflow

For meaningful work:

```text
/onboard -> /spec -> /pressuretest -> /implement -> /review -> /release
```

For UI:

```text
/ui -> /feature or /implement -> Playwright validation -> /review
```

For dependencies:

```text
/freshcheck -> /dependency-update -> full verification -> /release
```

## License

MIT — see `LICENSE`.
