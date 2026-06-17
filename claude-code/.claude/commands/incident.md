# /incident

Use this when something is broken.

Issue:
$ARGUMENTS

Required workflow:
1. Do not guess the fix first.
2. Capture symptoms, scope, recent changes, and reproduction steps.
3. Identify possible causes and evidence needed.
4. Inspect only relevant files, logs, tests, and runtime behavior.
5. Form a root-cause hypothesis and validate it.
6. Implement the smallest safe fix.
7. Add or update a regression test.
8. Run `/review` and release checks if production is affected.
9. Store a durable prevention note with `mem0 add` only if it will help future sessions.

Output:
- Symptoms
- Evidence checked
- Root cause
- Fix
- Regression test
- Prevention measure
