# Kit-v1 — Claude-native AI OS experiment

A clean-room AI-OS template built top down for current Claude Code.

This repo deliberately does **not** copy the structure of `Test-environment-`. That repo is a laboratory containing Charlie-specific projects, research, scripts, dashboards and historical experiments. Kit-v1 starts from current platform capabilities and adds complexity only when a test proves it is needed.

## Design order

1. Current Anthropic / Claude Code documentation.
2. Boris Cherny's current Claude Code workflow and public guidance.
3. Andrej Karpathy's current context, agent and verification guidance.
4. Nate Herk's modern Claude-native material (roughly 20 primary videos).
5. Older material only where the principle still survives the current platform.
6. Our own additions only after a measurable gap appears.

## Base template

```
AGENTS.md
CLAUDE.md
context/
  about-me.md
  current-focus.md
projects/
  README.md
.claude/
  settings.json
research/
  source-map.md
  boris-cherny.md
  andrej-karpathy.md
  nate-modern.md
  anthropic-current.md
design/
  principles.md
  test-environment-review.md
```

Research and design files are development evidence for this experiment. A finished beginner template may be smaller.

## Knowledge is external

Raw creator transcripts are not part of the AI-OS template. Charlie's portable transcript archive lives in `eddieedwardsv2-ux/eddie-ed`. A future user's AI-OS should connect to that user's own knowledge sources instead of inheriting Charlie's corpus.

## Current status

Foundation research pass started 2026-10-10. No claim is made yet that this structure is the final template. It must beat the existing template on fresh-session routing, context size, task completion and verification before promotion.
