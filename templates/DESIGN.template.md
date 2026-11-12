# [Product Name] — Creative Direction & Design System Contract (DESIGN.md)

> **Persistent Creative & Engineering Contract for [Product Name]**  
> *Generated via Sloppi v2.0 Creative Direction Framework*

---

## 1. Product Context & Category Subversion
- **Operational Reality & Persona**: [Who uses this, what is the core mechanism, and what are the stakes?]
- **Primary 5-Second Interactive Goal**: [What live interactive proof or instrument does the user manipulate immediately upon landing?]
- **Category Clichés Explicitly Subverted**:
  - *Gen-1 AI Slop Rejected*: [e.g., Centered H1 + 2 pills, purple/cyan blur orbs, 3-card icon grids, fake testimonials]
  - *Gen-2 Wireframe Clichés Rejected*: [e.g., Sterile flat `1px`-bordered boxes everywhere, default `Inter` + `JetBrains Mono`, generic dark-green CLI terminal, repetitive `11px` uppercase mono eyebrows]

---

## 2. Live Reference Observations (`OBSERVED` vs. `OFFLINE_SYNTHESIS`)
- **Reference Mode**: `[OBSERVED (Live Browser / Search) | OFFLINE_SYNTHESIS]`
- **Reference 1 — `[Name / URL]`**:
  - *Observed Layout & Spatial Ratio*: [Exact grid/viewport mechanics observed]
  - *Observed Typography & Materiality*: [Font contrast, surface texture/lighting]
  - *Transferable Principle Extracted*: [The rule we are adapting]
- **Reference 2 — `[Name / URL]`**:
  - *Observed Motion / Interactive Hook*: [Choreography and state feedback observed]
  - *Transferable Principle Extracted*: [The mechanic we are adapting]

---

## 3. Three-Direction Creative Divergence (A vs. B vs. C)

| Dimension | Direction A: [Name] | Direction B: [Name] | Direction C: [Name] |
| :--- | :--- | :--- | :--- |
| **Visual Metaphor** | [Metaphor A] | [Metaphor B] | [Metaphor C] |
| **Spatial Layout** | [Layout structure A] | [Layout structure B] | [Layout structure C] |
| **Font Pairing** | [Display + Sans + Mono A] | [Display + Sans + Mono B] | [Display + Sans + Mono C] |
| **Palette & Materiality** | [Colors, lighting & texture A] | [Colors, lighting & texture B] | [Colors, lighting & texture C] |
| **5-Sec Interactive Hook** | [Interactive centerpiece A] | [Interactive centerpiece B] | [Interactive centerpiece C] |

- **Selected Winning Direction**: **[Direction A / B / C or Hybrid]**
- **Why It Won the Originality Gate**: [1–2 sentences explaining why this direction is unmistakably original, passes the Silhouette Squint Test, and avoids both SaaS templates and flat wireframes.]

---

## 4. Winning Design Thesis & Visual Tension
- **Design Thesis**: *[2–3 sentence point of view defining the physical/editorial metaphor, atmospheric mood, and signature craft.]*
- **Controlled Visual Tension**: `[e.g., Literary High-Contrast Serif + Precision Cartographic Telemetry]`

---

## 5. Expressive Typography Architecture
- **Display / Headline (`--font-display`)**: `[Font Family]`, weights, optical character rationale.
- **UI / Body (`--font-sans`)**: `[Font Family]`, weights, legibility rationale.
- **Monospace / Numerals (`--font-mono`)**: `[Font Family]`, `tabular-nums` enforcement.

| Semantic Token | Fluid Size (`clamp`) | Weight | Line-Height | Tracking | Usage Role |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `--text-hero` | `clamp(...)` | `...` | `0.90–0.98` | `-0.035em` | Primary viewport sculptural headline |
| `--text-h1` | `clamp(...)` | `...` | `1.00–1.06` | `-0.025em` | Major chapter & screen anchors |
| `--text-h2` | `clamp(...)` | `...` | `1.10–1.18` | `-0.020em` | Section headers (`text-wrap: balance`) |
| `--text-body-lg` | `clamp(...)` | `400` | `1.55` | `-0.005em` | Lead narrative copy (`max-width: 60ch`) |
| `--text-body` | `1rem (16px)` | `400` | `1.60` | `normal` | Standard reading & inputs (`max-width: 65ch`) |
| `--text-meta` | `0.75rem (12px)` | `500` | `1.35` | `+0.03em` | Coordinates, footnotes, status chips |

---

## 6. Color Palette, Surface Materiality & Lighting

| Semantic Token | Value (Hex / OKLCH) | Contrast & Material Role |
| :--- | :--- | :--- |
| `--color-canvas` | `#XXXXXX` | Primary ground plane |
| `--color-canvas-alt` | `#XXXXXX` | Chapter contrast ground |
| `--color-surface` | `#XXXXXX` | Elevated/recessed container surface |
| `--color-text-primary` | `#XXXXXX` | Primary reading ink (WCAG AAA $\ge 7:1$) |
| `--color-text-secondary` | `#XXXXXX` | Supporting copy (WCAG AA $\ge 4.5:1$) |
| `--color-text-muted` | `#XXXXXX` | Metadata & captions (WCAG AA $\ge 4.5:1$) |
| `--color-brand` | `#XXXXXX` | Primary interactive anchor & signature focal hue |
| `--color-brand-contrast` | `#XXXXXX` | Accessible text on `--color-brand` |
| `--color-border` | `#XXXXXX` | Structural hairlines / dividers |
| `--color-focus-ring` | `#XXXXXX` | `2px` high-visibility `:focus-visible` ring |

- **Materiality & Depth Recipe**: [Specify surface grain/texture, specular inner highlights, tactile elevation shadows, or chromatic blocking rules so the UI never looks like a flat wireframe.]

---

## 7. Spatial Composition, Grid & Section Cadence
- **Primary Viewport Architecture**: [Exact composition of the above-the-fold hero / core workspace prototyped in Stage 4.]
- **Chapter / Screen Progression**:
  1. **[Chapter/Screen 1]**: [Compositional structure, user job, interactive mechanic, ground tone]
  2. **[Chapter/Screen 2]**: [Distinct spatial structure—never repeat consecutive identical grids]
  3. **[Chapter/Screen 3]**: [Distinct spatial structure]
  4. **[Chapter/Screen 4]**: [High-conviction closure / conversion anchor]

---

## 8. Signature Interactive Centerpiece & Motion Physics
- **The 5-Second Interactive Centerpiece**: [Detailed behavior of the primary interactive widget/canvas/instrument.]
- **Motion & Spring Choreography**:
  - *Primary Spring*: `stiffness: ..., damping: ..., mass: ...`
  - *Reveal / Easing*: `cubic-bezier(0.16, 1, 0.3, 1)`
  - *Reduced Motion*: Full `@media (prefers-reduced-motion: reduce)` and `MotionConfig` support.

---

## 9. Component Anatomy & Interactive States
- **Buttons & Triggers**: Geometry, tactile hover/active response (`scale`, specular shift), primary vs. secondary hierarchy.
- **Inputs & Controls**: Recessed/elevated field styling, focus ring (`2px` offset), validation states.
- **Data & Domain Widgets**: Custom SVG schematics, tabular numeral alignment (`tabular-nums`), interactive states.

---

## 10. Responsive Ergonomics (`390px`–`1440px+`) & Accessibility Verification
- **Mobile (`390px`)**: Single-column ergonomic reflow, thumb-zone controls, $\ge 44\times 44\text{px}$ touch targets, zero horizontal overflow (`scrollWidth <= innerWidth`).
- **Tablet (`768px`) & Desktop (`1280px–1440px+`)**: Multi-column grid/workbench expansion and max-width framing.
- **Keyboard & Screen Reader**: Semantic HTML landmarks, full Tab traversal, visible `:focus-visible` outlines, ARIA live/modal bindings.
