# Public Marketplace Agent Index

This index tracks customer-facing marketplace agents and readiness posture.

> Note: The broader catalog includes 83 agents in current planning scope, but many remain metadata-only placeholders pending full prompt/tool export. This file keeps readiness conservative.

| Agent | Category | Source completeness | Visibility | QA status | Promotion status | Source URL |
|---|---|---|---|---|---|---|
| Corporate Reputation Analyst | Strategic Intelligence / Corporate & Executive Risk | full_spec_draft (pilot baseline present) | public | qa_pending | not_promotion_ready | https://github.com/actual-armor-agent-catalog/agents/osint-socmint-intelligence/corporate-reputation-analyst |
| The Truth Scanner | Narrative Intelligence & Response | full_spec_draft | public_full | runtime_smoke_passed | not_promotion_ready | https://github.com/svdenisenko/actual-armor-agent-catalog/tree/main/agents/osint-socmint-intelligence/the-truth-scanner |
| YouTube Narratives Decoder | Media / Content Intelligence | full_spec_draft | public_full | qa_not_started | not_promotion_ready | https://github.com/svdenisenko/actual-armor-agent-catalog/tree/main/agents/osint-socmint-intelligence/youtube-narratives-decoder |
| Telegram Narrative Monitor | OSINT / SOCMINT Intelligence | metadata_only | public_limited (sensitivity review pending) | qa_not_started | not_promotion_ready | metadata-source-url-required |
| Executive Authority Auditor | Strategic Intelligence / Corporate & Executive Risk | metadata_only | public_limited (sensitivity review pending) | qa_not_started | not_promotion_ready | metadata-source-url-required |
| Remaining marketplace agents (planning set) | Mixed (see `docs/category-map.md`) | metadata_only (bulk) | mixed (default conservative) | qa_not_started | not_promotion_ready | pending validated export mapping |

## Usage
- Product: category and upgrade sequencing.
- CMO: promotion gate visibility and conservative launch filtering.
- QA: smoke-test backlog and sensitive-agent gating.
