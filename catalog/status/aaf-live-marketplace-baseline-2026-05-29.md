# AAF Live Marketplace Baseline — 2026-05-29

## 1. Purpose

This document records the first live AAF marketplace baseline after the 2026-05-28 discovery-only raw inventory import.

As of 2026-05-29, AAF marketplace agents are visible and accessible to users in AAF. The working marketplace estimate is **approximately 100 live user-accessible agents**, pending a fresh export for exact count, names, categories, metadata, and usable links.

This is a **live marketplace availability baseline**, not a full Product/QA pass. Live availability does not mean every live agent is production-grade, email-CTA-ready, paid-ads-ready, enterprise-ready, legally/compliance-approved, recommended, or best-in-class.

## 2. Relationship to the 2026-05-28 raw inventory import

The 2026-05-28 raw inventory remains preserved as historical evidence of a discovery-only import state. Its **88 rows are a historical snapshot**, not the current live marketplace count. At that time, the classification correctly treated imported records conservatively because public/live status and usable AAF links were not verified.

The 2026-05-28 import should not be erased, rewritten, or retroactively changed. It remains useful for provenance, duplicate analysis, and review planning.

The 2026-05-29 live marketplace baseline supersedes the 2026-05-28 import for **current availability status and marketplace/category lifecycle email usage**. Use a fresh AAF export, AAF marketplace visibility check, or Product human confirmation for exact current count, metadata, and links.

## 3. Baseline composition rule

The live marketplace baseline should be rebuilt from current AAF evidence and should include:

1. Historical imported agents from the 2026-05-28 raw inventory when their current AAF live availability is confirmed; and
2. Newly released AAF agents from 2026-05-29 when a fresh export or manual Product confirmation is available.

Do not present the old 88-row import as the current marketplace total. Until a fresh export is available, use the approximate current count: **about 100 live user-accessible AAF agents**.

Do not infer QA maturity, recommended placement, enterprise readiness, paid-ads readiness, or exact-agent CTA readiness solely from live marketplace visibility.

## 4. Status model

### 4.1 Availability status

Availability answers whether an agent can be accessed in AAF. It does **not** answer whether the agent is high quality, safe to promote as a top agent, or approved for exact-agent CTA campaigns.

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
| `QA_PASSED` | Product/QA reviewed the agent and approved the stated quality claims for the documented use case. |
| `NEEDS_IMPROVEMENT` | Agent is live or known, but prompt, copy, behavior, or UX needs improvement. |
| `DUPLICATE_CANDIDATE` | Agent may overlap with another agent and should be reviewed for merge/consolidation. |
| `REPOSITION_CANDIDATE` | Agent may be useful but needs a safer, clearer, or more accurate market position. |
| `DEPRECATE_CANDIDATE` | Agent is a candidate for retirement or removal. |

`QA_PASSED_LIMITED` and `QA_PASSED` may be assigned only after Product/QA review. Do not assign a QA-passed status by default. A live marketplace state is not evidence of a QA pass.

### 4.3 Sales status

Sales status defines what Sales, BD, CBDO, and CMO may sell or discuss.

| Status | Meaning |
|---|---|
| `CAN_SELL_CATEGORY` | Team may sell the live marketplace and workflow-category story without claiming every exact agent is QA-passed, recommended, enterprise-grade, or compliance-approved. |
| `CAN_SELL_WITH_REVIEW` | Team may discuss the agent with Product/QA-reviewed caveats, constraints, and links. |
| `CAN_SELL` | Team may sell the exact agent after Product/QA approves positioning, quality status, and user-facing link. |

### 4.4 Promotion status

Promotion status controls public marketing, demos, email, and paid ads.

| Status | Meaning |
|---|---|
| `CATEGORY_LEVEL_OK` | Marketplace/category/workflow-level language is allowed; exact-agent CTA claims remain gated. |
| `CAN_USE_IN_DEMOS` | Agent may be used in approved demos with reviewed constraints. |
| `CAN_USE_IN_EMAILS_IF_LINK_VERIFIED` | Agent may be used for exact-agent lifecycle/SendPulse CTA emails after Product verifies public-safe copy and a usable AAF link. |
| `CAN_USE_IN_PAID_ADS_AFTER_CMO_REVIEW` | Agent may be used in paid ads after CMO review and Product/QA approval. |
| `DO_NOT_PROMOTE_YET` | Do not use this exact agent in user-facing promotion. |

### 4.5 Email-use status

Email status separates normal lifecycle marketing for the live marketplace from gated exact-agent CTAs.

| Status | Meaning |
|---|---|
| `MARKETPLACE_EMAIL_OK` | OK to email about the live Actual Armor marketplace and invite users to open/explore AAF. |
| `CATEGORY_EMAIL_OK` | OK to email about categories such as OSINT, narrative intelligence, strategic intelligence, corporate investigations, media/content analysis, and risk workflows. |
| `EXACT_AGENT_MENTION_OK` | OK to mention selected live agents as examples if the agent is visible in AAF and copy avoids QA, enterprise, compliance, legal-authority, guarantee, and best-in-class claims. |
| `EXACT_AGENT_CTA_OK` | OK to use exact-agent CTA buttons only after Product verifies the usable AAF link and public-safe copy for that exact agent. |
| `DO_NOT_USE_IN_EMAILS` | Use for risky, disabled, duplicate, private/internal, test-looking, unsafe, or otherwise unsuitable exact agents. |

## 5. Default baseline rule for live agents pending Product/QA review

For currently live AAF agents that have not yet passed Product/QA review, assign this default bundle:

```yaml
aaf_visibility: LIVE_IN_AAF
quality_status: NEEDS_REVIEW
sales_status: CAN_SELL_CATEGORY
promotion_status: CATEGORY_LEVEL_OK
email_use_status: MARKETPLACE_EMAIL_OK
category_email_status: CATEGORY_EMAIL_OK
exact_agent_mention_status: ALLOWED_AS_EXAMPLE_WITH_SAFE_COPY
exact_agent_cta_status: NEEDS_LINK_CONFIRMATION
paid_ads_status: DO_NOT_USE_IN_PAID_ADS_YET
```

This default allows CMO/Sales/BD/CBDO to launch live marketplace and workflow-category lifecycle emails now, mention selected visible live agents as careful examples, and keep exact-agent CTA buttons and paid ads gated.

## 6. What CMO/CBDO/BD may safely do now

CMO, CBDO, and BD may now:

- Rewrite and launch lifecycle emails about the live Actual Armor marketplace.
- Use category-level messaging for OSINT, narrative intelligence, strategic intelligence, corporate investigations, media/content analysis, and risk workflows.
- Mention selected agents as examples when they are visibly live in AAF and the copy avoids QA-passed, enterprise-grade, compliance-approved, legal-authority, forensic-certainty, guaranteed-detection, recommended, or best-in-class claims.
- Use marketplace/category CTAs such as “Open Actual Armor,” “Explore live investigation workflows,” “Start your first investigation,” and “Explore the marketplace.”
- Say the team is actively reviewing, improving, consolidating, and packaging the live agent catalog.

Recommended framing: sell the live marketplace, user-accessible workflows, and categories. Exact-agent mentions may be examples, not guarantees of QA maturity or recommended placement.

## 7. What still requires Product/QA/link verification

The following remain gated by Product/QA review, public-safe copy, and/or verified usable AAF links:

- Exact-agent CTA buttons.
- Paid ads around a specific agent.
- Enterprise-grade claims.
- Compliance, legal, detection, or forensic certainty claims.
- Recommended, top-agent, best-in-class, or “officially approved” positioning.
- Any claim that an agent is `QA_PASSED_LIMITED`, `QA_PASSED`, QA-passed, reviewed, compliance-approved, legally authoritative, or guaranteed.

Do not imply that every live agent is recommended, best-in-class, enterprise-grade, compliance-approved, or QA-passed.

## 8. What CMO/CBDO/BD must not say yet

Until the relevant verification is complete, do not say or imply that:

- All agents are QA-passed.
- All agents are enterprise-grade.
- Agents provide regulated compliance determinations, legal conclusions, guaranteed detection, or forensic certainty.
- Exact-agent CTA buttons are approved without Product verification of quality status, public-safe copy, and a usable AAF link.
- Paid ads for exact agents are approved by default.
- Every live agent is recommended or best-in-class.

## 9. Product/QA marketplace review loop

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
6. Sales, email, and promotion status.
7. Next owner and target follow-up date.

## 10. Recommended review order

1. Corporate Investigations / Strategic Intelligence
2. Narrative / Media / Disinformation
3. OSINT / SOCMINT
4. Risk / Compliance-like workflows
5. PR / Reputation
6. Education / onboarding helpers

This order prioritizes commercially important and safety-sensitive categories first, then moves into broader onboarding and education support.

## 11. Operating guardrails

- `LIVE_IN_AAF` means visible/accessible to users in AAF; it does not mean QA-passed.
- Approximately 100 AAF agents are treated as live/user-accessible as of 2026-05-29 pending fresh export; the 88-row import is historical and is not the current marketplace count.
- `NEEDS_REVIEW` remains the default quality status until Product/QA changes it.
- Marketplace/category lifecycle emails are allowed now.
- Selected exact-agent mentions are allowed as examples when the agent is visibly live and the copy is careful.
- Exact-agent CTA emails, paid ads, enterprise claims, compliance/legal/detection/forensic-certainty claims, recommended positioning, and QA-passed claims require Product/QA review and verified usable AAF links.
- Historical 2026-05-28 evidence remains preserved and should continue to be cited as the discovery-only import snapshot.
