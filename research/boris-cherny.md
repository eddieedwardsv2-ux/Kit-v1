# Boris Cherny — current Claude Code workflow findings

Scope: public Claude Code guidance from Boris Cherny and reliable reproductions of his X threads/talks. Instagram search on 2026-10-10 did not surface a verifiable official technical corpus that added material beyond X/talks; do not claim Instagram coverage.

## High-confidence current patterns

1. **Vanilla Claude Code first.** His published setup is relatively light on custom orchestration and heavy on native Claude Code.
2. **Plan before execution.** Substantial sessions commonly start in Plan mode; refine the plan, then execute.
3. **Parallelism is normal, but separated.** He runs several local/web Claude sessions and uses worktrees/independent tasks rather than one giant shared context.
4. **One concise shared instruction surface.** His team keeps project guidance in a shared CLAUDE.md and feeds recurring mistakes back into it.
5. **Repeatable inner loops become reusable commands/Skills.**
6. **Subagents isolate recurring review/simplification/verification work.**
7. **Hooks handle lifecycle automation.** Example: PostToolUse formatting; Stop-style verification for long-running work.
8. **Permissions remove needless prompts without removing boundaries.**
9. **MCP connects external systems; it is not a substitute for task procedure.**
10. **Verification is the largest quality multiplier.** Give Claude tests, UI checks or another observable feedback loop.
11. **Newer hidden-feature guidance adds loops, lifecycle hooks, worktree parallelism and large fan-out.** These are capabilities to use when the task warrants them, not reasons to prebuild a large OS.
12. **Cross-device/cloud sessions reduce the need for home-grown handoff infrastructure in some workflows.**

## What this changes versus Test-environment-

- Do not encode every capability in the root router.
- Do not build custom orchestration merely because several agents exist.
- Prefer native Plan mode, Skills, subagents, hooks, permissions and worktrees.
- Keep verification, but make it task-specific and observable rather than equating a structural audit with correctness.
- A hook is useful when an event must reliably trigger an action; it should not become a second hidden prompt architecture.

## Source notes

Primary/near-primary material used:
- Boris Cherny's X setup thread as reproduced with direct X attribution (13 workflow tips).
- Boris Cherny March 2026 X thread on under-used Claude Code features (loops, hooks, worktrees, fan-out).
- Anthropic Claude Code Live / best-practice material featuring the Claude Code team.

Secondary reproductions are used only where X blocks full retrieval; claims should be checked against current Claude docs before becoming template behaviour.
