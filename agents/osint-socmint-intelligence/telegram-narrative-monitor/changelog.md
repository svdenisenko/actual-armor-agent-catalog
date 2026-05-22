# Changelog

## 2026-05-22
- Upgraded Telegram Narrative Monitor from metadata-only planning entry to `full_spec_draft` runtime package.
- Added complete public-safe operating spec files:
  - `agent.yaml`
  - `README.md`
  - `bootstrap.md`
  - `system.md`
  - `instructions.md`
  - `output-template.md`
  - `knowledge.md`
  - `tools.md`
  - `tests.md`
- Applied readiness/sensitivity constraints:
  - `catalog_status: full_spec_draft`
  - `qa_status: qa_not_started`
  - `promotion_status: not_promotion_ready`
  - `public_catalog_visibility: public_limited`
- Added explicit caveats for Telegram access/tool limitations and verification boundaries.


## 2026-05-22
- QA update: runtime loading smoke test `PASS` (all required operating files loaded via `http`; failed files: none).
- QA update: behavior smoke test `PASS` (narrative/framing analysis succeeded with proper verification boundaries and limitations).
- Updated readiness QA status to `runtime_smoke_passed`.
- Kept promotion status as `not_promotion_ready`.
