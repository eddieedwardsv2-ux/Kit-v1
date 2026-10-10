# Current Anthropic / Claude Code evidence

Purpose: platform behaviour outranks older workflow advice.

Primary references reviewed 2026-10-10:

- Claude Code extension/features overview: use CLAUDE.md for always-active project context; Skills for on-demand knowledge/workflows; subagents for isolated context; hooks for automation; MCP for external connections. The docs recommend keeping CLAUDE.md under roughly 200 lines and adding extensions when a specific trigger appears.
- Effective context engineering: Claude Code uses a hybrid strategy — some guidance is loaded up front, while glob/grep/file tools retrieve additional context just in time. Anthropic's stated general advice is to do the simplest thing that works.
- Agent Skills: progressive disclosure. Skill name/description can be known up front while detailed instructions/resources load only when relevant. Deterministic code can live inside a skill without being loaded into the model context.
- Effective harnesses for long-running agents: compaction alone is insufficient; durable artifacts and incremental progress matter across context windows.
- Claude Code sandboxing/permissions: safety boundaries should be enforced by the runtime where possible instead of relying only on model obedience.
- Building effective agents: successful systems tend to use simple, composable patterns and ground progress in the environment.

Implication for Kit-v1:

`small always-on router → just-in-time context → native Skills/subagents/tools → deterministic verification/enforcement where needed`

Do not create a custom substitute for a native feature without a measured failure.
