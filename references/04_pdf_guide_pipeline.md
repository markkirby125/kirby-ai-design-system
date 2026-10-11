# Module 4: Multi-Page PDF Guide & Lead-Magnet Pipeline

*Source: Brad Bonanno | AI Automation. Copy architecture (objection-demolition hierarchy, frameworks): `../../kirby-text-first-cro/SKILL.md` §14 (DOM-native lead-magnet layouts).*

### **4.1 Why DOM-Native Beats Document Generators for Lead Magnets**
Multi-page technical guides produced in monolithic generators couple content, layout, and branding into one artifact — every brand change re-opens every page. In this pipeline, pages are DOM frames: brand tokens restyle the whole guide by changing one layer class, callout blocks are reusable layer compositions, and export is direct vector PDF (type stays selectable, file sizes stay small).

### **4.2 Guide Architecture**
*   **Page archetypes** (compose any guide from these): cover, agenda/TOC, concept spread, data/callout page, checklist page, CTA/closing page.
*   **Master frame:** one 16:9 (or A4) master per archetype holding fixed zones — header band, body grid, footer band, page number slot. Pages instantiate archetypes; they never free-draw.
*   **Callout blocks:** pre-built layer compositions (warning, proof-stat, quote, action) placed into the body grid; copy slots inside them are DOM text (Module 2 §2.3).

### **4.3 Production SOP**
1.  Pull the offer, audience persona, and objection list from the Business Context Wiki.
2.  Structure the guide's narrative per `../../kirby-text-first-cro/SKILL.md` §14 (copy-first: every page exists to demolish an objection or deliver a proof point — no filler pages).
3.  Draft page copy into the copy slots BEFORE styling (text-first invariant; styling never rescues weak copy).
4.  Instantiate archetypes page-by-page; place callouts; fill asset slots via Higgsfield only where an image earns its space (diagrams, examples — not decoration).
5.  Run the contrast gate on the rendered token pairs (headers-on-band, body-on-page) per `../../kirby-accessible-contrast/SKILL.md`.
6.  Export direct vector PDF; verify text is selectable and page count matches the archetype manifest.

### **4.4 Batch Variants**
Because pages are frames and brands are tokens: the same guide re-skins per brand line by swapping the token set (Tri-Part Part 2), and re-formats between screen (16:9) and print (A4) via archetype masters. One content source, many branded artifacts — the consistency mechanism is structural, not discipline.
