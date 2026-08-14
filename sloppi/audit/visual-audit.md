# Sloppi Visual Inspection Protocol & Viewport Matrix

Visual Inspection is the systematic process of reviewing rendered interface screenshots, DOM layouts, and computed styles across standard viewport categories.

---

## 1. The 4-Tier Viewport Inspection Matrix

A Sloppi agent must verify layout stability and compositional integrity across four canonical viewport environments:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. MOBILE VIEWPORT (< 640px · Baseline: 390px × 844px)                 │
│    Key Checks: Single-column flow, touch target ergonomics (≥44px),   │
│                fixed action dock, zero horizontal scrollbar overflow.  │
├────────────────────────────────────────────────────────────────────────┤
│ 2. TABLET VIEWPORT (640px – 1023px · Baseline: 768px × 1024px)         │
│    Key Checks: 2-column wrapping, grid transition stability, drawer nav│
│                refactoring, legible data tables without truncation.    │
├────────────────────────────────────────────────────────────────────────┤
│ 3. DESKTOP STANDARD (1024px – 1439px · Baseline: 1280px × 800px)       │
│    Key Checks: Full multi-column bento grids, split hero composition,   │
│                horizontal navigation, visible keyboard focus rings.    │
├────────────────────────────────────────────────────────────────────────┤
│ 4. WIDE DESKTOP (≥ 1440px · Baseline: 1920px × 1080px)                 │
│    Key Checks: Container max-width constraints (no awkward over-stretch│
│                to screen edges), balanced macro-whitespace framing.    │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Inspection Tooling & Environmental Adaptability

Sloppi is **tool-agnostic**. The agent uses the best available rendering mechanism in the runtime environment:

| Available Tooling | Inspection Technique | Scope of Verification |
| :--- | :--- | :--- |
| **Browser Subagents / Playwright / Puppeteer** | Capture full-page and viewport screenshots; run automated accessibility scanners (`axe-core`). | Full pixel-accurate visual rendering, interactive states, and layout reflow. |
| **Framework Dev Server (Vite / Next.js)** | Launch local server (`npm run dev`) and inspect DOM via automated browser curl/fetch. | Structural layout, CSS class application, and component mounting. |
| **Static HTML / CSS Inspection** | Analyze generated markup, CSS custom property cascades, and media query definitions. | Token compliance, semantic HTML landmarks, and responsive rule coverage. |

> **Graceful Degradation Rule**: If browser screenshot capture is unsupported in the current environment, the agent inspects the static DOM structure, computed CSS rules, and media query definitions directly, noting the environmental limitation in the audit log.

---

## 3. The 8-Point Visual Inspection Checklist

When inspecting a rendered viewport, the agent tests for eight visual failure patterns:

1. [ ] **Horizontal Overflow**: Is `document.body.scrollWidth > window.innerWidth`? (Zero tolerance for horizontal body scroll).
2. [ ] **Text Clipping & Orphans**: Are display headlines wrapping awkwardly with single-word drop lines?
3. [ ] **Element Overlap**: Are floating badges, sticky headers, or modals colliding with underlying content?
4. [ ] **Spacing Collapse**: Have margins or padding collapsed to 0px on small screens?
5. [ ] **Contrast Degradation**: Are text labels washed out against lightened surface grounds?
6. [ ] **Image / Media Distortion**: Are aspect ratios preserved (16:10 / 1:1) without stretching or pixelation?
7. [ ] **Container Over-Stretch**: On 1920px displays, is the content bounded within its defined max-width (`1200px` / `1440px`)?
8. [ ] **Interactive Reachability**: Are all primary CTA buttons and form controls accessible within normal scrolling reach?
