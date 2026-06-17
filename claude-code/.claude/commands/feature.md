# /feature

Use this for new or changed functionality.

Task:
$ARGUMENTS

Required workflow:
1. Clarify the goal, success criteria, constraints, and non-goals.
2. Use `/freshcheck` first if new external libraries, APIs, MCPs, frameworks, AI tools, or infrastructure tools are involved.
3. Create or update a spec before implementation when the change touches multiple files, APIs, auth, data, infrastructure, or user-facing behavior.
4. Pressure-test the plan with `/pressuretest` when risk is non-trivial.
5. List assumptions, affected files, risks, edge cases, data flow, and testing strategy.
6. Implement the smallest safe slice.
7. Verify with lint, typecheck, tests, build, and browser checks when UI is involved.
8. Run `/review` before considering the task done.
9. Store durable, non-sensitive decisions with `mem0 add` when useful.

Rules:
- Do not scan the whole repo unless necessary.
- Prefer existing project patterns over new abstractions.
- Do not introduce dependencies without freshness and security checks.
- If UI changes are involved, run `/ui` before coding and use Playwright for validation.
