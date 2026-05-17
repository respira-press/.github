<p align="center">
  <img src="https://raw.githubusercontent.com/respira-press/.github/main/profile/cover.png?v=1779023145" alt="Respira for WordPress" width="100%" />
</p>

# [Respira for WordPress](https://respira.press)

The independent AI infrastructure layer for WordPress. Open-source tooling that lets AI coding agents safely edit live sites across 12 page builders, plus a free plugin in the WordPress.org pipeline.

Respira solves a specific problem: AI coding assistants can generate WordPress edits now, but they do not natively understand the page builder data structures those sites depend on. Divi shortcodes, Elementor JSON, Bricks elements, Gutenberg blocks, Oxygen meta. Respira reads each of them, edits at the right granularity, and undoes itself if anything looks off after render. Snapshot before every write. Validation after. Privacy-preserving by design (Respira does not read or transmit site content, only operation outcomes).

## Live now

A snapshot from May 17, 2026. Live numbers, refreshed every 60 seconds, at [respira.press/live](https://respira.press/live).

| | |
| --- | --- |
| Connected WordPress sites | **823** |
| Lines of AI-generated code shipped | **3,839,111** (target 4,000,000) |
| Pages edited / created | 29,080 / 1,793 |
| Posts edited / created | 5,134 / 1,842 |
| MCP events tracked | 51,276 since 2026-03-07 |
| Page builders covered | 12 (Elementor, Divi, Gutenberg, Bricks, WPBakery, Breakdance, Beaver Builder, Oxygen, Flatsome, Brizy, Thrive Architect, plus generic) |
| MCP tools available | 172 |
| Agent skills available | 26 (610 installs across 90 sites) |
| Latest Respira for WordPress | v6.7.5, shipped 2026-04-26 |

Top AI clients by event volume: Claude Code (86%), Cursor (6%), Codex (5%), Claude Desktop (2%), Claude Cowork (<1%), Gemini (<1%).

## Products

1. **[Respira for WordPress](https://respira.press)** (paid, v6.7.5) — the safety layer for AI-driven edits. Snapshot before every write, render validation after, one-click rollback. The reason agencies and solo developers pay.
2. **[Inhale: MCP Abilities](https://respira.press/inhale-mcp-abilities)** (free, v0.1.1, shipped 2026-05-16) — settings page for the WordPress MCP server. Replaces the `wp_register_ability_args` filter workaround with a UI. First Respira plugin in the wp.org plugin directory pipeline.
3. **[Respira CLI](https://www.npmjs.com/package/@respira/cli)** (open source) — local CLI for WordPress builds in AI coding agent workflows. Complementary to WP-CLI, not a replacement.
4. **[Agent Skills for WordPress](https://github.com/respira-press/agent-skills-wordpress)** (open source) — 26 skills that run in Claude Code, Codex, Cursor, Antigravity, any agent that supports the Skills + MCP shape. 610 installs across 90 sites.
5. **[Respira MCP Server](https://github.com/respira-press/respira-wordpress-mcp)** (open source) — 172 MCP tools. Install with `npx -y @respira/wordpress-mcp-server --setup`.
6. **[Cowork Plugin for WordPress](https://respira.press/cowork)** — Anthropic Cowork integration for editing WordPress across the same 12 page builders, from inside Claude Desktop.
7. **Respira Add-on SDK** — SDK for MCP-aware WordPress add-ons. First-party (Forms, SEO, Newsletter, WooCommerce) and partner add-ons build on this.
8. **Respira for WordPress Lite** (in development) — the wp.org-compliant free version of the main product.
9. **[Documentation and Community](https://github.com/respira-press/Respira.press-Documentation-and-Community)** — the docs source for respira.press/docs.

## Recently shipped

- **2026-05-16** — Inhale: MCP Abilities v0.1.0, hardened to v0.1.1 the same day.
- **2026-05-16** — Pull request [WordPress/mcp-adapter#184](https://github.com/WordPress/mcp-adapter/pull/184) opened against the canonical WordPress MCP Adapter, addressing issue #183 with a first-party settings page.
- **2026-04-26** — Respira for WordPress v6.7.5 released.

## How Respira works

- **Duplicate-first.** Every write happens on a snapshot of the target page or post. The original is never touched until the snapshot validates.
- **Render validation.** After each write, Respira loads the rendered output and compares against the expected shape. If the result looks wrong, the snapshot is discarded.
- **Typed property validators.** Each page builder has a typed schema. Edits that would produce invalid builder data are rejected at the validator layer, not at the render layer.
- **One-click rollback.** Any operation can be undone from the WordPress admin. Snapshots are kept until rolled back or explicitly cleared.
- **Privacy-preserving.** Respira does not read or transmit WordPress content. Only operation outcomes (success / failure, latency, tool name) are tracked via signed tool events, deduplicated by operation ID.

## Built by

Respira is built and maintained by [@webmyc](https://github.com/webmyc) (Mihai Dragomirescu), solo founder, based in Brașov, Romania.

## Links

- Site: [respira.press](https://respira.press)
- Live telemetry: [respira.press/live](https://respira.press/live)
- Docs: [respira.press/docs](https://respira.press/docs)
- X: [@respira_press](https://x.com/respira_press)
- LinkedIn: [showcase](https://www.linkedin.com/showcase/respira-press/)
- Email: mihai@respira.press

<p align="center">
  <img src="https://raw.githubusercontent.com/respira-press/.github/main/profile/storefront.jpg" alt="Respira for WordPress storefront, illustrated" width="100%" />
</p>

*One breath. AI infrastructure for WordPress.*
