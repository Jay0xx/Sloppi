# Sloppi v2.0 Visual Inspection Protocol, Primary Composition Gate & Viewport Matrix

Visual inspection in Sloppi v2.0 happens at **two critical moments**:
1. **Stage 5 — The Primary Composition Gate (Mid-Build)**: Right after building the above-the-fold hero or core workspace—**before** building the rest of the sections.
2. **Stage 7 & 8 — Full Multi-Viewport QA & Screenshot Regression (Pre-Ship)**: Across Mobile (`390px`), Tablet (`768px`), Desktop (`1280px`), and Wide (`1440px+`).

---

## 1. Stage 5: The Primary Composition Gate (Visual-First Check)

Never build an entire 8-section page before looking at the browser. Prototype any proposed interactions directly inside the primary composition (Hero / Core Workspace or Flow) first, and as soon as it renders:
1. **Capture Dual Proof Artifacts**:
   - **Screenshots** (via **Playwright MCP** or the `browser` subagent) for **layout, spacing, contrast, and typographic hierarchy**.
   - **Browser Recording or Interaction Trace** (if motion or state transitions are present) for **timing, anchoring, easing/spring continuity, repeated activation, and reduced motion**.
2. **Evaluate Creative Direction & Originality**:
   - **Reference Benchmark**: Does this composition hold its own against the live references inspected in Stage 1 ([references/source-registry.md](../references/source-registry.md))? Run `web-design-guidelines` (and `vercel-react-best-practices` for React/Next.js) when appropriate.
   - **Silhouette & Scale**: Is the display typography commanding (`clamp`)? Does a quiet direction carry clear hierarchy through spacing and scale alone, or did it collapse into a timid template or flat `1px`-border wireframe?
   - **Interaction & Timing Proof**: Trigger the primary state change via mouse, touch, keyboard, and repeated rapid activation. Does it preserve orientation, settle cleanly, and obey `@media (prefers-reduced-motion: reduce)`?
3. **Pass / Pivot Decision**: If the primary composition feels generic, flat, or laggy, **fix typography, materiality, or motion timing right now** before coding the remaining sections.

---

## 2. The 4-Tier Viewport Inspection Matrix

Before shipping, inspect rendered viewports across four canonical widths:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. MOBILE (`390px × 844px`)                                            │
│    Checks: Zero horizontal overflow (`scrollWidth <= innerWidth`),     │
│            ≥44×44px touch targets, thumb-zone nav, legible 16px inputs.│
├────────────────────────────────────────────────────────────────────────┤
│ 2. TABLET (`768px × 1024px`)                                           │
│    Checks: Clean 2-column or adaptive rail transition, zero squeezed   │
│            tables or colliding nav items.                              │
├────────────────────────────────────────────────────────────────────────┤
│ 3. DESKTOP STANDARD (`1280px × 800px`)                                 │
│    Checks: Full asymmetric grid / workbench proportions, dramatic      │
│            display typography scale, visible `:focus-visible` rings.   │
├────────────────────────────────────────────────────────────────────────┤
│ 4. WIDE DESKTOP (`1440px – 1920px`)                                    │
│    Checks: Intentional max-width framing or full-bleed canvas balance; │
│            no orphaned 140ch text lines.                               │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Epistemic Honesty in Visual Reporting

Always report the exact verification tier in your audit summary:
- **`OBSERVED (Live Browser Screenshot)`**: Verified directly in the rendered browser viewport across specified resolutions.
- **`INFERRED (Static DOM/CSS Analysis)`**: Evaluated ONLY when browser rendering is completely blocked by the host environment (must be explicitly stated). Never claim to have inspected a screenshot if no browser render occurred.
