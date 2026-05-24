# Corporate Reputation Analyst

Public-safe reference agent for source-grounded corporate reputation analysis.

## Readiness note

This agent is currently the first validated OpenWebUI Product V3 → AA GitHub Repo Reader → marketplace package reference case. It is package-generated and ready for manual craft as draft, but it is not runtime smoke-passed, not promotion-ready, and not public-ready.

## Files

- `agent.yaml` — public metadata and readiness flags.
- `bootstrap.md` — thin-shell bootstrap loader instructions.
- `system.md` — system persona.
- `instructions.md` — operator workflow.
- `output-template.md` — structured response shape.
- `knowledge.md` — domain guidance and constraints.
- `tools.md` — allowed and blocked tool policy.
- `craft-packet.md` — marketplace creation package notes for OpenWebUI Product V3.
- `tests.md` — focused runtime tests.
- `changelog.md` — version history.

## Runtime tool requirements

- Required: HTTP bootstrap loader, `webSearch`, `webContent`.
- Blocked / not required: Telegram MCP, Telemetr MCP, private AA context, raw legacy exports.

## QA handoff

- Smoke test plan: `qa/smoke-tests/corporate-reputation-analyst.md`
- Status tracking: `qa/status/corporate-reputation-analyst.md`
