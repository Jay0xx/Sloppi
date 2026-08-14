# Sloppi Design Reasoning Framework

Design reasoning is the disciplined cognitive process by which a coding agent translates a product description, target audience, and functional requirements into an intentional, cohesive visual system.

Coding agents often fail at design because they jump directly from a prompt ("Build a SaaS landing page for an API monitor") to raw CSS generation (`bg-slate-900 text-white rounded-lg p-6 flex flex-col items-center`). This bypasses design reasoning and defaults to statistical averages.

Sloppi enforces a structured 6-stage reasoning pipeline:

```
1. Product & Audience Analysis
               │
               ▼
2. Formulation of Design Thesis
               │
               ▼
3. Constraint & Ergonomic Mapping
               │
               ▼
4. Visual Synthesis & Token Definition
               │
               ▼
5. Layout Architecture & Narrative Pacing
               │
               ▼
6. Creation of Persistent DESIGN.md
```

---

## Stage 1: Product & Audience Analysis

Before choosing a single color or font, the agent must interrogate the product context across four dimensions:

### 1. Operational Stakes & Trust Level
- **Low Stakes / Casual**: Social apps, music visualizers, personal journals, hobbyist tools. Visual language can be playful, experimental, high-color, unconventional geometry.
- **Medium Stakes / Productivity**: Project management, team communication, marketing automation. Visual language prioritizes high legibility, clear workflows, and comfortable density.
- **High Stakes / Mission-Critical**: Developer infrastructure, medical tools, security auditing, financial settlement. Visual language requires uncompromising data clarity, high information density, precise typography, monospaced alignment, and zero frivolous ornamentation.

### 2. User Persona & Mental Model
- What tools does this audience live in?
  - A Linux systems engineer lives in terminals and text editors. They value keyboard shortcuts, tight monospace tables, and muted contrast over splashy animated cards.
  - A fashion brand marketer lives in Instagram, Figma, and print magazines. They value generous whitespace, high-impact editorial typography, and polished photography.
  - A healthcare professional values contrast, error prevention, scan-friendly data hierarchy, and calm neutrals.

### 3. Primary Value Proposition Dynamic
- **Demonstrative**: The product must be seen in action to be understood (e.g., video editor, code generator, canvas design tool). *Hero must feature an active interactive canvas or live demo.*
- **Analytical**: The value is in insights and data depth (e.g., analytics engine, fraud detector). *Hero and features must showcase high-density data visualizations, benchmark comparisons, and real telemetry.*
- **Ecosystem / Utility**: The value is in connectivity and simplicity (e.g., payments gateway, auth SDK). *Hero must showcase copyable code integration, SDK tabs, and architectural wiring diagrams.*

---

## Stage 2: Formulation of Design Thesis

The **Design Thesis** is a single-sentence visual point of view that governs all aesthetic decisions. It establishes the physical or emotional metaphor for the interface.

### Examples of Weak vs. Strong Design Theses

| Product | Weak Generic Thesis | Strong Sloppi Design Thesis |
| :--- | :--- | :--- |
| **API Load Testing Tool** | "A modern, clean dark-mode developer website with nice gradients." | *"A high-density telemetry console: midnight tungsten canvas, crisp phosphor-green latency indicators, monospaced tabular alignment, and zero decorative glassmorphism."* |
| **Boutique Coffee Subscription** | "A clean minimalist store with coffee images and cards." | *"An editorial broadsheet on textured warm paper: high-contrast serif headlines, asymmetric multi-column layout, and rich earth-tone accents."* |
| **Decentralized Wallet** | "A crypto web3 website with purple neon glow and 3D coins." | *"A tactile sticker-book universe: soft pastel sky background, crushed heavy display typography, 1px solid black hand-cut outlines, and pill-shaped controls."* |

Every token, component, and layout rule defined in the subsequent stages must derive from and support this thesis.

---

## Stage 3: Constraint & Ergonomic Mapping

Visual choices are not arbitrary artistic preferences; they are mathematical and ergonomic responses to constraints:

### 1. Spatial Density & Base Unit
- Choose a base spatial unit ($4\text{px}$ or $8\text{px}$) and stick to its multiples ($4, 8, 12, 16, 24, 32, 48, 64, 96\text{px}$).
- Map density to task complexity:
  - **Compact Density**: $4\text{px}$ base, $12\text{px}–16\text{px}$ card padding, $4\text{px}–8\text{px}$ element gaps. Used for data-dense dashboards, code tools, and spreadsheets.
  - **Comfortable Density**: $8\text{px}$ base, $24\text{px}–32\text{px}$ card padding, $16\text{px}–24\text{px}$ element gaps. Used for general SaaS workflows and account settings.
  - **Spacious / Editorial Density**: $8\text{px}$ base, $48\text{px}–80\text{px}$ section gaps, $32\text{px}–48\text{px}$ card padding. Used for landing pages, portfolios, and marketing storytelling.

### 2. Geometry & Corner Radii Scale
- Define a cohesive geometric progression rather than mixing random pixel values:
  - **Sharp / Technical**: `0px`–`4px` (industrial, terminal, tabular, brutalist).
  - **Balanced / Modern**: `6px` for small controls, `8px` for inputs/buttons, `12px` for cards, `16px` for dialogs.
  - **Soft / Organic**: `16px` for cards, `24px` for modals, `9999px` (pill) for interactive badges and action buttons.

---

## Stage 4: Visual Synthesis & Semantic Token Definition

Sloppi agents do not invent random hex codes in stylesheet selectors. Agents define a semantic token hierarchy where every color has a documented role.

### 1. Semantic Color Taxonomy
- **Canvas / Background**: Ground plane upon which all content rests (e.g., `#ffffff`, `#090a0f`, `#f7f5f0`).
- **Foreground / Primary Text**: Main reading contrast (WCAG AAA compliant against Canvas).
- **Muted Text / Secondary**: Subtitles, metadata, captions (WCAG AA compliant).
- **Brand Primary**: The signature brand anchor used for primary CTAs and active states.
- **Accents**: 1–4 defined secondary hues for distinct semantic categories (e.g., Amber for warnings, Emerald for success, Cyan for technical endpoints).
- **Border / Divider**: Structural boundary lines with explicit opacity or hex.
- **Card / Surface**: Elevated or indented content planes.

### 2. Typography Rationale & Scale Architecture
- **Font Pairing Rationale**: Pair at most two typeface families (e.g., a high-character Display font with a neutral UI/Body font, or a single variable font with contrasting optical weights).
- **Type Scale Ratio**: Select a mathematical scale (e.g., Minor Third $1.200$, Major Third $1.250$, Perfect Fourth $1.333$) from a defined base (e.g., $16\text{px}$).
- **Line-Height Proportions**:
  - Display / Hero Headlines ($48\text{px}–96\text{px}$): Tight leading ($0.85–1.05$) to prevent awkward spacing between stacked display words.
  - Section Headings ($24\text{px}–40\text{px}$): Medium leading ($1.10–1.25$).
  - Body Text ($14\text{px}–18\text{px}$): Generous leading ($1.50–1.65$) for optimal sustained readability.
  - Monospace Data / Code ($12\text{px}–14\text{px}$): Strict uniform line-height ($1.40–1.50$) to align tabular rows.

---

## Stage 5: Layout Architecture & Narrative Pacing

An interface is not a random collection of widgets; it is an organized sequence of visual and informational moments.

### 1. The Above-the-Fold Entry Point
- Determine the entry point based on Stage 1:
  - If the product solves an immediate friction, place the interactive solution directly into the hero.
  - If the product introduces a novel paradigm, lead with clear editorial framing followed by a visual diagram.

### 2. Rhythm and Modulation
- Avoid "card fatigue" where every section is a 3-column card grid.
- Modulate section pacing:
  - **Dense Data / Proof Section** (e.g., comparative benchmark table)
  - **Spacious Editorial Break** (e.g., large pull-quote or focused brand statement)
  - **Interactive Deep Dive** (e.g., tabbed feature sandbox with live code preview)
  - **High-Contrast Conversion Anchor** (e.g., focused CTA container)

---

## Stage 6: Creation of Persistent DESIGN.md

All design reasoning must be crystallized into a project-level `DESIGN.md` before any application code or UI components are written.

The `DESIGN.md` acts as a **persistent contract**. It guarantees that during subsequent implementation, refactoring, and feature expansion, the agent (or future agents) will maintain strict visual coherence and adhere to the established design thesis.
