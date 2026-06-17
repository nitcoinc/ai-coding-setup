# /security

Use this for security review, dependency risk, auth, permissions, data handling, and release hardening.

Target:
$ARGUMENTS

Required workflow:
1. Identify trust boundaries, sensitive data, auth paths, and external inputs.
2. Check dependencies with the project package manager and pinned lockfiles.
3. Use `/freshcheck` for new packages, MCP servers, auth libraries, crypto, infra tools, and AI tooling.
4. Validate secrets are not committed and are read through environment variables or secret stores.
5. Check authorization separately from authentication.
6. Review logging for secret leakage and privacy issues.
7. Add regression tests for security-relevant behavior.

Output:
- Threats
- Findings by severity
- Required fixes
- Tests
- Residual risk
