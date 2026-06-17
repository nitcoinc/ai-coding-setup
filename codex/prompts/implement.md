# /implement

Use this to execute an approved spec or plan with a bulletproof implementation loop.

Plan:
$ARGUMENTS

Bulletproof implementation strategy:
1. Re-read the approved spec/plan and agent rules.
2. Confirm the smallest safe slice.
3. Add or update tests first when practical.
4. Implement one slice.
5. Run targeted verification.
6. Repeat until the plan is complete.
7. Run full verification: lint, typecheck, tests, build, and UI/browser checks when relevant.
8. Run `/review`.
9. Update docs and memory only with durable decisions.

Stop if evidence contradicts the plan; revise the spec instead of forcing code through.
