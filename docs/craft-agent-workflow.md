# Craft Agent Workflow

## Purpose

Craft Agent turns a merged public-safe repository spec into an Actual Armor marketplace agent.

## Inputs

- agent slug
- merged public repo path
- raw GitHub `bootstrap.md` URL
- metadata
- title
- description
- category
- expected runtime behavior
- tool configuration notes
- publish mode: `draft` / `update` / `publish`

## Responsibilities

Craft Agent should:

1. Open AA marketplace admin or creation UI.
2. Create or update the agent shell.
3. Add public-facing metadata.
4. Configure thin shell instructions.
5. Configure HTTP bootstrap loading.
6. Save draft or publish depending on approved mode.
7. Return marketplace URL/ID.
8. Provide screenshots or evidence where available.
9. Produce a craft report.

## Current Manual-Assisted Mode

Until Playwright + Google Auth work is unblocked by CTO:

- Product/Codex produces a creation packet.
- Human/Crafter manually creates or updates the agent in AA UI.
- Human returns marketplace URL, screenshots, and notes.
- Craft status is patched manually or through Codex.

## Future Automated Mode

After CTO unlocks Playwright + Google Auth:

- OpenWebUI automation triggers Craft Agent.
- Craft Agent uses Playwright to create/update the marketplace agent.
- Human approves publish/update.
- Craft Agent returns a structured report.

## Output Format

Use this structured report:

```text
Agent:
Marketplace URL:
Marketplace ID:
Mode: created / updated / draft / published
Bootstrap URL:
Craft Status:
Evidence:
Known Issues:
Next Step:
```

## Failure Modes

- `blocked_by_auth`
- `blocked_by_ui_change`
- `blocked_by_missing_repo_spec`
- `blocked_by_missing_bootstrap_url`
- `blocked_by_tool_config`
- `blocked_by_publish_approval`
