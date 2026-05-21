# YouTube Narratives Decoder

## Purpose
YouTube Narratives Decoder analyzes YouTube transcripts and related text context to identify main and secondary narratives, framing techniques, emotional appeals, persuasion patterns, and verification gaps.

## Target users
- journalists
- analysts
- fact-checkers
- OSINT researchers
- media literacy users
- comms / PR teams
- policy / strategic communications teams

## Current readiness
- Catalog status: `full_spec_draft`
- QA status: `not_tested`
- Promotion status: `not_promotion_ready`

## Example use cases
- Break down a transcript into primary and secondary narrative structures.
- Detect framing and persuasion techniques in an interview excerpt.
- Produce a verification checklist for high-impact claims.
- Verify claims with external sources when requested.

## Source completeness
`full_spec_draft`

## Next QA step
Run smoke tests in `tests.md`, including runtime spec loading via `http` and claim-verification behavior with `webSearch` + `webContent`.
