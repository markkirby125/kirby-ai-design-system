# Module 1: The Tri-Part AI Design System Architecture

*Source: Brad Bonanno | AI Automation — "My Entire AI Design System"*

### **1.1 The Three Parts**
A durable AI design operation separates persistent knowledge, formalized taste, and execution tooling. Collapsing them into prompts is why most AI design workflows degrade: context evaporates between sessions, and every session re-negotiates brand basics.

| Part | Artifact | Function |
|---|---|---|
| 1. Business Context Wiki | Persistent markdown repository | Brand background, audience personas, product specs, core messaging — the facts every asset must respect. Prevents repetitive prompting across sessions. |
| 2. Brand Guidelines Skill | Formalized agent skill | Design tokens, color ramps, typography hierarchy, font pairings, spacing scales, layout rules — taste encoded as invokable instructions. |
| 3. Execution Toolstack | Paper MCP + Higgsfield connectors | The agent's hands: DOM-native canvas manipulation and multi-model generative media (Modules 2–5). |

### **1.2 Part 1 — Business Context Wiki**
*   Structure: `wiki/brand.md` (origin story, positioning, voice), `wiki/personas/*.md` (one file per audience, with objections and desired outcomes), `wiki/products/*.md` (specs, pricing, proof points), `wiki/messaging.md` (value props, banned phrases, claims that must never appear), `wiki/toolstack.md` (registered connector versions, pins, and re-verification log — see Module 5 §5.3).
*   Invariant: the wiki holds **facts and claims**, not styling. If a statement would survive a rebrand, it belongs here; if not, it belongs in Part 2.
*   Every production run (Modules 3–4) reads the wiki first; an asset whose copy contradicts the wiki is a defect, not a variation.

### **1.3 Part 2 — Brand Guidelines Skill**
*   Encode as a formal agent skill (hollow shell): design tokens (color ramps with hex values, type scale with px/rem, spacing scale, radii, elevation), typography hierarchy and font pairings, composition rules (margin grids, safe zones per aspect ratio), and do/don't pairs.
*   **Contrast gate:** before any canvas render, the color tokens pass the WCAG 2.1 AA / RNIB audit in `../../kirby-accessible-contrast/SKILL.md`. Failing token pairs are fixed at the guidelines level — never patched per-asset, which reintroduces drift.
*   The skill is versioned with the brand: token changes are commits, and generated assets reference the token set they were built against.

### **1.4 Part 3 — Execution Toolstack**
*   **Paper.design MCP server:** renders layouts as native HTML/CSS with an interactive MCP endpoint — agents inspect, style, position, and swap individual DOM layers over JSON-RPC (Module 2).
*   **Higgsfield connector:** generates isolated subjects, 3D assets, textures, and cinematic clips across multiple underlying models under a single account; output lands in designated canvas slots while headers, badges, and copy stay crisp editable vector/DOM elements (Module 2 §2.4).
*   Both connectors are installed ONLY after passing the Zero-Trust verification in Module 5.

### **1.5 Standing Up a New System (Order of Operations)**
1.  Write the Business Context Wiki (Part 1) — no design work before facts.
2.  Formalize the Brand Guidelines Skill (Part 2) and run the contrast gate on its tokens.
3.  Verify and connect the toolstack (Part 3) via Module 5's registration gate.
4.  Prove the loop with one thumbnail (Module 3) and one PDF page (Module 4) before scaling.
