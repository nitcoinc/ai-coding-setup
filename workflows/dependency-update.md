# /dependency-update

Use this for stable dependency updates.

Target:
$ARGUMENTS

Required workflow:
1. Use `/freshcheck` for the dependency or tool.
2. Prefer latest stable patch in the current major before minor/major upgrades.
3. Avoid prerelease versions unless explicitly approved.
4. Respect pnpm `minimumReleaseAge` and committed lockfiles.
5. For Python, use `uv lock --upgrade-package <name>` when possible.
6. Read changelog/release notes for breaking changes.
7. Run audit, tests, typecheck, lint, build, and app-specific smoke checks.
8. Document behavior changes and rollback.

Output:
- Current version
- Target version
- Reason
- Risks
- Verification results
- Rollback plan
