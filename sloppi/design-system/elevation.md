# Sloppi Elevation & Depth Architecture

Elevation defines how user interface elements occupy the third dimension ($Z$-axis) through layering, surface tints, borders, and shadows.

In Sloppi, depth must always serve a clear communicative purpose: establishing spatial hierarchy, indicating interaction readiness, focusing attention, or clarifying overlapping layers.

A coding agent must never default to adding heavy, muddy drop shadows to every card container. If a product’s visual language calls for a flat, border-governed aesthetic, use zero shadows.

---

## 1. The 3 Material Depth Strategies

The agent chooses a depth strategy that reinforces the project's Design Thesis:

```
1. PURE FLAT / BORDER-DRIVEN ──► Depth created strictly through 1px borders and surface tone shifts. Zero drop shadows. (Terminals, editorial, brutalist).
2. MULTI-LAYER AMBIENT OCCLUSION ──► Soft, low-opacity, double-layer shadows mimicking natural ambient lighting. (Modern SaaS, web apps).
3. HARD RETRO / TACTILE OFFSET ──► Hard 2px–4px solid offset shadows (e.g., `3px 3px 0px #000000`). (Sticker-book, neo-brutalist).
```

---

## 2. The 4-Level Canonical Elevation Model

When shadow-based elevation is appropriate, Sloppi structures depth into four standardized levels:

```
[ Level 3: Modal Dialogs & Overlays ]   ──► Highest Z-index, maximum ambient spread + backdrop scrim
[ Level 2: Popovers, Dropdowns, Hover ] ──► Interactive float above the standard interface plane
[ Level 1: Resting Elevated Cards ]     ──► Subtle physical separation above the base canvas
[ Level 0: Flush In-Flow Containers ]   ──► Co-planar with canvas; bounded by 1px border only
```

### Elevation Token Matrix

| Level Token | Box-Shadow Recipe (Light Mode Example) | Purpose & Application |
| :--- | :--- | :--- |
| `--elevation-0` | `none` (border: `1px solid var(--color-border)`) | In-flow feature sections, static dashboard grids, inline tables. |
| `--elevation-1` | `0 1px 3px 0 rgba(0,0,0,0.04), 0 1px 2px -1px rgba(0,0,0,0.02)` | Resting interactive cards, draggable kanban items. |
| `--elevation-2` | `0 4px 6px -1px rgba(0,0,0,0.06), 0 2px 4px -2px rgba(0,0,0,0.03)` | Card hover states, dropdown menus, autocomplete popovers. |
| `--elevation-3` | `0 20px 25px -5px rgba(0,0,0,0.08), 0 8px 10px -6px rgba(0,0,0,0.04)` | Centered modal dialogs, lightbox media previews. |

---

## 3. The Multi-Layer Ambient Shadow Rule

Never use a single harsh drop shadow (`box-shadow: 0 10px 20px rgba(0,0,0,0.4)`). Single-layer shadows create muddy, artificial smudges.

### Multi-Layer Shadow Formula
Always combine two shadow layers:
1. **The Ambient Occlusion Layer**: Wide spread, very low opacity ($2\%–5\%$), zero horizontal offset, small vertical offset. Simulates soft indirect environmental light.
2. **The Direct Light Layer**: Tight spread, slightly higher opacity ($4\%–8\%$), vertical offset. Simulates directional ceiling light and grounds the element.

```css
/* Sloppi Standard Elevated Card */
box-shadow: 
  0 1px 3px 0 rgba(0, 0, 0, 0.05),     /* Direct contact shadow */
  0 10px 15px -3px rgba(0, 0, 0, 0.03); /* Ambient atmospheric spread */
```

---

## 4. Backdrop Scrims & Surface Refraction

- **Modal Backdrops (`--color-scrim`)**: When activating a Level 3 dialog, apply a neutral darkened backdrop (`rgba(0, 0, 0, 0.5)`) paired with a subtle blur (`backdrop-filter: blur(4px)`). This lowers background contrast and locks user focus onto the modal task.
- **Glassmorphism Guardrail**: Never apply `backdrop-blur` to static in-flow cards resting on solid backgrounds. Reserve backdrop filters strictly for floating sticky headers and contextual overlays where scrolling content actually passes underneath.
