# Sloppi v2.0 Design Reasoning Framework

Design reasoning is the disciplined creative and engineering process by which a coding agent translates a product brief into an **unmistakable, original visual system**.

Coding agents fail at frontend design for two opposite reasons:
1. **Unthinking Autopilot**: Jumping straight from prompt to `bg-slate-900 text-white rounded-xl p-6`, producing generic purple/blue SaaS slop.
2. **Bureaucratic Over-Compliance**: Following rigid token rules so conservatively that every interface turns into the same flat `1px`-bordered wireframe with `Inter` and monospace labels.

Sloppi v2.0 enforces a **6-stage Creative Director & Engineering reasoning pipeline**:

```
1. Product, Persona & Category Subversion Analysis
               │
               ▼
2. Live Reference Inspection & Evidence Extraction
               │
               ▼
3. 3-Direction Creative Divergence (A vs. B vs. C)
               │
               ▼
4. Pre-Implementation Originality Gate & Design Thesis
               │
               ▼
5. Expressive Art Direction & Semantic Token System
               │
               ▼
6. Visual-First Primary Composition Prototype
```

---

## Stage 1: Product, Persona & Category Subversion Analysis

Before choosing a font or color, interrogate four dimensions:

### 1. Operational Stakes & Emotional Register
- **Low Stakes / Expressive**: Creative tools, consumer social, music/audio, culture, gaming. *Demands kinetic motion, bold chromatic tension, unconventional geometry, and playful tactility.*
- **Medium Stakes / High-Craft Productivity**: Collaborative workspaces, design tools, knowledge systems, commerce. *Demands tactile ergonomics, spatial clarity, warm or distinctive surface materiality, and fluid state choreography.*
- **High Stakes / Mission-Critical**: Developer infrastructure, financial ledgers, security, clinical systems. *Demands high legibility and precision—but **never** excuse boredom in the name of "utility." Distinguish through archival Swiss typography, cartographic schematics, or industrial hardware craft rather than generic dark-mode boxes.*

### 2. Category Cliché Identification (What to Subvert)
Ask explicitly: **"What do 90% of AI-generated websites in this category look like?"**
- *Fintech cliché*: Dark blue/purple cards OR sterile white-and-navy `1px` boxes with `Plus Jakarta Sans`.
- *Dev-tool cliché*: `#0b0d13` dark canvas + neon green `#00d084` + split CLI box + 3-card or 8+4 bento grid.
- *AI tool cliché*: Glowing violet/cyan mesh orbs, sparkles, and centered pill badges.
Write down the category cliché first so you can **deliberately subvert it**.

### 3. The 5-Second Interactive Proof
How does the user *experience* the product's core mechanism within 5 seconds of landing—without reading three paragraphs of marketing text?
- Design an **interactive instrument, live canvas, scrubbable timeline, morphing schematic, or tactile workbench** as the centerpiece of the primary viewport.

---

## Stage 2: Live Reference Inspection & Evidence Extraction

Consult [research/source-routing.md](../research/source-routing.md) and [references/source-registry.md](../references/source-registry.md) to route by design question and inspect 2–4 actual examples or clips (opening deep links rather than thumbnails).
- Record **deep links**, **observed composition/behavior** (and for motion: **trigger, what moves, what stays anchored, how it settles**), **adaptable principle**, **where it serves this product**, and mark `[INFERRED]` details.
- Never copy a single site's skin or auto-adopt a demo library; synthesize orthogonal mechanics across references.

---

## Stage 3: 3-Direction Creative Divergence

Generate **3 distinct creative concepts** (`Direction A`, `Direction B`, `Direction C`) as defined in [doctrine/creative-direction.md](creative-direction.md) and [research/synthesis.md](../research/synthesis.md):
- **Direction A**: Quiet / hierarchy-led direction relying on composition, typography, and spacing.
- **Direction B**: Editorial, archival, or section-led subversion of category conventions.
- **Direction C**: Motion-led or tactile-instrument direction naming the specific product moment where motion improves feedback, orientation, or continuity.

Each direction must make a different choice about **composition**, **typography**, and **interaction** (plus palette/materiality).

---

## Stage 4: Pre-Implementation Originality Gate & Design Thesis

Evaluate Directions A, B, and C against the **Pre-Implementation Originality Gate** ([doctrine/creative-direction.md](creative-direction.md#3-the-pre-implementation-design-originality-gate)):
- Reject any direction that relies on overused defaults—including Sloppi v1's own overused tropes (e.g., defaulting to `Inter` + `JetBrains Mono`, `#0b0d13` + `#00d084` terminals, or flat white/navy `1px` bordered tables).
- Formulate a **Design Thesis** for the winning direction that locks in its physical metaphor, visual tension, typographic voice, and interaction posture.

---

## Stage 5: Expressive Art Direction & Semantic Token System

Translate the winning direction into a cohesive system in `DESIGN.md`:
1. **Distinctive Typography**: Pair an expressive, high-character Display/Headline typeface with a razor-sharp UI/Body typeface and a purposeful Monospace face. Use fluid `clamp()` sizing and optical tracking.
2. **Perceptual Color & Materiality**: Define semantic tokens (`--color-canvas`, `--color-surface`, `--color-text-primary`, `--color-brand`, etc.) backed by rich materiality—whether warm paper grain, brushed metallic bevels, bold chromatic poster blocks, or deep optical refraction.
3. **Behavior-First Interaction & Stack-Fit Motion**: Start from intended behavior, choose a stack-fitting implementation after checking dependency cost and licensing, and specify trigger, end state, touch, keyboard, repeated activation, and reduced-motion behavior ([implementation/interaction-implementation.md](../implementation/interaction-implementation.md)).

---

## Stage 6: Visual-First Primary Composition Prototype

Crystallize the contract in `DESIGN.md`, then **implement and prototype the primary composition (plus any proposed effect) first**. Verify layout and hierarchy via **screenshots** and timing/continuity via a **browser recording or interaction trace** before scaling to the rest of the interface.
