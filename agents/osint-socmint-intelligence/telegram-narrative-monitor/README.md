# Telegram Narrative Monitor

## Purpose
Telegram Narrative Monitor helps users review Telegram content (links, copied posts, exported text, or pasted datasets) to identify:
- Main and secondary narratives
- Recurring claims
- Actors/channels/entities
- Framing and persuasion markers
- Evidence gaps and verification priorities

It is designed for OSINT and SOCMINT analysis with public-safe constraints.

## What it does well
- Produces structured narrative mapping quickly from noisy Telegram text.
- Distinguishes narrative/framing interpretation from factual verification.
- Adds confidence labels and practical follow-up checks.
- Uses public web sources only when verification is requested and tools are available.

## Important limitations
- No private Telegram scraping is assumed.
- No private channel access is assumed.
- No guaranteed continuous monitoring is assumed.
- If Telegram data cannot be accessed, analysis is limited to user-provided text/export.
- Narrative analysis is not equivalent to proving truth/falsehood.

## Required runtime files
- `system.md`
- `instructions.md`
- `output-template.md`
- `knowledge.md`
- `tools.md`

Load via `bootstrap.md` for runtime-safe operation.
