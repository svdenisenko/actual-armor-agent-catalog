# Agent Specification Schema

Each agent folder is expected to include the following files:
- `agent.yaml`
- `bootstrap.md`
- `system.md`
- `instructions.md`
- `output-template.md`
- `knowledge.md`
- `tools.md`
- `tests.md`
- `changelog.md`

## Expected Metadata Fields (`agent.yaml`)
- `id`
- `name`
- `description`
- `visibility`
- `category`
- `target audience`
- `use case`
- `user benefit`
- `required tools`
- `safety notes`
- `readiness fields`
- `version`


## Tool Naming Compatibility
- `required_tools` should use runtime-native tool names (for Actual Armor URL fetching, use `http`).
- When needed, add `required_tools_note` to clarify cross-runtime aliases (for example: `http` means HTTP(S) URL-fetch tool).
