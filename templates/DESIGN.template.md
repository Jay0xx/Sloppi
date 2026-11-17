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

## 2. Live Reference Observations (`OBSERVED`, `[INFERRED]`, or `OFFLINE_SYNTHESIS`)
- **Reference Mode**: `[OBSERVED (Live Browser / Search) | PARTIAL (mark [INFERRED] items) | OFFLINE_SYNTHESIS]`
- **Reference 1 — `[Registry Source / Deep Link URL]`**:
  - *Observed Behavior or Composition*: [Exact layout, typographic hierarchy, or interaction observed in actual example/clip]
  - *Motion Capture (if applicable)*: Trigger `[...]` · Moves `[...]` · Anchored `[...]` · Settles `[...]` *(tag unverified values `[INFERRED]`)*
  - *Design Principle Worth Adapting*: [Transferable rule extracted]
  - *Where It Serves This Product*: [Exact screen, section, or product moment]
- **Reference 2 — `[Registry Source / Deep Link URL]`**:
  - *Observed Behavior or Composition*: [...]
  - *Design Principle Worth Adapting & Product Fit*: [...]

---

## 3. Three-Direction Creative Divergence (A vs. B vs. C)

| Dimension | Direction A: [Name — e.g., Quiet / Hierarchy-Led] | Direction B: [Name — e.g., Section / Domain-Led] | Direction C: [Name — e.g., Motion-Led / Spatial] |
| :--- | :--- | :--- | :--- |
| **Composition Choice** | [Layout structure A] | [Layout structure B] | [Layout structure C] |
| **Typography Choice** | [Display + Sans + Mono A] | [Display + Sans + Mono B] | [Display + Sans + Mono C] |
| **Interaction Choice** | [Quiet hierarchy & spacing / minimal motion] | [Focused micro-feedback at specific controls] | [Motion-led: product moment improving feedback, orientation, or continuity] |
| **Palette & Materiality** | [Colors, lighting & texture A] | [Colors, lighting & texture B] | [Colors, lighting & texture C] |

- **Selected Winning Direction**: **[Direction A / B / C or Hybrid]**
- **Why It Won the Originality Gate**: [1–2 sentences explaining why this direction is unmistakably original, fits the product moment, and avoids both SaaS templates and flat wireframes.]

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

## 8. Intended Behavior, Motion Contract & Stack Fit
- **Product Moment & Intended Behavior**: [What this interaction clarifies—feedback, orientation, or continuity—or explicitly note "Quiet direction: hierarchy & spacing carry order with minimal motion."]
- **Stack Fit, Dependency Cost & License**: [Native CSS / View Transitions / `motion` / etc.; bundle cost, peer constraints, and license check—never auto-adopt demo packages]
- **Proposed Effect Specification**:
  - *Trigger*: [Event, gesture, or threshold]
  - *End State & Anchors*: [What moves, what stays anchored, how it settles]
  - *Touch Behavior*: [Tap/drag ergonomics, $\ge 44\times 44\text{px}$ target, zero hover dependency]
  - *Keyboard Behavior*: [`Tab`/`Enter`/`Space`/`Escape` parity, visible `:focus-visible`, focus preserved]
  - *Repeated Activation*: [Mid-flight cancellation/reversal safety, no queued backlog]
  - *Reduced Motion*: [`@media (prefers-reduced-motion: reduce)` / `MotionConfig` behavior preserving state clarity]
- **Verification Plan**: Prototyped inside primary composition; **screenshots** for layout/hierarchy + **browser recording or interaction trace** for timing/continuity.

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
