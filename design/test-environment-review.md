# Test-environment reduction review — baseline

Snapshot reviewed 2026-10-10.

Current `Test-environment-` contains approximately:
- 15 project Skills
- 5 specialist agents
- 23 Python/shell/JS scripts across `tools/` and research tooling
- 313 research-tree entries
- 68 audit-tree entries
- 29 system-tree entries
- 24 template-tree entries
- multiple dashboards, exports, learning material, brainstorms, side projects and historical compatibility rules

This is useful as a laboratory and evidence base. It is not an appropriate day-one beginner template.

## Keep as ideas, not necessarily implementation

- one small router;
- current priority;
- project-scoped situational context;
- source provenance;
- measurable finish conditions;
- verification;
- safe permissions;
- progressive capability growth.

## Do not copy into Kit-v1 by default

- raw transcript corpus;
- transcript-fetch/coverage scripts;
- creator brains;
- Charlie-specific agents (Architect, Quartermaster, Guardian, video tutor);
- dashboards/readers/maps;
- historical audit reports;
- compatibility migration language;
- parked projects/learning systems;
- custom handoff machinery unless native session continuity fails a test;
- custom context checker unless current Claude's own diagnostics leave a measured gap;
- weekly cadence/routines before there is a recurring proven workflow.

## Hypothesis

A modern beginner AI-OS can start with under ten meaningful files and zero custom agents/scripts/hooks, then grow through real use.

The comparison test is not folder count. Kit-v1 must equal or beat Test-environment on:
1. fresh-session routing;
2. correct context retrieval;
3. task completion against a defined finish condition;
4. verification quality;
5. permission safety;
6. context overhead;
7. recovery/continuity on a representative long task.

If a stripped system fails one of these, add the smallest mechanism that fixes the measured failure.
