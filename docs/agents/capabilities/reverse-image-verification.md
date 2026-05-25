# Reverse Image / Visual Verification

## Short Description
Checks visual claims by analyzing image reuse, profile photo consistency, misleading media context, and potential impersonation signals. This capability supports investigations with evidence-grounded findings and does not claim perfect identification.

## Primary Users
### Human operator
Investigators, trust and safety teams, and analysts who need to validate visual narratives before escalation, communication, or publication.

### AI agent
An AI agent that collects candidate matches, compares contextual clues, structures evidence, and drafts a confidence-scored visual verification summary for human review.

## When To Use
- A profile photo appears suspicious or reused.
- A visual claim is central to a risk decision.
- There are concerns about impersonation, fabricated context, or misleading screenshots.
- Teams need a quick visual authenticity checkpoint during due diligence.

## Inputs
- Image files, screenshots, or URLs.
- Claimed identity, timeline, or event context tied to the image.
- Platform/source metadata when available.
- Any prior evidence from related checks.

## Process
1. Normalize the image set (format, key crops, and distinguishing features).
2. Run reverse-image and similarity checks across multiple public sources.
3. Compare match timelines, publication context, and attribution patterns.
4. Assess whether the same image appears in unrelated identities, regions, or narratives.
5. Document manipulation or context-mismatch indicators (if present).
6. Build an evidence table with source links, timestamps, and relevance notes.
7. Draft a confidence summary with explicit uncertainty.

## Outputs
- Visual verification brief.
- Match table (source, date, context, similarity notes).
- Risk flags (possible impersonation, misleading context, reused image).
- Follow-up questions for unresolved issues.

## Evidence Requirements
- Prefer primary, attributable public sources.
- Capture URLs, publication dates, and context snapshots.
- Distinguish direct evidence from inference.
- Record conflicting evidence rather than suppressing it.

## Confidence / Risk Notes
- Confidence is graded (for example: low/medium/high) based on source quality and consistency.
- Similar-looking images are not proof of identity.
- No single visual signal should be treated as definitive on its own.

## Human Decision Checkpoints
- Confirm whether evidence quality is sufficient for action.
- Approve any escalation to legal, compliance, or external communication.
- Decide whether additional identity verification is required.

## Example Agent Use
An agent receives a suspicious founder profile photo, finds historical appearances of the same image tied to different names, compiles source timestamps, and submits a human-review brief recommending deeper identity checks.

## Not Included / Out of Scope
- Guaranteed identity determination.
- Legal adjudication or accusation.
- Device forensics or private-system intrusion.

## Public-Safe Notes
Public-safe documentation only. This capability excludes private credentials, internal-only playbooks, customer records, and non-public intelligence sources.
