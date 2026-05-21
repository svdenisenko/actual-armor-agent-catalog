# Public Agent Import Rules (Pre-Catalog)

These rules govern validation of OpenClaw exports before generating Actual Armor public catalog specs.

## 1) Required fields

Each candidate agent must include:

- `name`
- `description`
- `role` **or** `expertise`
- `instructions`
- `tools`

### Rule

If any required field is missing, the agent is not import-ready and must be listed in validation findings.

---

## 2) Internal/backoffice exclusion rules

The following assistant classes are excluded from public import scope:

- CEO
- CMO
- CTO
- CBDO
- Product
- Craft
- Test
- Workspace operators

### Rule

Any agent matching these classes is excluded from the public import dataset and logged with exclusion reason.

---

## 3) Sensitive agent tagging rules

Mark agents as sensitive if they involve:

- people search
- wealth / asset tracing
- PEP mapping
- dark web exposure
- sanctions / compliance
- identity analysis
- cyber risk

### Rule

Sensitive status requires explicit flagging for policy/compliance review and downstream visibility control.

---

## 4) Public visibility levels

Every import candidate must be assigned exactly one visibility level:

- `public_full`
- `public_limited`
- `aa_only`
- `restricted_internal`

### Rule

Visibility level must reflect risk, sensitivity, and publication policy.

---

## 5) Default readiness metadata

Set these defaults for imported agents:

- `catalog_status: imported`
- `qa_status: not_tested`
- `promotion_status: not_promotion_ready`

### Rule

Defaults are mandatory unless a later formal QA/promotion workflow overrides them.

---

## 6) Disallowed content (must not be included)

Do not include:

- private Actual Armor context
- investor/team/board information
- private links
- internal OpenWebUI/OpenClaw operating details
- revenue/traction/user/pilot claims

### Rule

If disallowed content is present, redact or block the agent from import based on policy severity, and capture action in validation report.

---

## 7) Phase boundary

This validation phase is pre-spec only.

### Rule

Do **not** generate actual public agent specs during this phase.
