# Due Diligence Squad

## Short Description
A pilot multi-agent workflow that combines Legitimacy Lens, Executive Authority Auditor, Scam Scout, Reverse Image / Visual Verification, and Source Verification / Evidence Pack Builder to produce structured, evidence-grounded diligence outputs for human decision-makers.

## Primary Users
### Human operator
Funds, analysts, partnership teams, B2B teams, and founders who need faster, repeatable diligence before commitments, introductions, vendor onboarding, or deal progression.

### AI agent
A coordinated set of specialized AI agents that divide investigation tasks, cross-check each other’s findings, and compile a unified evidence package and risk narrative for human approval.

## When To Use
- Early-to-mid diligence on counterparties, opportunities, or strategic proposals.
- Situations requiring rapid but structured trust and risk assessment.
- Multi-signal reviews where identity, authority, legitimacy, and scam risk all matter.
- Cases where teams need an auditable rationale before proceeding.

## Inputs
- Counterparty identity claims, organization details, and proposal materials.
- Links to websites, profiles, media assets, and communications.
- Key diligence questions from the human operator.
- Any prior notes, risk hypotheses, or constraints.

## Process
1. **Intake and scope definition**: Human defines objectives, timeline, and material decision thresholds.
2. **Legitimacy Lens stream**: Validate entity/project/founder legitimacy through claim-evidence mapping.
3. **Executive Authority Auditor stream**: Verify whether key contacts appear to have claimed authority.
4. **Scam Scout stream**: Perform rapid scam-risk triage and red-flag classification.
5. **Reverse Image / Visual Verification stream**: Test visual claims, profile-image reuse, and media context integrity.
6. **Source Verification / Evidence Pack Builder stream**: Standardize citations, timestamps, and evidence quality annotations.
7. **Cross-stream reconciliation**: Resolve conflicts, track unknowns, and unify confidence language.
8. **Human review package**: Deliver final outputs for approval, escalation, or next-step instruction.

## Outputs
- **Risk memo**: concise narrative of principal risks, mitigations, and open concerns.
- **Evidence pack**: organized source set with claim links, timestamps, and quality ratings.
- **Confidence summary**: per-domain confidence (identity, authority, legitimacy, scam risk, visual context).
- **Recommended next questions**: targeted requests to close material uncertainty before action.

## Evidence Requirements
- Every material claim should map to attributable evidence or be marked unverified.
- Use cross-source corroboration for high-impact conclusions.
- Maintain transparent provenance (where evidence came from, when, and why it matters).
- Preserve contradictory or disconfirming evidence in the final package.

## Confidence / Risk Notes
- This workflow improves rigor and speed, but does not eliminate uncertainty.
- Confidence is cumulative and should reflect weakest-link evidence gaps.
- Risk labels should be explicit, explainable, and revisable with new information.

## Human Decision Checkpoints
- Approve scope and decision criteria before analysis begins.
- Review and resolve major contradictions flagged by agents.
- Decide final disposition: proceed, proceed with controls, request more evidence, pause, or decline.
- Approve any external communication, publication, escalation, or contractual action.

## Example Agent Use
A diligence team receives a partnership proposal. Specialized agents run legitimacy, authority, scam triage, and visual checks in parallel, then hand a unified evidence pack to a human operator who approves a “proceed with additional verification” decision and sends targeted follow-up questions.

## Not Included / Out of Scope
- Autonomous deal approval or rejection.
- Legal, financial, or regulatory determinations.
- Private-source intelligence collection or unauthorized access.

## Public-Safe Notes
This is a public-safe capability workflow description for reusable agent collaboration. It excludes internal roadmap details, private strategy assumptions, credentials, and confidential customer/investor information.
