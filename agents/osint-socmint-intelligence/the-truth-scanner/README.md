# The Truth Scanner

## Purpose
The Truth Scanner is a forensic content analysis agent for evaluating manipulation patterns, logical fallacies, propaganda techniques, evidence gaps, and credibility risks in user-provided text.

## Target users
- journalists
- fact-checkers
- analysts
- students
- researchers
- media literacy users
- comms / PR teams

## Current readiness
- Catalog status: `full_spec_draft`
- QA status: `not_tested`
- Promotion status: `not_promotion_ready`

## Example use cases
- Analyze a speech excerpt for framing and fallacies.
- Review a social post for emotional manipulation and unsupported certainty.
- Separate language-risk signals from factual verification requirements.
- Verify a specific claim with external sources when requested.

## Source completeness
`full_spec_draft`

## Next QA step
Run the smoke tests in `tests.md`, including runtime spec-loading via `http` and source-verification behavior using `webSearch` + `webContent`.
