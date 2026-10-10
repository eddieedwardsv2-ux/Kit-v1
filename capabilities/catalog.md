# Curated capability catalog

Reviewed: 2026-10-10

This is intentionally selective. The goal is not to mirror the marketplace.

| Capability | Type | Source/trust | Use when | Default? |
|---|---|---|---|---|
| GitHub | MCP/plugin | Official GitHub integration in Anthropic official marketplace | Repo issues, PRs, search and remote actions | Recommended for repo-centric users |
| document-skills | Skills bundle | Anthropic `anthropics/skills` | PDF, Word, Excel, PowerPoint | When document work exists |
| skill-creator | Skill | Anthropic example skills | Turn proven repeated workflow into a Skill | When first custom Skill is needed |
| Playwright | MCP/plugin | Microsoft, listed by Anthropic | Browser E2E testing, screenshots, UI verification | Optional |
| Browser Use | plugin | Anthropic marketplace | General website/browser workflows | Optional; avoid overlap with Playwright unless justified |
| Notion | MCP/plugin | Official Notion integration in Anthropic marketplace | External knowledge/docs/databases | Optional |
| Slack | MCP/plugin | Official Slack integration in Anthropic marketplace | Team context/messages | Optional |
| Figma | MCP/plugin | Official Figma integration in Anthropic marketplace | Design context and design-to-code | Optional |
| Canva | MCP/plugin | Canva integration in Anthropic marketplace | Create/review/resize branded designs | Optional |
| Zapier | MCP/plugin | Zapier official integration | Broad actions across many apps | Optional, when narrower integration is unavailable |
| Render | plugin | Render integration in Anthropic marketplace | Deploy/debug/monitor Render apps | Platform-specific |
| Vercel | plugin | Vercel integration in Anthropic marketplace | Deploy/manage Vercel apps | Platform-specific |
| HyperFrames | plugin | Anthropic marketplace | Programmatic motion/video generation | Media-specific |
| chrome-devtools-mcp | MCP/plugin | Chrome DevTools integration in Anthropic marketplace | Browser inspection, performance/network debugging | Developer-specific |
| desktop-commander | MCP/plugin | Anthropic official marketplace listing | Desktop/process/file operations beyond native environment | Only if native local tools are insufficient |

## Official marketplaces worth knowing

- Anthropic official plugins: `anthropics/claude-plugins-official`
- Anthropic-reviewed community marketplace: `anthropics/claude-plugins-community`
- Anthropic Agent Skills: `anthropics/skills`
- Anthropic knowledge-work plugins: `anthropics/knowledge-work-plugins`

## Installation principle

Kit-v1 should expose the catalog, not silently install third-party access.

Connections usually require authentication and may grant real external permissions. The user should deliberately connect only the services they use.

## Maintenance

A capability stays in this catalog when:
- it has a clear non-overlapping job;
- its source remains maintained/trusted;
- current Claude does not make it redundant;
- it still offers measurable value.

Remove or demote it when native Claude replaces it or a simpler official option becomes better.
