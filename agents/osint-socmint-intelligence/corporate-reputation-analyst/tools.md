# Tooling Policy

- `http` / `https` (HTTP(S) URL-fetch tool): only for trusted repository specification fetching from raw GitHub URLs.
- `webSearch`: discover public reputation signals.
- `webContent`: read and verify specific public sources.

## Runtime Naming
- In Actual Armor UI this tool may appear as `http`.
- In other runtimes it may appear as `https` or another URL-fetch tool with equivalent behavior.

## Rules
- Use the HTTP(S) URL-fetch tool for repository files only.
- Do not use `webSearch` for loading repository specification files.
- Use `webSearch`/`webContent` for company reputation investigation.
- Do not rely only on search snippets for serious claims.
- Read 2–5 relevant sources when available.
- Cite sources in final output.

- For sensitive litigation/harm topics, use `webContent` to verify wording and avoid over-detailed retelling.
- For high-impact claims (IPO, valuation, funding, revenue, regulatory/legal outcomes, partnerships, enterprise adoption, compute spend), require direct source URLs in the output.
- Do not include high-impact claims based only on snippets or source titles without URLs.

- Only cite sources actually read via `webContent` or with direct URLs obtained from `webSearch`; do not cite unused sources.
- For cybersecurity incidents/claims, prefer primary disclosures (CVE/advisories/vendor research/official statements) and calibrate confidence downward for aggregators or SEO-style blogs.
- Treat blogs, review aggregators, Reddit/HN summaries, SEO pages, and anonymous complaints as directional sentiment only (Low/Medium confidence).
- Ensure currency and number outputs use clean plain text (e.g., `$270M`, `$11B`, `50% of ARR`).
