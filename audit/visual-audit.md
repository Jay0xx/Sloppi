# Sloppi v2.0 Visual Inspection Protocol, Primary Composition Gate & Viewport Matrix

Visual inspection in Sloppi v2.0 happens at **two critical moments**:
1. **Stage 5 — The Primary Composition Gate (Mid-Build)**: Right after building the above-the-fold hero or core workspace—**before** building the rest of the sections.
2. **Stage 7 & 8 — Full Multi-Viewport QA & Screenshot Regression (Pre-Ship)**: Across Mobile (`390px`), Tablet (`768px`), Desktop (`1280px`), and Wide (`1440px+`).

---

## 1. Stage 5: The Primary Composition Gate (Visual-First Check)

Never build an entire 8-section page before looking at the browser. As soon as the primary composition (Hero / Core Workspace) is rendered:
1. **Capture a Live Browser Screenshot** (using the `browser` subagent or Playwright/headless screenshot tool).
2. **Evaluate Creative Direction & Originality**:
   - **Reference Benchmark**: Does this composition hold its own against the live references you inspected in Stage 1 (`awwwards.com`, `godly.website`, `minimal.gallery`, `60fps.design`)?
   - **Silhouette & Scale**: Is the display typography commanding (`clamp`)? Is there unmistakable spatial tension, or did it collapse into a timid, centered SaaS template or flat `1px`-border wireframe?
   - **5-Second Interactive Proof**: Click/interact with the centerpiece widget in the browser. Does it respond with smooth spring physics and clear visual causality?
3. **Pass / Pivot Decision**: If the primary composition feels generic, flat, or lifeless, **overhaul its typography, materiality, or spatial split right now** before coding the remaining sections.

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
