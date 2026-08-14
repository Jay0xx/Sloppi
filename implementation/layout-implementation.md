# Sloppi Layout Implementation & Spatial Cadence

Layout Implementation translates the compositional structures, grid models, and section rhythms defined in `DESIGN.md` into clean CSS layouts.

A coding agent must never default to rigid boilerplate layout classes (`max-w-6xl mx-auto py-12` on every single section) or resort to fragile absolute positioning hacks.

---

## 1. Container Width Archetypes & Spatial Constraints

Sloppi establishes four deliberate container widths based on content density and visual gravity:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. EDITORIAL MEASURE   ──► max-width: 768px (48rem)                    │
│    Optimal for: Long-form technical essays, legal disclosures, single- │
│                 column manifesto blocks (maintains 65ch reading line). │
├────────────────────────────────────────────────────────────────────────┤
│ 2. STANDARD APP / SAAS ──► max-width: 1200px (75rem)                   │
│    Optimal for: Standard feature overviews, pricing matrices, and      │
│                 onboarding flows.                                      │
├────────────────────────────────────────────────────────────────────────┤
│ 3. WIDE TELEMETRY / HUD ─► max-width: 1440px (90rem)                   │
│    Optimal for: Multi-column developer hubs, asymmetric bento grids,   │
│                 and live telemetry streams.                            │
├────────────────────────────────────────────────────────────────────────┤
│ 4. FULL-BLEED CANVAS   ──► width: 100vw (padding: 0 var(--space-6))    │
│    Optimal for: Interactive WebGL canvases, live terminal REPLs, and   │
│                 immersive video showcases.                             │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Layout Modes: Flexbox vs. Grid Discipline

| Layout Task | Recommended CSS Mechanism | Rationale & Guardrail |
| :--- | :--- | :--- |
| **1-Dimensional Rows / Bars** (Nav, Action bars, Tag lists) | `display: flex; align-items: center; justify-content: space-between;` | Flexbox excels at intrinsic content-based wrapping and baseline alignment. |
| **Asymmetric Bento Grids** (1 dominant hero card + 3 micro tiles) | `display: grid; grid-template-columns: repeat(12, 1fr); gap: var(--space-6);` | Explicit 12-column subgrid allows precise `col-span-8` vs `col-span-4` asymmetric weights. |
| **Data Specification Matrices** | `display: grid; grid-template-columns: 240px 1fr 1fr;` | Fixed label column paired with fractional comparison tracks prevents alignment jitter. |
| **Editorial 2-Column Split** (Headline left + Code right) | `display: grid; grid-template-columns: 1fr 1.25fr; gap: var(--space-12);` | Asymmetric ratio gives interactive terminal visual dominance over copy anchor. |

---

## 3. Section Cadence & Vertical Rhythm

To eliminate the monotone "cookie-cutter" look of stacked AI templates, Sloppi modulates vertical padding and ground contrast down the page:

```
┌────────────────────────────────────────────────────────────────────────┐
│ SECTION 1: HERO (SPLIT COMPOSITION)                                    │
│ Height: ~750px · Padding: var(--space-24) (96px) · Ground: --color-canvas
├────────────────────────────────────────────────────────────────────────┤
│ SECTION 2: TELEMETRY STREAM (COMPACT DATA HUD)                         │
│ Height: ~320px · Padding: var(--space-12) (48px) · Ground: --color-canvas-alt
├────────────────────────────────────────────────────────────────────────┤
│ SECTION 3: ARCHITECTURAL DEEP-DIVE (ASYMMETRIC BENTO)                  │
│ Height: ~850px · Padding: var(--space-32) (128px) · Ground: --color-canvas
├────────────────────────────────────────────────────────────────────────┤
│ SECTION 4: REPRODUCIBLE BENCHMARK MATRIX (DATA GRID)                   │
│ Height: ~450px · Padding: var(--space-16) (64px) · Ground: --color-canvas-alt
├────────────────────────────────────────────────────────────────────────┤
│ SECTION 5: FINAL ACTION CLOSURE (HIGH-CONTRAST FOCUS)                  │
│ Height: ~400px · Padding: var(--space-24) (96px) · Ground: --color-canvas
└────────────────────────────────────────────────────────────────────────┘
```

---

## 4. Stacking Contexts & Overflow Discipline

- **Z-Index Scale**: Never use arbitrary values like `z-index: 99999`. Maintain a strict scale:
  - Base Content: `z-index: 0`
  - Sticky Headers: `z-index: 10`
  - Dropdowns & Popovers: `z-index: 20`
  - Modal Overlays: `z-index: 50`
  - Toast Notifications: `z-index: 100`
- **Horizontal Overflow Zero Tolerance**: The body document must never introduce horizontal scrollbars on any viewport. Apply `overflow-x: clip;` or `overflow-x: hidden;` at the layout root while testing responsive breakpoints.
