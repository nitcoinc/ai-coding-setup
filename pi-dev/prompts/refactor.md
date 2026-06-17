# /refactor

Use this to improve structure without changing behavior.

Target:
$ARGUMENTS

Required workflow:
1. State the behavior that must remain unchanged.
2. Identify code smells, coupling, duplication, ownership boundaries, and tests that protect behavior.
3. Create a staged refactor plan.
4. Do not mix feature work with refactor work.
5. Run tests before and after changes.
6. Keep each edit reversible.
7. Run `/review` after implementation.
8. Store durable architecture decisions with `mem0 add` only if useful.

Output:
- Current problems
- Safe stages
- Files affected
- Behavior-preservation tests
- Rollback plan
