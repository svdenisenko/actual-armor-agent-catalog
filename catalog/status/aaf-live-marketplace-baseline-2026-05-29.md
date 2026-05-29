# AAF Live Marketplace Baseline — 2026-05-29

## 1. Purpose

This document records the first live AAF marketplace baseline after the 2026-05-28 discovery-only raw inventory import.

As of 2026-05-29, AAF marketplace agents are visible and accessible to users in AAF. This means the marketplace now has live availability that was not confirmed in the 2026-05-28 raw import classification.

This is a **live marketplace availability baseline**, not a full Product/QA pass. Live availability does not mean every live agent is production-grade, email-ready, paid-ads-ready, enterprise-ready, legally/compliance-approved, recommended, or best-in-class.

## 2. Relationship to the 2026-05-28 raw inventory import

The 2026-05-28 raw inventory remains preserved as historical evidence of a discovery-only import state. At that time, the classification correctly treated imported records conservatively because public/live status and usable AAF links were not verified.

The 2026-05-28 import should not be erased, rewritten, or retroactively changed. It remains useful for provenance, duplicate analysis, and review planning.

The 2026-05-29 live marketplace baseline supersedes the 2026-05-28 import **only for current availability status** when agents are freshly exported or manually confirmed as live/user-accessible in AAF.

## 3. Baseline composition rule

The live marketplace baseline should combine:

1. The previous **88 imported agents** from the 2026-05-28 raw inventory, where their current AAF live availability is confirmed; and
2. Newly released AAF agents from 2026-05-29, when a fresh export or manual Product confirmation is available.

Do not infer live status for an exact agent solely from the historical CSV. Use a fresh AAF export, AAF marketplace visibility check, or Product human confirmation.

## 4. Status model

### 4.1 Availability status

Availability answers whether an agent can be accessed in AAF. It does **not** answer whether the agent is high quality, safe to promote, or approved for campaign use.

| Status | Meaning |
|---|---|
| `LIVE_IN_AAF` | Agent is visible and accessible to users in AAF. |
| `PRIVATE_INTERNAL` | Agent exists but is internal-only, private, or not intended for general user access. |
| `DISABLED` | Agent is disabled, retired, removed from access, or intentionally unavailable. |
| `UNKNOWN` | Current access state has not been confirmed. |

### 4.2 Quality status

Quality answers what Product/QA currently believes about the agent's prompt, outputs, positioning, safety, overlap, and readiness.

| Status | Meaning |
|---|---|
| `NEEDS_REVIEW` | Default for live agents that have not yet passed Product/QA review. |
| `QA_PASSED_LIMITED` | Product/QA reviewed the agent and approved limited use within documented constraints. |
| `NEEDS_IMPROVEMENT` | Agent is live or known, but prompt, copy, behavior, or UX needs improvement. |
| `DUPLICATE_CANDIDATE` | Agent may overlap with another agent and should be reviewed for merge/consolidation. |
| `REPOSITION_CANDIDATE` | Agent may be useful but needs a safer, clearer, or more accurate market position. |
| `DEPRECATE_CANDIDATE` | Agent is a candidate for retirement or removal. |

`QA_PASSED` must not be assigned by default. A live marketplace state is not evidence of a QA pass.

### 4.3 Sales status

Sales status defines what Sales, BD, CBDO, and CMO may sell or discuss.

| Status | Meaning |
|---|---|
| `CAN_SELL_CATEGORY` | Team may sell the marketplace and workflow category story without promoting exact agents as reviewed products. |
| `CAN_SELL_WITH_REVIEW` | Team may discuss the agent with Product/QA-reviewed caveats, constraints, and links. |
| `CAN_SELL` | Team may sell the exact agent after Product/QA approves positioning, quality status, and user-facing link. |

### 4.4 Promotion status

Promotion status controls public marketing, demos, email, and paid ads.

| Status | Meaning |
|---|---|
| `CATEGORY_LEVEL_OK` | Category/workflow-level language is allowed; exact-agent claims remain gated. |
| `CAN_USE_IN_DEMOS` | Agent may be used in approved demos with reviewed constraints. |
| `CAN_USE_IN_EMAILS_IF_LINK_VERIFIED` | Agent may be used in lifecycle/SendPulse emails only after Product verifies quality, copy, and a usable AAF link. |
| `CAN_USE_IN_PAID_ADS_AFTER_CMO_REVIEW` | Agent may be used in paid ads after CMO review and Product/QA approval. |
| `DO_NOT_PROMOTE_YET` | Do not use in user-facing promotion. |

## 5. Default baseline rule for live agents pending Product/QA review

For all currently live AAF agents that have not yet passed Product/QA review, assign this default bundle:

```yaml
aaf_visibility: LIVE_IN_AAF
quality_status: NEEDS_REVIEW
sales_status: CAN_SELL_CATEGORY
promotion_status: CATEGORY_LEVEL_OK
email_status: EXACT_AGENT_NEEDS_REVIEW
paid_ads_status: DO_NOT_USE_IN_PAID_ADS_YET
```

This default allows Sales/BD/CMO to describe the live marketplace and broad workflow categories while keeping exact-agent promotion gated.

## 6. What CMO/CBDO/BD may safely say now

CMO, CBDO, and BD may use category-level marketplace language such as:

- Actual Armor has a live marketplace of agents and workflows.
- Users can access live agents in AAF.
- The marketplace supports workflow categories such as OSINT, narrative intelligence, strategic intelligence, corporate investigations, media/content analysis, and risk workflows.
- The team is actively reviewing, improving, consolidating, and packaging the live agent catalog.

Recommended framing: sell the existence of the live marketplace, the workflow categories, and the review/improvement process. Avoid implying that every exact agent is reviewed, recommended, or suitable for all public promotion.

## 7. What CMO/CBDO/BD must not say yet

Until Product/QA has reviewed exact agents and verified usable AAF links, do not say or imply that:

- All agents are QA-passed.
- All agents are enterprise-grade.
- Agents provide regulated compliance determinations, legal conclusions, guaranteed detection, or forensic certainty.
- Exact agents may be promoted in SendPulse or paid ads without Product verification of quality status, public-safe copy, and a usable AAF link.
- Every live agent is recommended or best-in-class.

Do not promote exact agents in SendPulse or paid ads unless Product verifies quality status, public-safe copy, and usable AAF link.

## 8. Product/QA marketplace review loop

Product human reviewers, AAB Product, and Craft/Test/QA agents should review the live marketplace category by category. For each exact agent, assign one review disposition:

| Disposition | Meaning |
|---|---|
| `KEEP_AS_IS` | Agent can remain live as currently positioned, subject to any documented constraints. |
| `IMPROVE_PROMPT` | Agent should remain under review while prompt, behavior, output format, or instructions are improved. |
| `REPOSITION` | Agent should be renamed, reframed, recategorized, or scoped more safely/clearly. |
| `MERGE_WITH_DUPLICATE` | Agent overlaps with another agent and should be consolidated or redirected. |
| `DISABLE` | Agent should be disabled or removed from marketplace access. |
| `PROMOTE_TO_RECOMMENDED` | Agent is strong enough, reviewed enough, and linked enough for recommended placement or exact-agent promotion. |

The review loop should capture:

1. Current AAF availability.
2. Usable AAF link status.
3. Prompt and output quality.
4. Safety, legal, compliance, and claim-risk constraints.
5. Duplicate/overlap status.
6. Sales and promotion status.
7. Next owner and target follow-up date.

## 9. Recommended review order

1. Corporate Investigations / Strategic Intelligence
2. Narrative / Media / Disinformation
3. OSINT / SOCMINT
4. Risk / Compliance-like workflows
5. PR / Reputation
6. Education / onboarding helpers

This order prioritizes commercially important and safety-sensitive categories first, then moves into broader onboarding and education support.

## 10. Operating guardrails

- `LIVE_IN_AAF` means visible/accessible to users in AAF; it does not mean QA-passed.
- `NEEDS_REVIEW` remains the default quality status until Product/QA changes it.
- Category-level marketplace sales are allowed now.
- Exact-agent email, paid-ads, enterprise, compliance, or recommended claims require Product/QA review and verified usable AAF links.
- Historical 2026-05-28 evidence remains preserved and should continue to be cited as the discovery-only import snapshot.
