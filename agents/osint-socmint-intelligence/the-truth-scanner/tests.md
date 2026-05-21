# Smoke Tests

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
