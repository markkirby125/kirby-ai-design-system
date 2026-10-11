# Module 3: High-CTR Thumbnail Pipeline

*Source: Brad Bonanno | AI Automation. Consumes: Business Context Wiki (Module 1), Paper MCP orchestration (Module 2), verified connectors (Module 5). Full faceless-video production flow: `../../kirby-yt-faceless-formula/SKILL.md`.*

### **3.1 Layered Thumbnail Architecture**
A high-CTR thumbnail is three independent layers, each editable in isolation:
1.  **Subject layer (asset slot):** isolated subject or face cutout with clean edges — generated/extracted via Higgsfield into the designated slot (Module 2 §2.4). Never baked into the background.
2.  **Typography layer (DOM text):** 2–6 words, set in the Brand Guidelines display weight; the promise or the tension of the video, not its title.
3.  **Background layer (GPU shader):** mesh gradients, liquid metal, or equivalent shader backgrounds rendered as a canvas layer — swappable without touching subject or type.

### **3.2 Production SOP**
1.  Pull the video's hook from the Business Context Wiki / script; derive ≤6 words of thumbnail copy (one idea, not a sentence).
2.  Assemble the three-layer scaffold on a 16:9 frame; subject occupies one golden-ratio zone, type the counter-zone, per the Brand Guidelines composition rules.
3.  Fill the subject slot: generate 3–5 candidate cutouts; pick by expression/clarity, not novelty.
4.  Fill the background slot: 3–5 shader variants; pick by contrast against BOTH subject and type (the pre-render contrast verdict from `../../kirby-accessible-contrast/SKILL.md` applies to type-on-background pairs).
5.  Reflow to 1:1 and 9:16 shorts variants (Module 2 §2.5) — same layers, adjusted safe zones.

### **3.3 CTR Iteration Loop**
*   Variant testing swaps exactly one layer at a time (background first — cheapest signal; then subject; type last). Because layers are isolated, a losing variant costs one slot fill, not a rebuild.
*   Keep a per-channel scoreboard in the wiki: thumbnail composition → CTR, so Part 1 accumulates taste data.
*   Banned moves: text the viewer cannot read at 120px wide; subject + type sharing a zone; shader backgrounds that fight the subject's edge contrast.

### **3.4 Handoff to kirby-yt-faceless-formula**
The faceless-formula skill owns video production end-to-end; this pipeline is its thumbnail station. When operating under `../../kirby-yt-faceless-formula/SKILL.md`, execute this module as `05_thumbnails_mcp_canvas.md` there directs.
