# [Product Name] — Design System Specification (DESIGN.md)

> **Persistent Design Contract for [Product Name]**  
> *Generated via Sloppi Design Intelligence Framework*

---

## 1. Design Thesis
<!-- 1-3 sentence core visual point of view, material metaphor, and density model -->
*Example: A high-density telemetry console built with a midnight tungsten canvas, crisp phosphor-green latency indicators, monospaced tabular alignment, and zero decorative glassmorphism.*

---

## 2. Product Context & Operational Stakes
- **Operational Stakes**: [Low / Medium / High & Mission-Critical]
- **User Persona & Mental Model**: [Description of target audience expectations and daily workflow context]
- **Core Conversion Objective**: [Primary user journey and task completion metric]

---

## 3. Design Personality Profile
- **Diagnostic Axes**: Technical ([X]%) · Expressive ([X]%) · Dense ([X]%) · Geometric ([X]%)
- **Tonal Anchors**: [Anchor 1] · [Anchor 2] · [Anchor 3] · [Anchor 4]

---

## 4. Content Principles
- **Truthfulness Mandate**: Zero fabricated logos, fake user testimonials, or unverified benchmark metrics.
- **Vocabulary Standard**: Plain technical verbs and domain nouns over vague marketing adjectives.
- **Reading Measure**: Max 65ch measure for body paragraphs; max 12 words with `text-wrap: balance` for display titles.

---

## 5. Messaging & Value Architecture
- **Primary Mechanism**: [Underlying architectural breakthrough]
- **Feature vs. Benefit vs. Outcome**:
  - *Feature*: [What technology executes]
  - *Benefit*: [What user directly achieves]
  - *Outcome*: [Ultimate business/operational impact]
- **Banned Clichés**: [Explicit list of purged buzzwords and concrete replacements]

---

## 6. Information & Attention Hierarchy
- **7-Tier Attention Allocation**:
  - Tier 1 Display Hook (`display-2xl` / `display-xl`)
  - Tier 2 Supporting Subhead (`body-lg`)
  - Tier 3 Evidentiary Proof (Terminal REPL / Architecture SVG)
  - Tier 4 Primary Action (`var(--color-brand)` button)
  - Tier 5 Deep Mechanics (`heading-md` + `body`)
  - Tier 6 Assurance Micro-Copy (`body-sm`)
  - Tier 7 Metadata & Specs (`caption` / `font-mono`)
- **Single Focal Point Mandate**: Exactly one primary visual anchor per visible viewport.

---

## 7. Page Architecture & Section Cadence
- **Hero Architecture Paradigm**: [e.g., Demonstration-First, Split CLI Composition, Dense HUD, Text-First Editorial]
- **Feature Presentation Models**: [e.g., Asymmetric Bento, Interactive Sandbox, Annotated Blueprint, Side-by-Side Diff]
- **Section Sequence & Justification**:
  1. *[Section 1]*: Purpose, User Need, Content, Action.
  2. *[Section 2]*: Purpose, User Need, Content, Action.
  3. *[Section 3]*: Purpose, User Need, Content, Action.
- **Section Rhythm Modulation**: Alternating heights ($320\text{px} \longleftrightarrow 750\text{px}$) and ground tones (`--color-canvas` $\longleftrightarrow$ `--color-canvas-alt`).

---

## 8. CTA Rules & Action Hierarchy
- **Primary Action**: `[Exact Label, e.g., "Create Free Workspace"]` · Fill: `var(--color-brand)`
- **Secondary Action**: `[Exact Label, e.g., "Inspect API Documentation"]` · Border: `1px solid var(--color-border)`
- **Inline Assurance**: `[e.g., "🔒 No credit card required · Instant setup in 60 seconds"]`

---

## 9. Content Density & Text Measure
- **Density Mode**: [Sparse / Moderate / Balanced / Dense / Information-Heavy]
- **Text Measure**: Body max-width `65ch`; Display headings constrained to single-concept balanced lines.

---

## 10. Visual Principles
1. [Principle 1 — e.g., Typographic hierarchy carries authority before boxes are drawn]
2. [Principle 2 — e.g., Asymmetric composition breaks repetitive grid monotony]
3. [Principle 3 — e.g., Micro-interactions provide instantaneous state feedback]
4. [Principle 4 — e.g., Negative space functions as cognitive punctuation]

---

## 11. Typography Architecture

### Font Families
- **Display / Heading**: `[Font Family Name]`, fallback: `[system-ui, sans-serif / serif]`
- **UI / Body**: `[Font Family Name]`, fallback: `[system-ui, sans-serif]`
- **Monospace / Data**: `[Font Family Name]`, fallback: `[ui-monospace, monospace]`

### Type Scale (Base: 16px / 1rem · Scale Ratio: [e.g., Minor Third 1.200 / Major Third 1.250])

| Token | Size (px/rem) | Weight | Line-Height | Letter-Spacing | Intended Semantic Assignment |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `display-2xl` | `61px / 3.81rem` | 800 | `0.95` | `-0.030em` | Hero visual anchor, major punchlines |
| `display-xl` | `49px / 3.05rem` | 700 | `1.02` | `-0.025em` | Page main titles (H1) |
| `heading-lg` | `39px / 2.44rem` | 600 | `1.12` | `-0.020em` | Section headers (H2) |
| `heading-md` | `31px / 1.95rem` | 600 | `1.22` | `-0.015em` | Feature headers, subsection titles (H3) |
| `heading-sm` | `25px / 1.56rem` | 600 | `1.30` | `-0.010em` | Card titles, modal headers (H4) |
| `body-lg` | `20px / 1.25rem` | 400 | `1.50` | `-0.005em` | Lead introduction paragraphs |
| `body` | `16px / 1.00rem` | 400 | `1.60` | `normal` | Standard reading body copy, inputs |
| `body-sm` | `13px / 0.81rem` | 500 | `1.45` | `+0.010em` | Buttons, navigation links, table cells |
| `caption` | `11px / 0.69rem` | 500 | `1.40` | `+0.030em` | Monospace tags, status pills, timestamps |

---

## 12. Color Palette & Semantic Roles

```
[ Canvas Ground ]  ───────────► #XXXXXX (Base backdrop)
[ Canvas Ground Alt ] ────────► #XXXXXX (Alternating section ground)
[ Surface Fill ]  ────────────► #XXXXXX (Card / panel container)
[ Text Primary ]  ────────────► #XXXXXX (WCAG AAA >= 7:1)
[ Text Secondary ] ───────────► #XXXXXX (WCAG AA >= 4.5:1)
[ Text Muted ]  ──────────────► #XXXXXX (Metadata, labels)
[ Brand Signature ] ──────────► #XXXXXX (Primary CTA anchor)
[ Brand Contrast Text ] ──────► #XXXXXX (Text on brand fill)
[ Border Perimeter ] ─────────► #XXXXXX (1px structural dividers)
[ Border Subtle ] ────────────► #XXXXXX (Inner table / card splits)
```

### Functional & Semantic Accents
- **Accent Info**: `#XXXXXX` — [Usage description]
- **Accent Success**: `#XXXXXX` — [Usage description]
- **Accent Warning**: `#XXXXXX` — [Usage description]
- **Accent Danger**: `#XXXXXX` — [Usage description]

---

## 13. Spacing & Density System
- **Base Unit**: `4px` or `8px`
- **Container Max-Width**: `[e.g., 1200px / 1440px]`
- **Section Vertical Gap**: `[e.g., 64px / 96px / 128px]`
- **Card Internal Padding**: `[e.g., 16px compact / 24px comfortable / 32px spacious]`
- **Element Control Gap**: `[e.g., 8px / 12px / 16px]`

---

## 14. Layout, Grids & Container Symmetry
- **Primary Grid**: `[Asymmetric bento / 2-column editorial / dense data HUD]`
- **Alignment Discipline**: `[Left-aligned narrative / centered dialog]`

---

## 15. Geometry & Border Radii
- **Tags & Badges**: `[e.g., 4px / 9999px]`
- **Buttons & Inputs**: `[e.g., 6px / 8px / 9999px]`
- **Cards & Containers**: `[e.g., 8px / 12px / 16px / 24px]`
- **Dialogs & Modals**: `[e.g., 12px / 16px / 20px]`
- **Border Stroke**: `[1px solid #XXXXXX]`

---

## 16. Elevation, Shadows & Depth Strategy
- **Depth Model**: `[Pure flat border-driven / multi-layer ambient occlusion / hard offset]`
- **Elevation Tokens**: Level 0 (flat), Level 1 (resting), Level 2 (hover/dropdown), Level 3 (modal overlay).

---

## 17. Imagery, Diagrams & Media Standards
- **UI Screenshot Standards**: Real domain data, syntactically valid code, 16:10 aspect ratio.
- **Diagram Standards**: Clean SVG linework, consistent stroke weights, semantic flow arrows.

---

## 18. Iconography Architecture
- **Library Selection**: `[Lucide / Phosphor / Custom SVG]`
- **Stroke Weight**: `[1.5px / 2.0px]`
- **Scale**: XS (12px), SM (16px), MD (20px), LG (24px).

---

## 19. Motion & Micro-Interactions
- **Fast / Micro-Interactions**: `120ms ease-out`
- **Normal / State Transitions**: `240ms cubic-bezier(0.16, 1, 0.3, 1)`
- **View Changes / Drawers**: `350ms cubic-bezier(0.16, 1, 0.3, 1)`
- **Reduced Motion**: Universal `@media (prefers-reduced-motion: reduce)` fallback protocol.

---

## 20. Responsive & Mobile Ergonomics
- **Breakpoints**: Mobile (<640px), Tablet (640–1024px), Desktop (1024–1440px), Ultrawide (>1440px).
- **Transformations**: Desktop data tables → stacked cards; top nav → bottom mobile drawer.
- **Touch Target Minimum**: Strictly $\ge 44\text{px} \times 44\text{px}$.

---

## 21. Accessibility & WCAG Verification
- **Contrast Ratios**: Verified WCAG AA / AAA compliance.
- **Focus Rings**: High-contrast 2px `:focus-visible` ring on all interactive elements.

---

## 22. Component Primitive Rules
- Specific behavioral and state rules for Buttons, Inputs, Cards, Navigation, Tabs, Modals, Tables, Badges, and Empty States.

---

## 23. Anti-Patterns & Deliberately Rejected Defaults
1. [Banned Default 1 with rationale]
2. [Banned Default 2 with rationale]
3. [Banned Default 3 with rationale]
4. [Banned Default 4 with rationale]

---

## 24. Design Decision Rationale Log
- 5-part rationale entries (Value, Role, Rationale, Usage, Avoid) for all major color, typography, and layout choices.

---

## 25. Reference Constellation & Code Integration Notes
- External references analyzed and principles extracted.
- CSS variable naming conventions and framework import structure.
