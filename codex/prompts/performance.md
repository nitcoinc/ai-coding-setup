# /performance

Use this for slow APIs, slow UI, heavy queries, memory growth, CPU issues, or inefficient workflows.

Problem:
$ARGUMENTS

Required workflow:
1. Identify the bottleneck category: database, network, CPU, memory, frontend rendering, external API, startup time, or build time.
2. Gather evidence before optimizing.
3. Use `/freshcheck` if a tool, runtime, framework, or library recommendation may have changed recently.
4. Use Context7 for implementation docs after the tool/framework is chosen.
5. Propose fixes with tradeoffs and rollback risk.
6. Add a validation method: benchmark, regression test, profiling trace, Lighthouse result, or query plan.
7. Avoid large rewrites unless the evidence demands it.

Output:
- Suspected bottleneck
- Evidence
- Recommended fix
- Tradeoffs
- Risk
- Validation method
