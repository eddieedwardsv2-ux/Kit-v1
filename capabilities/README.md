# Capabilities

Kit-v1 is small by default, but it is not capability-blind.

This folder is the self-contained selection guide for Skills, MCP servers, plugins and tools that can extend the base Claude system. A new user does **not** need access to any other repository.

## Selection rule

```
Can base Claude do it well?
  yes → use base Claude
  no
   ↓
Is there an official / first-party extension for the exact job?
  yes → prefer it
  no
   ↓
Use a well-maintained community extension only after checking trust, permissions and fit.
```

Do not install everything. Install the smallest capability that solves a real repeated need.

## Files

- `starter-stack.md` — the recommended default and optional stack.
- `selection-guide.md` — Skill vs MCP vs plugin vs hook vs subagent vs script.
- `catalog.md` — curated current extensions and when to use them.

## Trust order

1. Claude native capability.
2. Anthropic-maintained Skill/plugin.
3. Official integration from the service vendor.
4. Anthropic-reviewed community marketplace entry.
5. Other community tooling only after explicit review.

The Anthropic community plugin marketplace is security-scanned and reviewed for distribution, but that is not the same as proving the plugin is necessary or correct for every user.
