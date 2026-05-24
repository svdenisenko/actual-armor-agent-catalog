# QA Status: Corporate Reputation Analyst

- status: craft_packet_ready
- workflow_state: ready_for_manual_craft
- reference_role: first practical factory-loop reference agent
- required_tools:
  - HTTP bootstrap loader
  - web search
  - web content
- blocked_tools:
  - Telegram MCP
  - Telemetr MCP
  - private AA context
  - raw legacy exports
- next_step: OpenWebUI Product V3 should prepare Marketplace Creation Package, then run manual craft (or future Playwright craft).
- post_craft_step: Tester Agent must run smoke QA using qa/smoke-tests/corporate-reputation-analyst.md
- approval_gate: human Product approval is required before promotion/public-ready status
- public_readiness: not public_ready until runtime marketplace QA and human Product approval
- tester_handoff: qa/smoke-tests/corporate-reputation-analyst.md
