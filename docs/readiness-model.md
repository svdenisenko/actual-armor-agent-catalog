# Readiness Model

This model is the canonical readiness framework for public marketplace agents.

## Levels

### 1) `metadata_only`
- Name/description/source metadata exists.
- Prompt/tool/instruction files are missing or intentionally not yet exported.
- Not launchable for promotion.

### 2) `imported_draft`
- Raw imported artifacts exist from source export.
- Content is unrefined and may not yet meet public-safe spec quality.

### 3) `full_spec_draft`
- Core spec files exist (system/instructions/output/tests/knowledge/tools) in draft form.
- Requires technical and policy review.

### 4) `runtime_load_tested`
- Agent spec can be loaded by supported runtime shell via repository artifacts.
- Confirms packaging/loading, not quality claims.

### 5) `qa_smoke_tested`
- QA has executed baseline smoke tests and documented outcomes.
- Failing or partial outcomes must block promotion progression.

### 6) `soft_launch_candidate`
- Meets minimum quality and policy standards for limited release.
- Still requires controlled rollout expectations.

### 7) `promotion_ready`
- Eligible for broad marketing/landing-page promotion.
- **Only a designated human owner can approve `promotion_ready`.**
- Automation can recommend but cannot self-approve this state.

## Governance Rules
- Do not up-level readiness solely from metadata presence.
- `metadata_only` agents must remain clearly labeled in indexing and planning docs.
- Sensitive agents require stricter gating before any promotion state.
