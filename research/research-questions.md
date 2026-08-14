# Sloppi Design Research Questions Framework

The Research Questions framework teaches coding agents how to convert product requirements and audience constraints into explicit, sharp, high-intent design questions.

A coding agent must never begin research with vague inquiries like *"What are some nice SaaS designs?"* or *"What color looks modern?"*. Vague questions produce superficial aesthetic imitation. Precise questions produce architectural clarity.

---

## 1. High-Intent vs. Low-Intent Research Questions

| Design Domain | ❌ Low-Intent (Lazy/Vague) | ✅ High-Intent Sloppi Question |
| :--- | :--- | :--- |
| **Visual Identity** | "What theme looks cool for this app?" | *"What visual tone will convey institutional audit-level credibility to enterprise security architects without feeling sterile?"* |
| **Typography** | "What fonts are trending right now?" | *"How can typographic scale and line-height contrast establish strict reading hierarchy across dense technical data without relying on bordered containers?"* |
| **Composition** | "Should we use cards or a grid?" | *"Does this product's value proposition communicate better through an asymmetric editorial narrative or a high-density bento-box comparison?"* |
| **Hero Entry Point**| "What should we put in the hero?" | *"What immediate visual proof (e.g., interactive code snippet, live telemetry stream, or interactive calculator) must the first viewport demonstrate to prove value in < 3 seconds?"* |
| **Navigation** | "Should we use a sticky navbar?" | *"Given that this platform has 4 primary tools and 18 deep API reference docs, what navigation pattern balances immediate discoverability with zero viewport obstruction?"* |
| **Conversion / CTA**| "Where should we place the signup button?"| *"What is the primary action consequence and supporting assurance copy required to convert a developer who refuses to talk to sales?"* |
| **Motion** | "Can we add some cool animations?" | *"Which specific state transitions (e.g., query execution, schema diff rollback) benefit from spatial continuity and micro-feedback under 150ms?"* |
| **Mobile UX** | "How does desktop resize to mobile?" | *"Which multi-column comparison tables and interactive desktop canvases must be fundamentally re-architected into mobile-native bottom sheets or swipe sequences?"* |
| **Brand Geometry** | "What border radius should we pick?" | *"How can the sharp 45-degree angular motif of the product's logomark organically influence container corners, divider lines, and button geometry?"* |

---

## 2. Core Question Catalog by Design Axis

When scoping a project, the agent selects and answers only the questions directly relevant to the current task:

### Axis 1: Visual Identity & Emotional Calibration
- What are the operational stakes of this product (low-stakes social vs. mission-critical infrastructure)?
- What is the user's everyday aesthetic context (e.g., GitHub and Neovim vs. Bloomberg Terminal vs. Apple Notes)?
- What visual tone anchors the brand: Industrial, Clinical, Editorial, Playful, Brutalist, or Minimalist?

### Axis 2: Typography & Information Architecture
- What mathematical type scale ratio (Minor Third 1.200 vs. Major Third 1.250 vs. Perfect Fourth 1.333) matches the required spatial density?
- What line-height proportion prevents awkward line wrapping on large display headings (`0.85–1.05`) while keeping long-form body text effortless to read (`1.55–1.65`)?
- What role does monospaced typography play: decorative accent, code syntax, or tabular data alignment?

### Axis 3: Composition, Whitespace & Density
- Is the interface compact (data-first), comfortable (workflow-first), or spacious (narrative-first)?
- Where can negative space replace artificial container borders to group related information?
- How does the layout break columnar monotony across successive sections?

### Axis 4: Hero Section & Visual Entry Points
- Is the product's core value demonstrative (needs live interaction), analytical (needs data proof), or utility-based (needs copyable integration code)?
- How is visual weight balanced between the primary headline, product demonstration, and immediate call-to-action?
- Does the hero require an interactive sandbox, terminal emulator, or high-impact typography canvas?

### Axis 5: Navigation & Wayfinding
- What is the total link count and structural depth of the site/application?
- Does link density call for a floating island header (3–5 links), a persistent full-bleed navigation bar (6–10 links), or a sidebar dock with command palette (10+ links)?
- How does the desktop wayfinding system transform on mobile viewports (e.g., bottom tab bar vs. fullscreen overlay)?

### Axis 6: Conversion Patterns & Action Hierarchy
- What is the single most important user action on each screen?
- How is the visual weight contrast established between Primary, Secondary, and Tertiary actions?
- What outcome-explicit verbs replace generic placeholder labels ("Get Started" → "Create Free PostgreSQL Instance")?
- What inline assurance proof is required adjacent to the CTA (e.g., "No credit card required", "Deploy in 30 seconds")?

### Axis 7: Interaction, State & Motion
- What user interactions require instantaneous feedback (<100ms)?
- Which structural transitions require layout continuity (e.g., shared layout IDs, modal expansions from card triggers)?
- What fallback behavior is required under `prefers-reduced-motion`?

### Axis 8: Mobile Ergonomics & Responsive Refactoring
- Are all touch targets strictly $\ge 44\text{px} \times 44\text{px}$?
- Are primary navigation triggers anchored within the bottom thumb-reach zone?
- How are wide desktop data grids refactored into stacked narrative cards or swipeable carousels?

### Axis 9: Brand Motif & Interface Geometry
- What geometric rules govern the brand identity (e.g., circular, rectangular, chamfered, sharp)?
- How do corner radii scale across component levels (tags $\rightarrow$ buttons $\rightarrow$ cards $\rightarrow$ dialogs)?
- Are borders 1px subtle, 2px heavy hand-cut outlines, or replaced entirely by tonal surface shifts?

### Axis 10: Page Closures & Social Identity
- What information density is appropriate for the footer (minimal single-line closure vs. full directory sitemap)?
- How does the 1200x630 Open Graph (OG) social card extend the typography, color mood, and headline hierarchy to external social feeds?

---

## 3. Question Scoping Protocol

An agent must never answer all 30 questions for every project:
- **For a full greenfield product**: Select 5 to 7 primary questions across Visual Identity, Typography, Hero, Navigation, and Conversion.
- **For a focused redesign or new component**: Select 2 to 3 targeted questions.
- **For a localized bug fix**: Select 0 questions (rely entirely on existing `DESIGN.md` tokens).
