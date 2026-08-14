# Sloppi Frontend Implementation Protocol

The Implementation Protocol governs how a coding agent translates a Sloppi design specification (`DESIGN.md`), content architecture, and design thesis into working frontend code without compromising or diluting the underlying design reasoning.

Sloppi is **strictly framework-agnostic**. It does not replace React, Vue, Svelte, Next.js, Astro, or vanilla HTML/CSS; it establishes the cognitive and architectural discipline required to implement any interface with high fidelity and token integrity.

---

## 1. The Core Implementation Workflow

Implementation is strictly downstream from design reasoning. A Sloppi agent must never generate code by guessing layout aesthetics or writing ad-hoc styles.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   THE SLOPPI IMPLEMENTATION WORKFLOW                   │
│                                                                        │
│   1. DESIGN DECISION          (Design Thesis & Operational Stakes)     │
│             │                                                          │
│             ▼                                                          │
│   2. DESIGN SYSTEM            (DESIGN.md Contract & Token Taxonomy)    │
│             │                                                          │
│             ▼                                                          │
│   3. PROJECT INSPECTION       (Stack, Existing Tokens, Library Audit)  │
│             │                                                          │
│             ▼                                                          │
│   4. COMPONENT ARCHITECTURE   (Primitives, Components, Sections, Pages)│
│             │                                                          │
│             ▼                                                          │
│   5. CONTENT STRUCTURE        (7-Tier Hierarchy & Data Models)         │
│             │                                                          │
│             ▼                                                          │
│   6. VISUAL IMPLEMENTATION    (Layout, Typography, Tokens, Surfaces)   │
│             │                                                          │
│             ▼                                                          │
│   7. RESPONSIVE COMPOSITION   (Breakpoint Transformations & Ergonomics)│
│             │                                                          │
│             ▼                                                          │
│   8. INTERACTION & MOTION     (State Feedback, Keyboard, Transitions)  │
│             │                                                          │
│             ▼                                                          │
│   9. RENDER & VALIDATION      (Accessibility, Anti-Drift Audit)        │
└────────────────────────────────────────────────────────────────────────┘
```

### The Anti-Pattern to Reject
```
[❌ The Lazy AI Implementation Anti-Pattern]
Generate Generic Components ──► Add Ad-hoc Styles ──► Add Random Gradients ──► Hope It Looks Nice
```

---

## 2. Visual Implementation Priority: Structure Before Polish

When building an interface, the agent must resolve structural and informational challenges before applying surface styling. Sloppi enforces a 10-tier implementation priority:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. INFORMATION HIERARCHY  ──► Correct sequence, reading flow & anchors │
│ 2. LAYOUT & CONTAINERS    ──► Max-widths, alignment, grid structures   │
│ 3. TYPOGRAPHY & MEASURE   ──► Font scales, line-heights, 45-75ch limit │
│ 4. SPATIAL CADENCE        ──► Systematic margins, padding, rhythm      │
│ 5. COLOR TAXONOMY         ──► Semantic canvas, surface, text tokens    │
│ 6. GEOMETRY & RADII       ──► Concentric radii, border stroke weights  │
│ 7. IMAGERY & MEDIA        ──► Real domain data, verified diagrams      │
│ 8. INTERACTION STATES     ──► :hover, :focus-visible, :active, loading │
│ 9. PURPOSEFUL MOTION      ──► Micro-timings, state transitions (240ms) │
│ 10. DECORATIVE ACCENTS    ──► Subtle hairline highlights, dividers     │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 3. The "Polish Trap" & Remediation Protocol

A critical failure mode of AI coding agents is the **"Polish Trap"**: when an interface feels generic, flat, or unconvincing, the agent instinctively reacts by adding superficial decorative clutter:
- Adding radial background blur gradients (*"mesh gradients"* / *"glowing orbs"*).
- Slapping excessive glassmorphism (`backdrop-filter: blur(16px)`) onto every box.
- Applying dramatic multi-colored neon button drop-shadows.
- Adding arbitrary float animations or constant rotational spins to icons.
- Rounding every card corner to an exaggerated pill shape (`rounded-3xl`).

### The Sloppi Remediation Protocol
When an interface feels visually weak or generic, **do not add decorative effects**. Instead, diagnose and resolve core structural deficiencies:

| Symptom of Weak Design | ❌ Wrong Response (Polish Trap) | ✅ Sloppi Structural Remediation |
| :--- | :--- | :--- |
| **Page feels boring / flat** | Add colorful gradient orbs and animated particle canvas | Increase typographic scale contrast (e.g. bump display title from $36\text{px}$ to $56\text{px}$ with tight $-0.03\text{em}$ tracking). |
| **Cards feel disconnected** | Add heavy dark drop-shadows and glassmorphic opacity | Tighten card padding, apply razor-sharp 1px border (`--color-border`), and introduce clear section ground contrast (`--color-canvas-alt`). |
| **Hero feels empty** | Add arbitrary 3D floating shapes or generic stock mockup | Replace placeholder text with an interactive live code terminal, SVG architecture diagram, or split value layout. |
| **Sections blend together** | Add wavy SVG divider curves | Modulate vertical padding ($64\text{px} \longleftrightarrow 128\text{px}$), alternate ground planes, and switch from grid to asymmetric editorial layout. |
| **Buttons feel weak** | Add pulsing glow animations and rainbow borders | Use high-contrast solid brand fill (`--color-brand`), outcome-explicit copy (*"Create Free Workspace"*), and 2px high-contrast `:focus-visible` rings. |

---

## 4. Incremental 7-Pass Implementation Strategy

To ensure precision and prevent compounding bugs, the agent must implement complex interfaces across seven distinct, verifiable passes:

```
Pass 1: Structural Skeleton & Landmark Containers (Semantic HTML5: header, main, nav, section, footer)
   ↓
Pass 2: Content & Typographic Scale (Real domain copy, display/body tokens, balanced text wrapping)
   ↓
Pass 3: Spacing & Ground Surface Tokens (Canvas grounds, card fills, 1px perimeter borders)
   ↓
Pass 4: Responsive Transformations (Mobile ergonomics, layout refactoring, touch targets ≥44px)
   ↓
Pass 5: Interactive States & Keyboard Focus (:hover, :focus-visible, :active, disabled, loading)
   ↓
Pass 6: Purposeful Motion & State Transitions (Micro-durations 120ms–240ms, prefers-reduced-motion)
   ↓
Pass 7: Accessibility & Anti-Drift Audit (WCAG AA/AAA contrast check, token traceability validation)
```

---

## 5. Design Drift Governance

**Design Drift** occurs when implementation incrementally diverges from the approved `DESIGN.md` contract through ad-hoc coding shortcuts:
- Introducing unmapped arbitrary hex colors (`color: #3b82f6`).
- Using hardcoded pixel margins (`margin-top: 37px`) outside the spatial scale.
- Inventing new component radius values (`border-radius: 19px`).
- Replacing domain-specific copy with generic placeholder text.

### The Deviation Rule
If implementation necessitates modifying a token or layout rule, the agent must determine if the change is **intentional and necessary**. If so, it must explicitly update `DESIGN.md` or record the rationale in the **Implementation Decision Log**. Silent drift is strictly prohibited.
