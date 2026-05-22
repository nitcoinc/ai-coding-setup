# AI Coding Setup

> Copy-paste files for **Claude Code** and **OpenCode**. Manual install, zero scripts. One playbook, one workflow, every project.

This is the minimum kit to make an AI coding agent useful on a real project. No automation. No `curl | bash`. You install tools manually, copy a folder into your project, and follow the 7-phase playbook.

---

## What's in this repo

| Path | What it is |
|---|---|
| **[INSTALL.md](INSTALL.md)** | Manual install — prerequisites, tools, agent choice, copy steps. Start here. |
| **[PLAYBOOK.md](PLAYBOOK.md)** | The 7-phase workflow: Brief → Brainstorm → Plan → Implement → Verify → Review → Ship. |
| **[DEMO.md](DEMO.md)** | End-to-end walkthrough for the team — one realistic feature from idea to merged PR. ~30 min. |
| **[MAINTAINING.md](MAINTAINING.md)** | Maintainer's guide — north star, design decisions, enhancement backlog, AI-session prompts for evolving this repo. |
| `skills/` | 11 skills copied into `~/.claude/skills/` once. Used by both agents. |
| `claude-code/` | Drop-in folder for Claude Code projects (`CLAUDE.md`, `.mcp.json`, hooks, slash commands). |
| `opencode/` | Drop-in folder for OpenCode projects (`AGENTS.md`, `opencode.json`, slash commands). |

---

## Get going in 4 steps

1. Read **[INSTALL.md](INSTALL.md)** — install prerequisites, pick an agent.
2. Copy `skills/` → `~/.claude/skills/` (global, once).
3. Copy either `claude-code/` or `opencode/` contents into your project root.
4. Fill in the `<PLACEHOLDERS>` in `CLAUDE.md` / `AGENTS.md`.

Open the project. Read **[PLAYBOOK.md](PLAYBOOK.md)**. Start at Phase 0.

---

## Why this exists

Most "AI coding setups" are loose collections of prompts. This one is intentionally small:

- **Skills do the work.** Brainstorm, plan, TDD, debug, review — each is a self-contained skill the agent invokes.
- **PROJECT.md tracks state.** A single file at your repo root holds current task, decisions, failed approaches, next steps. Survives context compaction, session switches, and handoffs.
- **AGENTS.md / CLAUDE.md is the contract.** One short file every agent reads first. Verification commands live there once, never inline.
- **The playbook is the orchestration.** Seven phases, mapped to skills. Stack-agnostic.

If you outgrow it, delete what you don't use. The whole repo is < 1000 lines.

---

## What this repo does NOT do

- No installer script. Every step is manual.
- No `/setup-stack` slash command.
- No telemetry. Nothing phones home.
- No stack opinions baked into the playbook — your `AGENTS.md` defines the stack.

Manual is the feature.

---

## Skills shipped

| Skill | When it activates |
|---|---|
| `brainstorm` | Designing a feature — produces an approved spec |
| `plan` | Writing a TDD-ready implementation plan from a spec |
| `tdd` | Implementing a task — failing test first, always |
| `debug` | Something broken — 4-phase root cause before any fix |
| `code-review` | Reviewing diff — severity-prefixed feedback |
| `refactor` | Restructuring code without changing behaviour |
| `pr-review` | Reviewing a pull request from another author |
| `frontend-design` | Building React components, pages, visual UI |
| `migration` | Live database schema changes — expand/contract |
| `profile` | System is slow — measure-before-optimize |
| `onboarding` | First session in unfamiliar codebase |

Each is one `SKILL.md`. Read them. Edit them. They are not magic.

---

## License

MIT — see [LICENSE](LICENSE).
