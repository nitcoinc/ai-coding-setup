# Playbook

> Use workflow aliases to keep agent work focused, current, and verifiable.

## Default Flow

```text
/onboard -> /spec -> /pressuretest -> /implement -> /review -> /release
```

Skip steps only when the task is truly small.

## When To Use Each Alias

| Situation | Alias |
|---|---|
| New repo or unfamiliar area | `/onboard` |
| Serious feature or architecture change | `/spec` |
| New functionality | `/feature` |
| Approved spec ready for coding | `/implement` |
| Bug or production issue | `/incident` |
| Slow API, UI, build, query, memory, CPU | `/performance` |
| UI or frontend behavior | `/ui` |
| Auth, permissions, secrets, dependency risk | `/security` |
| Package upgrades | `/dependency-update` |
| Before deployment | `/release` |
| Behavior-preserving cleanup | `/refactor` |
| Code review | `/review` |
| Test planning | `/testplan` |
| Current external research | `/freshcheck` |
| Challenge a plan | `/pressuretest` |
| Improve repo health | `/goodpractices` |

## Spec-Driven Work

Use `/spec` when work touches multiple files, APIs, auth, data, infrastructure, dependencies, or user-facing behavior.

The spec should define:
- Goal
- Non-goals
- Affected files
- Data flow
- Error handling
- Security boundaries
- Tests
- Rollback or recovery

Then use `/implement` to execute in small slices.

## Tool Rules

- Use `ccc search "<intent>"` for semantic repo search before broad reads.
- Use `/freshcheck` for external tool/library freshness.
- Use Context7 only after a library/framework is selected.
- Use Playwright for browser/UI validation.
- Use `mem0 add` only for durable, non-sensitive memory.

## Done Means

- Verification commands pass.
- UI work checked on desktop and mobile when relevant.
- `/review` has no unresolved critical/high findings.
- `PROJECT.md` is current.
- Durable decisions are stored with Mem0 when useful.
