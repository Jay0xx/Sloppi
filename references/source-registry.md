# Sloppi v2.0 Design Reference Source Registry & Live Inspection Rules

This registry maps specialized design galleries and live inspiration channels for Sloppi-enabled coding agents.

> **MANDATORY LIVE INSPECTION RULE (v2.0)**:
> You are **strictly forbidden** from merely name-dropping URLs or brand names (*"Inspired by Linear, Stripe, and Mercury"*) from memory.
> - **When Online**: Use your browser (`browser` subagent) or search tools (`search_web`) to actually inspect 2–4 references from this registry and document **concrete visual observations** (exact layout proportions, font pairings, surface materiality, and motion mechanics).
> - **When Offline / Sandboxed**: Explicitly declare `Reference Mode: OFFLINE_SYNTHESIS` in `DESIGN.md` and synthesize your 3 divergent directions from first-principles art direction ([doctrine/creative-direction.md](../doctrine/creative-direction.md)). Never fake a live inspection.

---

## 1. High-Craft Art Direction, Visual Storytelling & Originality

### Awwwards
- **URL**: `https://www.awwwards.com/websites/`
- **Design Domain**: Experimental Art Direction, Scrollytelling, WebGL/Canvas Craft, Expressive Typography
- **Tier**: **Primary Art Direction Source**
- **When to Inspect**:
  - When formulating `Direction B` or `Direction C` during 3-Direction Divergence to break out of safe SaaS/corporate layouts.
  - When designing hero sections that rely on dramatic typographic scale, choreographed scroll reveals, or interactive canvas shaders.
- **What to Observe & Document**:
  - Unconventional viewport divisions (asymmetric splits, full-bleed kinetic posters, pinned narrative chapters).
  - Display typography scale jumps, mixed serif/sans headline treatments, and negative space tension.
  - Bespoke cursor/scroll choreography and page transition mechanics.

### Godly
- **URL**: `https://godly.website/`
- **Design Domain**: Contemporary Web Craft, Interactive Product Launches, High-Taste Digital Design
- **Tier**: **Primary Art Direction Source**
- **When to Inspect**:
  - When seeking contemporary, astronomically high-craft web design across developer tools, AI studios, creative agencies, and hardware brands.
  - When evaluating how top studios combine tactile materiality (grain, specular borders, micro-schematics) with fast, legible UX.
- **What to Observe & Document**:
  - Surface depth and lighting techniques (how elements separate without muddy drop shadows or flat wireframe boxes).
  - Interactive centerpiece mechanics in the first viewport.

### Minimal Gallery
- **URL**: `https://minimal.gallery/`
- **Design Domain**: Editorial Restraint, Whitespace Architecture, Swiss Grid Precision
- **Tier**: **Primary Composition Source**
- **When to Inspect**:
  - When designing products that require calm institutional authority, literary/editorial elegance, or gallery-grade negative space.
  - When eliminating card-inside-card clutter so typography and proportion carry the layout.
- **What to Observe & Document**:
  - Macro vs. micro whitespace ratios and column alignment axes.
  - How hierarchy is achieved through scale and contrast rather than boxes and badges.

### Dribbble (Curated Product & UI Explorations)
- **URL**: `https://dribbble.com/shots/popular/web-design`
- **Design Domain**: Visual Concept Exploration, Chromatic Harmonies, Tactile UI Controls, Custom Data Viz
- **Tier**: **Primary Visual Exploration Source**
- **When to Inspect**:
  - When exploring unexpected color palettes, bespoke chart/telemetry visualizations, tactile skeumorphic/hardware controls, or expressive card/widget silhouettes.
- **What to Observe & Document**:
  - Novel color pairings, custom SVG dial/chart aesthetics, and lighting/texture details (while verifying that extracted patterns remain accessible and functional in production DOM).

---

## 2. Motion Physics, Micro-Interactions & Mobile Ergonomics

### 60fps.design
- **URL**: `https://60fps.design/`
- **Design Domain**: Micro-Interactions, Spring Physics, State Transitions, Spatial Continuity
- **Tier**: **Primary Motion Source**
- **When to Inspect**:
  - Whenever engineering interactive state changes (morphing navbars, layoutId shared-element transitions, drawer physics, keypad feedback, live chart scrubbing).
- **What to Observe & Document**:
  - Trigger causality, spring stiffness/damping feel, choreography staggering, and how motion preserves spatial orientation.

### Loadmo.re
- **URL**: `https://loadmo.re/`
- **Design Domain**: Mobile-First Web Design, Thumb-Zone Ergonomics, Touch Choreography
- **Tier**: **Primary Mobile Source**
- **When to Inspect**:
  - Whenever designing mobile web apps (`390px` viewport target) or ensuring desktop layouts transform into native-feeling mobile experiences (bottom sheets, swipeable rails, thumb-zone triggers).
- **What to Observe & Document**:
  - Mobile header compression, bottom-docked action ergonomics, and vertical pacing on narrow viewports.

---

## 3. Product Category Architecture, Sections & Token Systems

### SaaSPO
- **URL**: `https://saaspo.com/`
- **Design Domain**: Industry-Specific UX, Real Product Workflows, Category Conventions (to Adopt or Subvert)
- **Tier**: **Primary Category Source**
- **When to Inspect**:
  - During Stage 1 (`Understand`) to see how live products in Fintech, DevTools, AI, Healthcare, or Commerce structure their domain information—both to extract functional clarity and to **identify the category clichés you must subvert**.
- **What to Observe & Document**:
  - Domain-authentic proof structures (interactive calculators, live sandboxes, compliance architecture) vs. overused category defaults to reject.

### Supahero
- **URL**: `https://supahero.io/`
- **Design Domain**: Above-the-Fold Hero Compositions, Entry-Point Hierarchy
- **Tier**: **Secondary Component Source**
- **What to Observe & Document**:
  - Visual weight balance between display typography, interactive product proof, and primary conversion triggers.

### Refero Styles
- **URL**: `https://styles.refero.design/`
- **Design Domain**: Production Design Tokens, Mathematical Type Ratios, Semantic Color Roles
- **Tier**: **Secondary System Source**
- **What to Observe & Document**:
  - Real-world token architectures, leading/tracking ratios, and surface contrast calibrations (never copy-paste a token sheet without adapting it to your chosen creative direction).

### Navbar Gallery / CTA Gallery / Deck.Gallery / Footer.design
- **URLs**: `https://navbar.gallery/` · `https://cta.gallery/` · `https://deck.gallery/` · `https://footer.design/`
- **Design Domain**: Wayfinding Systems, Conversion Mechanics, Narrative Pacing, Page Closures
- **Tier**: **Secondary Structural Sources**
- **What to Observe & Document**:
  - Navigation density scaling, sequential storytelling arcs (`Deck.Gallery`), and high-impact editorial footers.

---

## Summary Routing Matrix by Creative Goal

| Creative / Engineering Goal | Primary Channels to Inspect | What You Must Log Before Coding |
| :--- | :--- | :--- |
| **Break Out of Generic Layouts (3 Directions)** | `awwwards.com`, `godly.website`, `minimal.gallery` | 3 distinct spatial paradigms, font voices, and interactive hooks. |
| **Color, Materiality & Custom Data Viz** | `dribbble.com`, `godly.website`, `minimal.gallery` | Surface texture/lighting recipe, perceptual color harmony, SVG craft. |
| **Motion Choreography & Tactile States** | `60fps.design`, `awwwards.com` | Spring physics parameters, shared-layout transitions, hover/active mechanics. |
| **Domain UX & Category Subversion** | `saaspo.com`, `supahero.io`, `deck.gallery` | Core domain workflow + explicit list of category clichés being subverted. |
| **Mobile-First & Responsive Ergonomics** | `loadmo.re`, `60fps.design` | `390px` thumb-zone layout, sheet mechanics, responsive table transformation. |
