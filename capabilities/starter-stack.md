# Starter capability stack

This is the recommended **starting point**, not an instruction to install every option.

## Core — available to every Kit-v1 user

### Claude native
Use before adding anything:
- project instructions via `AGENTS.md`;
- Plan mode for substantial work;
- file search/read/edit and shell/CLI;
- native Skills support;
- subagents and worktrees when isolation/parallelism is useful;
- hooks and permissions for deterministic lifecycle/safety needs;
- web access/current documentation when available;
- built-in code review / simplify / testing capabilities where exposed by the current Claude Code version.

### Git + GitHub CLI
Git remains the project history and collaboration substrate. Prefer ordinary Git/CLI first when it is enough.

## Recommended official extensions

### GitHub — official MCP
**Status:** recommended for repo-centric users.

Use when Claude needs GitHub data/actions beyond local Git:
- issues;
- pull requests;
- repository search;
- review metadata;
- GitHub API actions.

Do not require it for simple local file or Git operations.

### Anthropic document skills
**Status:** recommended if the user regularly handles documents.

Official `anthropics/skills` bundle:
- PDF;
- DOCX;
- XLSX;
- PPTX.

Install the document bundle when document work is real, rather than reproducing these workflows in Kit-v1.

### Skill Creator
**Status:** add when the user has a repeated procedure worth encoding.

Do not pre-create many custom Skills. Use the official skill-creation guidance/tooling to turn proven repeated procedures into Skills.

## Strong optional extensions

### Notion — official integration
Use when Notion is genuinely the user's durable external knowledge/workspace.

### Playwright — Microsoft browser testing MCP
Use for:
- website interaction;
- screenshots;
- end-to-end tests;
- form/click flows;
- observable UI verification.

This is preferable to inventing a custom browser-test harness.

### Browser Use
Use when the job is general browser automation rather than software E2E testing.

### Canva
Use for design production/review when Canva is part of the user's workflow.

### Zapier
Use when the user needs broad cross-app actions and no narrower official integration is better.

### Slack
Use for team message/channel context when Slack is actually used.

### Figma
Use for design-to-code and design-system context when Figma is actually used.

### Render / Vercel
Use the deployment plugin matching the user's real deployment platform.

### HyperFrames
Use for programmatic video/motion workflows when video production is a demonstrated need.

## Not defaults

Do **not** preinstall these merely because they are powerful:
- large community skill packs;
- generic web-scraping stacks;
- RAG/vector databases;
- agent orchestration frameworks;
- multiple overlapping browser tools;
- multiple deployment plugins;
- multiple knowledge systems.

The best starter stack is the smallest set matching the user's actual work.
