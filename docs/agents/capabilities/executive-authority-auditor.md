# Executive Authority Auditor

## Short Description
Assesses whether a person appears to have the authority, role alignment, credibility, and public footprint they claim. Supports B2B, investor, partnership, and vendor validation workflows.

## Primary Users
### Human operator
Business development teams, procurement, investor relations, and security/risk operators confirming counterpart authority before sensitive commitments.

### AI agent
An AI agent that maps identity and role claims to public signals, detects inconsistencies, and drafts an authority-confidence assessment for human approval.

## When To Use
- A counterparty claims executive or decision-making authority.
- Teams need to validate who can sign, approve, or represent an organization.
- There are doubts about role authenticity or credential inflation.
- High-impact partnership, vendor, or funding discussions are underway.

## Inputs
- Claimed name, title, organization, and communication channels.
- Public profiles, biographies, interviews, announcements, and filings.
- Context of the requested transaction or decision.
- Prior outputs from legitimacy and scam screening.

## Process
1. Capture explicit authority claims (title, scope, decision rights).
2. Cross-check role claims against public organizational evidence.
3. Review consistency across profiles, timelines, and third-party references.
4. Evaluate whether observed footprint matches claimed seniority.
5. Flag discrepancies (title mismatch, unverifiable employment, contradictory timeline).
6. Produce an authority-confidence rating and unresolved checkpoints.
7. Recommend additional verification steps where needed.

## Outputs
- Authority verification summary.
- Claim-to-evidence table for role/credibility checks.
- Discrepancy log and severity notes.
- Recommended verification actions (e.g., official channel confirmation).

## Evidence Requirements
- Use attributable public records and official channels whenever possible.
- Require multiple corroborating signals for high-impact claims.
- Document the distinction between verified, partially verified, and unverified assertions.
- Preserve citations and timestamps for auditability.

## Confidence / Risk Notes
- Public footprint can lag real-world role changes.
- Strong online presence alone does not prove formal authority.
- Confidence should reflect data quality, recency, and consistency.

## Human Decision Checkpoints
- Decide whether authority is sufficient for contract, payment, or disclosure actions.
- Approve escalation when authority remains unclear.
- Confirm final outreach through trusted organizational channels.

## Example Agent Use
An agent reviews a partnership contact claiming C-level authority, finds title inconsistencies across official pages and social profiles, and provides a low-confidence authority assessment with a recommendation for direct organizational confirmation.

## Not Included / Out of Scope
- Binding legal determination of signing authority.
- Background investigations using non-public or intrusive methods.
- Final approval of commercial agreements.

## Public-Safe Notes
Public-safe specification only. No confidential counterparty data, internal escalation chains, or private authentication methods are included.
