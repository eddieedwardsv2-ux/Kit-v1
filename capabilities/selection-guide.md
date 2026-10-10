# Capability selection guide

## Skill
Use when Claude already has the tools/data but needs a repeatable procedure, domain method or quality standard.

Examples:
- produce a specific weekly report;
- review a deliverable against a repeatable rubric;
- transform a known input into a known output.

A Skill changes **how Claude works**.

## MCP / connector
Use when Claude needs structured access to an external system or service.

Examples:
- GitHub;
- Notion;
- Slack;
- Figma;
- database;
- browser automation server.

An MCP changes **what Claude can reach**.

## Plugin
Use when a packaged extension conveniently combines Skills, commands, MCP servers, hooks or agents for a coherent job.

Use a plugin when the package is genuinely better than installing/configuring its pieces individually.

## CLI / deterministic tool
Use when the task can be executed reliably without model judgment.

Examples:
- Git;
- tests;
- formatters;
- build commands;
- converters.

Prefer this over an agent when the operation is deterministic.

## Hook
Use when an event should automatically trigger a deterministic action.

Examples:
- format after edit;
- run a proven check on stop;
- block/inspect a dangerous tool call.

A hook is lifecycle automation, not a knowledge store.

## Permission
Use for hard boundaries the model must not be allowed to cross.

## Subagent
Use when a task benefits from isolated context, specialist focus or safe parallelism.

Do not create permanent named departments by default.

## Rule
Use when instructions apply only to a path/file class rather than every task.

## Routine / schedule
Use only after a workflow has worked reliably and genuinely needs recurring execution.

## Decision test

```
Need knowledge/procedure? → Skill
Need external access? → MCP
Need a packaged combination? → Plugin
Need deterministic execution? → CLI/tool
Need automatic lifecycle action? → Hook
Need hard safety boundary? → Permission
Need isolated reasoning/context? → Subagent
Need path-specific instruction? → Rule
Need recurring execution? → Routine
```
