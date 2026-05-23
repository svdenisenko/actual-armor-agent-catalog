# Product v2 Workflow: Selecting Next Public-Safe Refactor Candidates

## Goal

Product v2 should convert the private legacy export into a prioritized, public-safe refactor queue **without** copying raw prompts into the public repository.

## Inputs

Product v2 may use the following private-side inputs to decide prioritization:
- private legacy export summary
- agent names
- short public-safe descriptions
- category
- user segment
- likely customer value
- overlap with existing public catalog
- strategic value
- runtime complexity
- tool dependency
- safety/privacy risk
- launch readiness

Raw prompts remain private and must not be copied into this repository.

## Candidate Scoring

Score each candidate from 1-5 across:
- Customer-facing value
- Differentiation from existing public agents
- Runtime simplicity
- Reusability across B2C/B2B/B2G
- Public-safety confidence
- QA feasibility

Optional flags to improve triage quality:
- `duplicate_or_overlap_risk`
- `needs_private_context`
- `requires_sensitive_tools`
- `unclear_user_value`
- `good_p0_candidate`

## Recommended Selection Logic

Prioritize agents that:
- are easy to explain publicly
- have strong customer-facing value
- do not require private AA context
- can run through the thin-shell runtime pattern
- can be smoke-tested quickly
- expand the public catalog without duplicating existing P0 agents

Avoid agents that:
- depend on private workflows
- require raw internal prompts
- overlap too much with existing P0 agents
- need sensitive data or internal tools
- are hard to QA deterministically

## Output Format

Product v2 should produce a short candidate queue in this format:

| Rank | Agent Name | Category | User Segment | Why This Candidate | Public-Safety Risk | Runtime Complexity | Recommended Next Step |
|---|---|---|---|---|---|---|---|

Recommended next-step values:
- `create_metadata_skeleton`
- `merge_with_existing_agent`
- `hold_for_private_review`
- `reject_duplicate`
- `needs_product_clarification`

## Next-Step Flow

For each selected candidate:

1. Create metadata skeleton.
2. Write public-safe clean spec.
3. Create or update `bootstrap.md`.
4. Run runtime loading smoke.
5. Run behavior smoke.
6. Patch QA/readiness status.
7. Add to public-ready catalog only after pass.

## Guardrails

- Do not copy raw prompts.
- Do not commit legacy export files.
- Do not expose private AA context.
- Do not treat live marketplace dump as public source of truth.
- Public catalog specs must be rewritten, not copied.
