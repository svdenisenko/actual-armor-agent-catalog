# P0 Upgrade Plan

This plan defines the first full-spec upgrade batch for high-priority marketplace agents.

## P0 Batch
1. Corporate Reputation Analyst (already full-spec pilot)
2. The Truth Scanner
3. YouTube Narratives Decoder
4. Telegram Narrative Monitor
5. Executive Authority Auditor

## 1) Corporate Reputation Analyst
- **Why important:** Existing full-spec pilot establishes baseline architecture and QA patterns.
- **Expected user segment:** Communications leads, risk teams, and strategic narrative operators.
- **Required next files:** Maintain and iterate existing full set; add/expand scenario coverage in tests and changelog as needed.
- **First smoke test:** Runtime load + baseline narrative intake/output consistency test.
- **Marketing/landing page potential:** High; can be used as reference implementation with conservative claims.

## 2) The Truth Scanner
- **Why important:** Core trust-oriented narrative verification use case.
- **Expected user segment:** Comms teams, analysts, and decision support stakeholders.
- **Required next files:** `agent.yaml`, `bootstrap.md`, `system.md`, `instructions.md`, `output-template.md`, `knowledge.md`, `tools.md`, `tests.md`, `changelog.md`.
- **First smoke test:** Validate claim triage flow with explicit source-backed/unknown separation.
- **Marketing/landing page potential:** High, with strict evidence-positioning language.

## 3) YouTube Narratives Decoder
- **Why important:** Addresses high-volume video narrative channels relevant to influence tracking.
- **Expected user segment:** Media intelligence teams and narrative monitoring operators.
- **Required next files:** full standard agent file set (same list as above).
- **First smoke test:** Parse sample channel/content metadata and return structured narrative themes + confidence notes.
- **Marketing/landing page potential:** High for media-intelligence positioning.

## 4) Telegram Narrative Monitor
- **Why important:** Supports OSINT/SOCMINT monitoring in high-velocity messaging ecosystems.
- **Expected user segment:** OSINT analysts, SOC teams, and risk monitoring functions.
- **Required next files:** full standard agent file set (same list as above).
- **First smoke test:** Ingest sample Telegram narrative snippets and produce source-tagged trend summary.
- **Marketing/landing page potential:** High, but must include sensitivity and QA disclaimers.

## 5) Executive Authority Auditor
- **Why important:** Executive-risk and authority-perception analysis supports strategic and reputational decisions.
- **Expected user segment:** Executive offices, corporate affairs, and risk advisory teams.
- **Required next files:** full standard agent file set (same list as above).
- **First smoke test:** Generate structured executive authority risk factors with explicit evidence/uncertainty fields.
- **Marketing/landing page potential:** Medium-high with careful policy framing.

## P0 Execution Guardrails
- Do not infer unsupported traction, revenue, user, pilot, or partnership claims.
- Do not mark metadata-only agents as launch-ready.
- Apply sensitive-agent policy gating where applicable.
