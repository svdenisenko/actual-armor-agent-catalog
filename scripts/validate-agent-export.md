# Validate Public Agent Export (Pre-Spec)

Use this checklist before any public catalog spec generation.

## Inputs

- Raw export file: `exports/aa-public-agents-raw.json`
- Rules reference: `docs/import-rules.md`

## Output (this step)

- A validated import-ready dataset (naming TBD by implementation team)
- Validation report with:
  - excluded agents and reasons
  - sensitive flags applied
  - visibility assignments
  - missing/invalid field findings

## Step-by-step checklist

1. **Load raw export**
   - Confirm file exists and is valid JSON.
   - Confirm top-level structure (array/object) expected by importer.

2. **Validate required fields per agent**
   - `name`
   - `description`
   - `role` **or** `expertise`
   - `instructions`
   - `tools`
   - If missing, mark agent as invalid for import and add to validation report.

3. **Exclude internal/backoffice assistants**
   - Exclude if agent is identified as one of:
     - CEO
     - CMO
     - CTO
     - CBDO
     - Product
     - Craft
     - Test
     - Workspace operators
   - Record exclusion rationale in validation report.

4. **Mark sensitive agents**
   - Flag when scope includes any of:
     - people search
     - wealth / asset tracing
     - PEP mapping
     - dark web exposure
     - sanctions / compliance
     - identity analysis
     - cyber risk
   - Do not auto-exclude solely for sensitivity; flag for policy review.

5. **Assign public visibility level**
   - Allowed values:
     - `public_full`
     - `public_limited`
     - `aa_only`
     - `restricted_internal`
   - Assign based on content risk and publication policy.

6. **Apply default readiness statuses**
   - `catalog_status: imported`
   - `qa_status: not_tested`
   - `promotion_status: not_promotion_ready`

7. **Strip disallowed content**
   - Ensure records do not include:
     - private Actual Armor context
     - investor/team/board information
     - private links
     - internal OpenWebUI/OpenClaw operating details
     - revenue/traction/user/pilot claims
   - If detected, redact or block import per policy severity.

8. **Finalize validation report**
   - Include totals:
     - total agents processed
     - valid agents
     - excluded agents
     - sensitive-flagged agents
     - blocked agents (policy violations)

## Acceptance gate

Proceed to spec generation only when:

- Rules in `docs/import-rules.md` were fully applied.
- Validation report is complete and auditable.
- This phase produced **no public catalog specs**.
