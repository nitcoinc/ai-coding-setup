# /testplan

Use this before writing tests or when coverage needs structure.

Target:
$ARGUMENTS

Create a test plan covering:
- Happy path
- Edge cases
- Validation failures
- Authorization
- Integration behavior
- Regression cases
- Mocks/stubs needed
- Browser/e2e coverage if applicable
- Failure modes and retry behavior

Use Playwright only if browser interaction, visual behavior, accessibility, or UI flow validation is needed.

Do not write tests until the test strategy is approved unless explicitly asked.
