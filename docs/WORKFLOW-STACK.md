# Workflow Stack

This repo uses a lean workflow-alias stack instead of local skill folders.

## Included Aliases

- `/onboard` — understand a repo before work.
- `/spec` — write/pressure-test a spec.
- `/feature` — build functionality safely.
- `/implement` — execute an approved spec.
- `/incident` — debug and fix issues.
- `/performance` — investigate slowness.
- `/ui` — design and verify frontend work.
- `/security` — review security-sensitive work.
- `/dependency-update` — upgrade packages safely.
- `/release` — prepare deployment.
- `/refactor` — improve structure safely.
- `/review` — review code.
- `/testplan` — design tests.
- `/freshcheck` — research current external facts.
- `/pressuretest` — challenge assumptions.
- `/goodpractices` — improve repo health.

## Tools To Keep

- Context7 MCP for current implementation docs.
- Playwright MCP for browser and UI validation.
- Mem0 CLI for durable personal/project memory.
- CocoIndex Code (`ccc`) for semantic repo search.

## Tools To Avoid By Default

- Duplicate memory MCPs.
- Duplicate documentation MCPs.
- Dox or another overlapping documentation framework.
- Full unfiltered third-party skill libraries.
- Unpinned MCP versions in committed config.

## Memory Rule

Use Mem0 as CLI-first memory:

```bash
mem0 add "This repo uses workflow aliases, not local skill folders."
mem0 search "repo workflow"
mem0 list --limit 20
```

Never store secrets or private customer data.
