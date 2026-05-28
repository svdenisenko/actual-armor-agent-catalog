# AAF Agent Inventory Raw Import Summary — 2026-05-28

## Import details

- **Import date:** 2026-05-28
- **Source:** Read-only AAF inventory collected under `chat@actualarmor.com`.
- **Raw snapshot:** `catalog/imports/aaf-agent-inventory-2026-05-28.csv`
- **Workflow status:** Raw inventory review input only. This import is **not** a confirmed live marketplace catalog and does **not** promote any imported agent into `catalog/marketplace-agents.yaml`.

## CSV verification

- **Expected columns verified:** `agent_id`, `name`, `category_or_expert_in`, `aaf_edit_url`, `aaf_public_url`, `short_description`, `tools`, `visibility_status`, `public_safe_status`, `qa_status`, `duplicate_possible`, `notes`.
- **Data rows verified:** 88.
- **Prompt/guideline handling:** Full prompts and guidelines were not imported.

## Inventory totals

| Metric | Count |
|---|---:|
| Total agents found | 88 |
| Confirmed public/live agents | 0 |
| Needs review | 66 |
| Internal/test-looking | 22 |

## Visibility/status breakdown

| Field | Value | Count | Review meaning |
|---|---|---:|---|
| `visibility_status` | `readonly` | 66 | Discovered in read-only inventory; requires QA/Product/CMO review before any catalog promotion. |
| `visibility_status` | `private` | 22 | Internal/test-looking inventory; do not promote without explicit review and approval. |
| `public_safe_status` | `NEEDS_REVIEW` | 66 | Public-safe status is unknown and must not be inferred. |
| `public_safe_status` | `INTERNAL_OR_TEST` | 22 | Treat as internal/test-looking until reviewed. |
| `qa_status` | `UNKNOWN` | 88 | No QA pass is recorded by this import. |
| `aaf_public_url` | `UNKNOWN` | 88 | No public AAF links are available from this snapshot. |
| `notes` | `PROMPT_NEEDS_REVIEW` | 88 | Every imported record requires prompt/safety review. |

## Limitations

- All `aaf_public_url` values are `UNKNOWN`.
- Inventory visibility is not enough to confirm public or live marketplace status.
- Full prompts and guidelines were not imported into this repository.
- Every imported agent has `PROMPT_NEEDS_REVIEW` and requires prompt/safety review before any public catalog promotion.
- This snapshot should not be used to claim that any imported agent is `LIVE_IN_AAF`, public-safe, QA-approved, or launch-ready.

## CMO / SendPulse guardrail

- This import is discovery-only.
- Do not use “try this agent now” language for any raw imported agent unless both the catalog status and AAF public link are later verified in the canonical catalog.
- Do not invent public availability, AAF links, lifecycle-email CTAs, or launch claims from this raw inventory snapshot.

## Product / Craft guardrail

- Use this import to avoid duplicates and identify agents that may already exist in AAF.
- Do not treat raw imported agents as launch-ready.
- Do not convert raw imported agents to public catalog records until QA, Product, and CMO review have confirmed their status, safety posture, and public AAF link.

## Recommended next workflow

1. QA classifies the raw inventory and records which agents are duplicates, internal/test-only, candidates for merge, or candidates for public catalog promotion.
2. Product and CMO mark which reviewed agents are SendPulse-safe and what user-facing language, if any, is allowed.
3. Promote only verified public-safe agents into the canonical catalog, with repo-backed evidence, QA state, and verified AAF public links.

## Non-promotion statement

No imported agent from `catalog/imports/aaf-agent-inventory-2026-05-28.csv` is marked `LIVE_IN_AAF`, public-safe, QA-approved, or launch-ready by this summary. This file is raw inventory review input only.
