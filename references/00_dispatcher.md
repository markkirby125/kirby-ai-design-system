# Kirby AI Design System - Dispatcher

This skill deploys Tri-Part AI Design Systems and orchestrates DOM-native canvas layouts via the Paper.design MCP server and generative media via Higgsfield. It escapes the Flat Pixel Trap: monolithic AI image generators bake typography, elements, subjects, and backgrounds into flat raster pixels, so a single edit forces destructive prompt retries or manual masking. Here, every element stays an independently addressable layer.

## 📚 Module Index
- **Module 1: The Tri-Part AI Design System Architecture** (Business Context Wiki / Brand Guidelines Skill / Execution Toolstack) -> Read `./01_tri_part_architecture.md`
- **Module 2: Paper MCP Orchestration** (JSON-RPC canvas commands, layer isolation, asset slot injection) -> Read `./02_paper_mcp_orchestration.md`
- **Module 3: High-CTR Thumbnail Pipeline** (layered YouTube thumbnail production) -> Read `./03_thumbnail_pipeline.md`
- **Module 4: Multi-Page PDF Guide & Lead Magnet Pipeline** (vector PDF export SOP) -> Read `./04_pdf_guide_pipeline.md`
- **Module 5: MCP Security Guardrails** (Zero-Trust connector verification) -> Read `./05_mcp_security_guardrails.md`

## When to Use
- You are standing up an AI design system for a brand: context wiki, brand-guidelines skill, or MCP toolstack (Module 1).
- You are editing designs programmatically: swapping text, restyling layers, reflowing layouts, or injecting generated assets without regenerating the canvas (Module 2).
- You are producing YouTube thumbnails: isolated subject cutouts + bold DOM typography + shader backgrounds (Module 3). Full faceless-video production context: `../../kirby-yt-faceless-formula/SKILL.md`.
- You are generating multi-page branded PDF guides or lead magnets with direct vector export (Module 4). Copy frameworks and objection-demolition hierarchy: `../../kirby-text-first-cro/SKILL.md` Module 1.
- You are resizing one design across 16:9 / 1:1 / 9:16 without layout drift (Modules 2–4).
- You are auditing brand color tokens for WCAG 2.1 AA / RNIB contrast BEFORE canvas rendering: `../../kirby-accessible-contrast/SKILL.md`.
- You are verifying or updating the Paper MCP server / Higgsfield connector installation: Module 5 routes to `../../kirby-agent-security/SKILL.md` Module 1.

## When NOT to Use
- Pure image generation with no layered layout requirements — use a generative tool directly.
- Contrast auditing as a standalone task — that is `../../kirby-accessible-contrast/SKILL.md`'s skill; this system only consumes its verdicts pre-render.
