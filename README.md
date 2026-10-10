# Kit-v1 — Claude-native AI OS experiment

A clean-room AI-OS template built top down for current Claude Code.

`Test-environment-` remains the laboratory. `Kit-v1` does not copy its Charlie-specific projects, creator corpora, dashboards, historical audits, named agents or custom orchestration.

## Current base

```
AGENTS.md
context/
  about-me.md
  current-focus.md
projects/
  README.md
.claude/
  settings.json
```

That is the candidate day-one system.

The `research/` and `design/` folders in this repository are evidence used while developing and testing the template. They are not automatically part of the finished beginner kit.

## Why there is no CLAUDE.md

Current Claude Code can read `AGENTS.md` directly when a project has no `CLAUDE.md`. We therefore use one shared instruction file rather than maintaining a compatibility bridge. Older Claude Code versions can be handled as a compatibility case only if testing shows we still need it.

## Evidence order

1. Current Anthropic / Claude Code documentation.
2. Boris Cherny's current Claude Code workflow.
3. Andrej Karpathy's current context, agent and verification guidance.
4. Nate Herk's modern Claude-native material.
5. Older material only where the principle still survives current platform capabilities.
6. Our additions only after a measured gap appears.

## Knowledge stays external

Raw creator transcripts live in `eddieedwardsv2-ux/eddie-ed`. A reusable AI-OS should not ship Charlie's research corpus. A user's own knowledge can be attached later when their work actually needs it.

## Promotion rule

This becomes the new template only if it equals or beats the old system on fresh-session routing, context retrieval, task completion, verification, safety and continuity while using materially less always-loaded context and less architecture.
