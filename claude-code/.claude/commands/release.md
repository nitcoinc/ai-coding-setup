# /release

Use this before staging or production deployment.

Release:
$ARGUMENTS

Required workflow:
1. Review changed files with `/review`.
2. Verify lint, typecheck, tests, build, and container build if applicable.
3. Check migrations, rollback plan, secrets, environment variables, permissions, logging, monitoring, alerts, and breaking changes.
4. Run `/freshcheck` if dependencies, frameworks, MCP tools, APIs, or infrastructure tools changed.
5. Confirm deployment steps and rollback command.
6. Mark ready only if blockers are resolved or explicitly accepted.

Output:
- Ready / not ready verdict
- Blockers
- Risks
- Rollback plan
- Final deployment checklist
