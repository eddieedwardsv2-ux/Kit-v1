# Claude-native AI OS v0.1

## Goal

Build the smallest project structure that lets a fresh Claude session understand the operator, find the current work, complete a real task and verify the result without carrying unnecessary architecture.

## First-principles model

```
small persistent instructions
        ↓
current task
        ↓
retrieve only relevant context
        ↓
use native Claude capability
        ↓
perform work
        ↓
verify observable outcome
        ↓
persist only information worth carrying forward
```

## Day-one components

### 1. `AGENTS.md`
Purpose: instructions that matter in nearly every session plus routes to situational context.

Why one file:
- Current Claude Code can read AGENTS.md directly.
- Codex and other compatible tools can also use it.
- A duplicate CLAUDE.md would create another maintenance surface without adding day-one value.

### 2. `context/about-me.md`
Purpose: durable operator facts that materially change how the system should work.

It is not:
- a session log;
- a transcript archive;
- a general notes dump;
- a place for every preference Claude can learn automatically.

### 3. `context/current-focus.md`
Purpose: one short statement of the active priority, finish condition and deliberately parked work.

It prevents historical notes from competing with current intent.

### 4. `projects/`
Purpose: situational context and deliverables for outcomes that need their own workspace.

Project-specific knowledge stays here instead of being promoted to the root instructions.

### 5. `.claude/settings.json`
Purpose: hard technical boundaries that should not depend on model obedience.

Initial use is deliberately narrow: block destructive Git/shell operations. Add more only when a real risk is demonstrated.

## Components that are deliberately absent on day one

### Skills
Add a Skill when the same multi-step procedure recurs or when task-specific instructions are too detailed for the root instructions.

### Subagents
Add a subagent when isolated context, specialist review or safe parallel work materially improves a task. Do not create permanent named roles in advance.

### Hooks
Add a hook when an event should deterministically trigger an action, for example formatting after a write or running a proven check before completion.

### Rules
Add a path-scoped rule when instructions apply only to a specific file type or directory.

### Connections / MCP
Add external connections only when a real workflow needs external data or actions.

### Knowledge layer
Attach a compact derived knowledge pack when normal project files stop being enough. Keep raw source corpora external and traceable.

### Retrieval / RAG
Do not add semantic retrieval until normal files, indexes and search demonstrate a measurable retrieval failure.

### Schedules / routines
Do not schedule a process before the manual/native workflow has worked reliably.

## Mechanism selection

When a need appears:

```
Can Claude already do it natively?
  yes → use native feature
  no
   ↓
Can a deterministic command/workflow do it?
  yes → use that
  no
   ↓
Is it a repeatable task procedure?
  yes → Skill
  no
   ↓
Does it need isolated context / parallel work?
  yes → subagent
  no → solve in the main session
```

Safety is separate:

```
Behavioural guidance → AGENTS.md / rules
Hard prohibition → permissions
Automatic event response → hook
```

## Knowledge architecture

For Charlie:

```
eddie-ed
  raw immutable transcripts
        ↓
optional derived knowledge packs
        ↓
Kit-v1 / future project reads only what the task needs
```

For another user, the same OS points to their own sources. The template itself contains no Nate, Boris, Karpathy or Charlie corpus.

## Why this is different from Test-environment-

Test-environment accumulated architecture while exploring what was possible. It currently contains many skills, agents, scripts, research files, dashboards and historical mechanisms.

Kit-v1 starts from the opposite direction:

```
nothing is present until it earns its place
```

The old repo is evidence and a regression target, not the structure to copy.

## Open questions to prove

1. Does direct AGENTS.md loading work reliably in the Claude Code versions/environments Charlie actually uses?
2. Can a fresh session answer routing questions correctly with only the two context files?
3. Can a real project be completed without a custom handoff, audit agent or routing hierarchy?
4. Which verification mechanisms are genuinely missing after using Claude's native tests, browser feedback, prompt audit and normal project checks?
5. Does long-running work expose a continuity gap that requires one additional durable artifact?
