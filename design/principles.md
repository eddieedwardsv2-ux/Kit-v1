# Kit-v1 design principles

1. **Native before custom.** Use current Claude Code features before recreating them in Markdown, scripts or agents.
2. **Small persistent context.** Always-loaded instructions are expensive attention. Route to detail instead of storing detail at the root.
3. **Progressive disclosure.** Task-specific procedure belongs in Skills; file-specific guidance in scoped rules; large independent work in subagents.
4. **External knowledge, internal pointers.** The OS does not need to carry the user's full source corpus.
5. **Declarative finish conditions.** Give agents goals and observable success criteria; avoid procedural micromanagement unless the procedure itself matters.
6. **Verification before autonomy.** Raise autonomy where success can be checked mechanically; keep human judgment for taste, ambiguity and irreversible actions.
7. **Deterministic enforcement outside prompts.** Permissions and hooks are stronger than asking the model to remember a prohibition or lifecycle action.
8. **Parallelism needs isolation.** Parallel workers should have separate tasks/state/worktrees; shared integration remains explicit.
9. **Architecture must be earned.** No folder, agent, hook, script, knowledge layer or retrieval system exists merely because a template author can imagine needing it.
10. **Fresh-session evidence beats documentation.** The template passes only when a new session routes, executes and verifies representative work without hidden guidance.
