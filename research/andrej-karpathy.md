# Andrej Karpathy — current agent/context findings

Scope: Karpathy's public X threads plus existing first-party talks/videos already represented in Charlie's research archive. Instagram search on 2026-10-10 did not surface a verifiable official technical corpus that added unique architecture guidance.

## Important newer findings

### Context engineering
Karpathy argues that the engineering problem is not simply writing a better prompt; it is filling the context window with the right information for the next step. Too little context fails; too much irrelevant context can also reduce performance.

Implication: Kit-v1 should keep always-loaded instructions small and make retrieval/progressive disclosure a first-class design constraint.

### Agent coding is a phase change, not perfect autonomy
In his 2026 Claude-coding notes, Karpathy describes moving from mostly manual coding to mostly agent coding, but warns that modern agents fail through subtle conceptual errors, silent assumptions, over-complication and unrelated edits.

Implication: give agents goals and success criteria, but keep strong verification and scoped changes.

### Declarative goals beat micromanaged steps
He highlights agents' tenacity and recommends giving them success criteria and letting them loop, including tests-first or browser-feedback loops.

Implication: project tasks should define observable finish conditions rather than enormous procedural prompts.

### The unit of work is moving upward
Karpathy argues the future development environment's basic unit is increasingly the **agent**, not the file.

Implication: isolated workers and parallel work matter, but coordination/review becomes a higher-level human/system responsibility.

### Build for agents
Karpathy's newer X guidance emphasizes agent-accessible surfaces: Markdown documentation, CLI, GitHub CLI, Skills and MCP. Legacy CLIs are valuable because agents can combine them easily.

Implication: prefer simple text/files/CLI/API surfaces over bespoke graphical control layers.

### LLM knowledge bases
Karpathy's July 2026 knowledge-base workflow is especially relevant:
`raw immutable sources → LLM-maintained Markdown wiki → indexes/backlinks/concepts → CLI tools/Q&A → health checks`.
He reports that at his scale (~100 wiki articles / ~400K words), normal file/index navigation remained effective enough that he did not need sophisticated RAG.

Implication: Charlie's raw transcript archive should remain external evidence. A working AI-OS can attach a compact derived knowledge pack and follow source pointers back to raw evidence when required.

### Verification and autonomy
Across his coding/agent material: use the highest autonomy where success is objectively checkable; keep humans in the loop for judgment/taste/irreversible decisions. A demo passing once is not evidence of robust reliability.

## Useful primary X threads

- Context engineering over prompt engineering — status 1937902205765607626.
- Claude coding notes / 80% agent coding — status 2015883857489522876.
- IDE → agent as higher-level unit — status 2031767720933634100.
- LLM Knowledge Bases — status 2039805659525644595.
- Build-for-agents / CLI guidance — 2026 X post captured in the research sweep.

## Existing external audit

The public `benfngu/karpathy-claude-skills` project independently audited a larger Karpathy source set and reports 66 verified claims, 1 contradicted and 4 unverifiable in its provenance review. It is useful as a discovery map, not as authority over Karpathy's primary material.
