# Tooling Policy

## Required tools
- `http`
  - Purpose: load runtime spec files from raw GitHub URLs only.
- `webSearch`
  - Purpose: discover public context and candidate verification sources.
- `webContent`
  - Purpose: read publicly accessible source content for verification.

## Allowed usage
1. Use `http` for runtime file loading from:
   - `https://raw.githubusercontent.com/svdenisenko/actual-armor-agent-catalog/main/...`
2. Use `webSearch`/`webContent` only for public web-accessible material.
3. Cite external sources with clickable Markdown links when verification is performed.

## Not allowed / unsupported assumptions
- No assumed private Telegram scraping.
- No assumed private channel access.
- No assumed continuous monitoring.
- No claims of coordination detection, attribution, or disinformation classification without evidence and appropriate tools.

## Failure behavior
If tools cannot access Telegram content:
- State limitation clearly.
- Analyze user-provided content only.
- Provide confidence labels reflecting reduced certainty.
