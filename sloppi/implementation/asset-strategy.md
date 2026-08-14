# Sloppi Asset Strategy & Icon Governance

Asset Strategy governs how imagery, illustrations, product captures, and icons are selected, optimized, and managed in the codebase.

A coding agent must never generate fake placeholder images, insert irrelevant stock photos, or mix multiple incompatible icon libraries across an application.

---

## 1. The 7 Asset Categories & Implementation Rules

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. BRAND LOGOS & WORDMARKS   ──► Clean inline SVGs; currentColor fill. │
│ 2. ICONOGRAPHY               ──► Single curated library; uniform stroke│
│ 3. PRODUCT UI SCREENSHOTS    ──► Real domain data; 16:10 aspect ratio; │
│                                  lossless WebP/AVIF compression.       │
│ 4. TECHNICAL SYSTEM DIAGRAMS ──► Semantic SVG linework; labeled nodes. │
│ 5. EDITORIAL PHOTOGRAPHY     ──► Authentic high-res photography; no    │
│                                  generic cheesy office stock images.   │
│ 6. MOTION & VIDEO REELS      ──► Autoplay muted loop with poster frame;│
│                                  prefers-reduced-motion fallback.      │
│ 7. DECORATIVE ASSETS         ──► Subtle hairline patterns; zero random │
│                                  blurred 3D spheres.                   │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Intentional Asset Absence: The "No Stock Slop" Rule

If high-fidelity product screenshots or authentic customer photography do not yet exist, **do not insert generic AI-generated stock photos or placeholder wireframe boxes**.

Make asset absence **intentional, functional, and authoritative**:
1. **Use Interactive Monospace Terminals**: Show live CLI commands and execution outputs.
2. **Use Vector Architecture Schematics**: Draw clean, annotated SVG dataflows.
3. **Use Typographic Gravity**: Allow oversized display headlines and expansive whitespace to carry visual authority.
4. **Use Tabular Telemetry Matrices**: Display real system metrics and benchmarks.

---

## 3. Icon Governance & Dependency Rules

Mixing different icon libraries creates visual dissonance and amateurism (e.g. mixing rounded outline icons with sharp filled icons).

### The 4 Icon Rules
1. **Single Icon Family**: Select one curated library (e.g. `Lucide`, `Phosphor`, `Heroicons`) and use it exclusively across the entire application.
2. **Uniform Optical Stroke**: Enforce consistent stroke width (strictly `1.5px` or `2.0px`) across all rendered icons.
3. **Optical Scale Hierarchy**:
   - `XS (12px)`: Micro inline metadata and status chips.
   - `SM (16px)`: Buttons, table cells, and input adornments.
   - `MD (20px)`: Navigation links and standard actions.
   - `LG (24px)`: Major section anchors and modal headers.
4. **No Heavy Packages for Single Icons**: If an application requires only a right chevron (`→`) and a copy icon, write clean inline SVG strings rather than installing a 15MB icon dependency.
