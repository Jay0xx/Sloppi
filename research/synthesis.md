# Sloppi Design Synthesis & Thesis Formulation

Design Synthesis is the cognitive bridge between external research and original UI implementation. 

After completing reference analysis, a Sloppi agent must not immediately begin writing code. It must synthesize its findings into an original, coherent **Design Thesis** supported by explicit constraints, rejected conventions, and calibrated visual tensions.

---

## 1. The Cross-Reference Comparison Matrix

Before drafting the design thesis, the agent compares all analyzed references across five analytical vectors:

```
[ References Analyzed ]
           │
           ├────────────────────────► 1. Common Patterns (Shared solutions)
           ├────────────────────────► 2. Strategic Divergences (Where & why they differ)
           ├────────────────────────► 3. Convention vs. Default Test (Separating utility from cliché)
           ├────────────────────────► 4. Unexplored Opportunities (Novel whitespace in the market)
           └────────────────────────► 5. Rejected Clichés (Explicitly banned patterns for this project)
```

### The Convention vs. Default Evaluation Test

| Observed Pattern | Is it a Convention or a Default? | Sloppi Evaluation Rationale |
| :--- | :--- | :--- |
| **Sticky Navigation Bar** | **Convention** | Solves a universal wayfinding friction on long-form pages. Retained and styled according to token rules. |
| **3-Column Feature Cards**| **Default** | An unthinking layout reflex. Replaced by asymmetric bento or live interactive demo. |
| **Pill Buttons for CTAs** | **Convention** | Universally signals clickability and primary action affordance. Adapted to brand radius scale. |
| **Pills for Eyebrow Headers**| **Default** | Adds container clutter above headlines. Replaced by clean uppercase tracking-expanded typography. |
| **Radial Purple Gradient Blobs**| **Default** | Disguises empty space without conveying light source or depth. Replaced by solid canvas or intentional surface tint. |
| **Monospaced Data Alignment** | **Convention** | Essential for optical scanning of numerical metrics, timestamps, and code parameters. |

---

## 2. The 5 Core Synthesis Pillars

Every synthesis pass must yield five concrete outputs:

### 1. Design Opportunities
- Unconventional or underutilized approaches discovered during research that directly serve the product thesis (e.g., replacing static screenshots with a live browser-based REPL; replacing multiple feature cards with an interactive architecture flow diagram).

### 2. Design Constraints
- Non-negotiable ergonomic, technical, and accessibility boundaries (e.g., strict WCAG AAA contrast for medical data; 100% viewport containment on desktop dashboards without page scrolling; $\ge 44\text{px}$ touch targets for mobile).

### 3. Rejected Conventions
- Specific industry defaults that this product deliberately chooses *not* to use, along with the rationale (e.g., *"We reject the standard dark-neon crypto aesthetic in favor of high-restraint alpine banking neutrals to communicate institutional reliability"*).

### 4. Selected Principles
- The 4 to 6 structural rules governing the product's visual execution (e.g., asymmetric section rhythm, 4px base density, crushed display leading, zero ambient drop shadows).

### 5. Controlled Visual Tensions
Distinctive character in digital product design arises from **controlled contrast between paired opposing qualities**, not from random decoration:

| Controlled Visual Tension | How It Manifests in the Interface |
| :--- | :--- |
| **Technical + Warm** | Monospaced tabular data and precise 1px borders resting on warm textured paper (`#fbf9f5`) and rich terracotta accents. |
| **Dense + Spacious** | High-density data metrics contained inside compact cards, balanced by generous macro-margins between major section chapters. |
| **Minimal + Expressive** | Severe monochrome typography and stark layout restraint punctuated by a single, vibrant, kinetic brand interaction. |
| **Precise + Playful** | Rigorous geometric grid alignment softened by hand-cut sticker-style borders and organic corner curvatures. |
| **Serious + Approachable** | High-contrast audit-grade legibility paired with conversational, outcome-explicit copywriting. |

---

## 3. Formulating the Design Thesis

The **Design Thesis** is the definitive 2-to-4 sentence contract that governs all subsequent UI generation. It must directly answer four questions:

1. **What should this product feel like?**
2. **Why does that feeling serve the target audience and operational stakes?**
3. **What concrete visual principles will create that feeling?**
4. **What generic industry defaults are we deliberately avoiding?**

---

### Exemplary Design Theses Across Archetypes

#### Archetype A: Enterprise Database & Telemetry Monitor (Technical / High-Stakes)
> *"The product must feel like a mission-critical flight recorder: midnight tungsten canvas, crisp phosphor-green latency indicators, strict monospaced tabular alignment, and zero decorative glassmorphism. Because database engineers require instant anomaly detection without cognitive fatigue, we prioritize compact data density and 1px crisp borders. We deliberately reject marketing-style gradient blobs, floating badges, and generic 3-card feature grids in favor of live query telemetry and an interactive schema workbench."*

#### Archetype B: Boutique Financial Advisory & Wealth Management (High-Trust / Editorial)
> *"The product must feel like a bespoke private bank broadsheet: warm alabaster paper canvas (`#f9f8f5`), authoritative high-contrast serif headlines, deep navy structural ink, and asymmetric editorial columns. To convey enduring financial stewardship to high-net-worth clients, we rely on generous macro-whitespace and rigorous typographic scale contrast. We explicitly reject trendy neon accents, floating 3D coins, and generic SaaS card containers."*

#### Archetype C: Expressive Mobile Social & Audio Sandbox (Playful / Low-Stakes)
> *"The product must feel like a tactile, kinetic soundboard: soft pastel ground, oversized sculptural display type, 2px hand-cut carbon outlines, and spring-physics touch gestures. To invite creative exploration, interactive elements use pill-shaped geometries and vibrant multi-accent sticker chips. We avoid rigid enterprise tables, muted gray monochrome palettes, and static desktop-style navigations."*
