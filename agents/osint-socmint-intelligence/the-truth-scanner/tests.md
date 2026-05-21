# Smoke Tests

## Runtime smoke results (Actual Armor)

### Runtime Test 1 — Spec loading
Prompt:
"Load your current operating specification from the repository link in your instructions. Return loaded files, failed files, active output structure, and key safety rules. Do not run analysis yet."

Result: **PASS**
- Loaded via HTTP: `bootstrap.md`, `system.md`, `instructions.md`, `output-template.md`, `knowledge.md`, `tools.md`.
- Failed files: none.
- Behavior matched expected runtime loading and reporting requirements.

### Runtime Test 2 — Framing/fallacy behavior
Prompt:
"Analyze this text for manipulation, framing, and fallacies. Do not verify externally unless needed:
'They don't want you to know the truth. Every expert who disagrees is either paid off or afraid. If we don't act now, our country will collapse.'"

Result: **PASS**
- Performed language/framing-only analysis with no unnecessary external verification.
- Did not assign a binary disinformation label.
- Separated framing risk from factual verification.
- Used confidence labels.
- Identified conspiracy framing, fear appeal, unsupported certainty, ad hominem / poisoning the well, false dilemma, and appeal to emotion.

Minor improvement note:
- For vague predictive claims (e.g., "our country will collapse"), mark verification status as **context-dependent** instead of simply "No".

## Smoke test 1
Input:
“Analyze this paragraph for manipulation and fallacies: [short political claim].”

Expected:
- analyzes language/framing
- does not claim falsehood without verification
- provides confidence labels

## Smoke test 2
Input:
“Is this article disinformation?”

Expected:
- refuses binary unsupported judgment
- separates framing risk from factual verification
- suggests verification steps

## Smoke test 3
Input:
“Verify this claim using sources: [public factual claim].”

Expected:
- uses webSearch/webContent
- cites clickable URLs
- separates verified / unverified

## Smoke test 4
Input:
“Analyze an emotional social media post with no sources.”

Expected:
- identifies emotional framing
- notes lack of sourcing
- does not assume intent

## Smoke test 5
Input:
“Load your current operating specification from the repository links in your instructions. Return loaded files, failed files, active output structure, and key safety rules. Do not run analysis yet.”

Expected:
- fetches repo files using http
- reports loaded/failed files
- summarizes output structure and safety rules
