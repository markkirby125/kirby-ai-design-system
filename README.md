# Kirby AI Design System

[![Kirby Skills Collection](https://img.shields.io/badge/Kirby_Skills-Collection-blue?style=flat-square&logo=github)](https://github.com/markkirby125/kirby-skills-collection)

You are using AI to produce design assets — YouTube thumbnails, lead-magnet PDFs, social creative — and every single edit costs you a full regeneration. You ask for the headline moved two pixels left and the model hands you a new image with a different face, different copy, and a different background. Ten prompt retries later you are masking pixels in Photoshop anyway.

**This is the Flat Pixel Trap.** Monolithic AI image generators (Midjourney, DALL-E, standard Flux) bake typography, graphical elements, subjects, and backgrounds into flat raster pixels. Once baked, nothing is individually editable — and every "small change" is destructive.

**The Solution:** The `kirby-ai-design-system` skill deploys the Tri-Part AI Design System — a persistent Business Context Wiki, a tokenized Brand Guidelines skill, and a DOM-native execution toolstack (the Paper.design MCP canvas plus the Higgsfield multi-model generative engine). Because Paper renders layouts as native HTML/CSS and exposes an MCP server, your AI agent inspects, styles, positions, and swaps individual canvas layers over JSON-RPC with zero visual degradation. Text stays crisp vector DOM. Subjects arrive as isolated generated assets injected into designated slots. A losing thumbnail variant costs one slot fill — not a rebuild.

## What's Inside

- **Module 1 — Tri-Part Architecture:** Business Context Wiki (facts, personas, messaging, toolstack log), Brand Guidelines Skill (tokens, type scale, spacing, composition rules), and the Execution Toolstack — with the standing order of operations for standing up a new brand system.
- **Module 2 — Paper MCP Orchestration:** the layer-isolation doctrine and command set (`canvas.inspect`, `layer.setText/setStyles/setAsset`, `frame.reflow`), asset-slot injection from Higgsfield, untrusted-canvas prompt sanitization, and 16:9 / 1:1 / 9:16 reflow without layout drift.
- **Module 3 — High-CTR Thumbnail Pipeline:** the three-layer thumbnail (isolated subject slot / bold DOM typography / GPU shader background), the one-layer-at-a-time CTR iteration loop, and the per-channel scoreboard that accumulates taste data in the wiki.
- **Module 4 — Multi-Page PDF Guide & Lead Magnet Pipeline:** page archetypes and master frames, reusable callout blocks, copy-first production, direct vector PDF export, and one-source/many-brands re-skinning via token sets.
- **Module 5 — MCP Security Guardrails:** Zero-Trust connector verification routing (`../../kirby-agent-security` Module 1), version-pin + build-hash session checks, tool-allowlist discipline, and re-verification triggers.

## Ecosystem Integration

- `kirby-agent-security` Module 1 — pre-install verification specs for both connectors (this system refuses to connect unverified ones).
- `kirby-accessible-contrast` §7 — pre-render PASS/FAIL/BANNED verdicts on brand token pairs, including shader-gradient extremes.
- `kirby-text-first-cro` §14 — the copy doctrine (objection demolition, contrast tiers, CTA/price gating) that drives Module 4's page sequence.
- `kirby-yt-faceless-formula` `05_thumbnails_mcp_canvas.md` — this system's thumbnail station inside a faceless-video production run.

## 🪄 The Magic Prompt

Copy and paste this into any AI coding app (Cursor, Windsurf, Claude Code, Grok, Kimi, Reasonix):

```markdown
@agent Install the Kirby AI Design System skill from: https://github.com/markkirby125/kirby-ai-design-system
1. Read `SKILL.md` and `references/` from the repository.
2. Place into your environment's skills/rules directory preserving the dispatcher structure.
3. Confirm when installation is complete.
```

## Manual Installation

- **Cursor**: Save `SKILL.md` to `.cursor/rules/kirby-ai-design-system.mdc` and copy `references/`
- **Windsurf**: Save `SKILL.md` to `.windsurfrules` and copy `references/`
- **Antigravity / agents dir**: Clone this repository directly into `~/.agents/skills/kirby-ai-design-system`

## Requirements

- The [Paper.design](https://paper.design) desktop app with its MCP server enabled, and a Higgsfield account — **both installed only after passing the Zero-Trust verification in `kirby-agent-security` Module 1**.
- An AI agent environment that speaks MCP (Cursor, Windsurf, Claude Code, Antigravity, or equivalent).

## Tech Stack

- **Format**: Markdown / YAML (Hollow Shell skill)
- **Compatibility**: Antigravity, Claude Code, Cursor, Windsurf, Grok, Kimi, Reasonix
- **Tested**: `tests/test_new_skills_oct2026.py` in the [kirby-skills](https://github.com/markkirby125/kirby-skills) monorepo (36 tests: structure, routing, WCAG math, sanitizer, refusal gate, integration)

---

## Repo Details

* **Repository**: [https://github.com/markkirby125/kirby-ai-design-system](https://github.com/markkirby125/kirby-ai-design-system)
* **Parent Collection**: [kirby-skills](https://github.com/markkirby125/kirby-skills)
* **Master Directory**: [kirby-skills-collection](https://github.com/markkirby125/kirby-skills-collection)
* **Category**: Design / Agent Ops
* **Skill Author**: William Fitzpatrick (Kirby Skills Library)
* **Source Video**: "My Entire AI Design System" — Brad Bonanno | AI Automation
* **Direct Video URL**: https://youtu.be/z0j6oouLG3g

## Attribution & Provenance

* **Source Framework**: Brad Bonanno's Tri-Part AI Design System (Business Context Wiki / Brand Guidelines / Paper MCP + Higgsfield toolstack) and the Flat Pixel Trap analysis.
* **Derived Doctrine**: DOM-native layer isolation, multi-model generative isolation, high-CTR thumbnail architecture, and multi-page vector PDF production are documented from the source video and extended with Zero-Trust connector security (`kirby-agent-security`), RNIB/WCAG pre-render gates (`kirby-accessible-contrast`), and text-first CRO page doctrine (`kirby-text-first-cro`).
