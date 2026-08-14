# Sloppi Design Token Model

This document defines the mathematical and semantic taxonomy for design tokens within the Sloppi system.

Tokens represent the fundamental visual variables of an application. Rather than using raw magic numbers in component styling, agents define semantic tokens in `DESIGN.md` and translate them into native CSS custom properties or theme configuration objects.

---

## 1. Color Token Taxonomy

Color tokens must always be separated into two tiers: **Primitive Values** and **Semantic Roles**.

```
[ Primitive Palette ] (e.g., slate-900, blue-600, emerald-500)
         │
         ▼
[ Semantic Role Assignment ] (e.g., bg-canvas, text-primary, border-muted)
         │
         ▼
[ Component Application ] (e.g., button-primary-bg, card-border)
```

### Semantic Token Roles

| Token Name | Semantic Role | Rationale & Usage Example |
| :--- | :--- | :--- |
| `--color-canvas` | Base page background | The main canvas ground plane (e.g., `#ffffff` or `#0a0b0e`). |
| `--color-canvas-alt` | Secondary section background | Alternating ground to establish scroll rhythm without lines. |
| `--color-surface` | Card / Container fill | Elevated or resting card background. |
| `--color-surface-hover` | Interactive card hover fill | Feedback for hoverable elements. |
| `--color-text-primary` | Main reading text | Highest contrast against canvas (WCAG AAA >= 7:1). |
| `--color-text-secondary`| Supporting descriptions | High readability, medium contrast (WCAG AA >= 4.5:1). |
| `--color-text-muted` | Metadata, captions, labels | Lower contrast for non-essential annotations (WCAG AA >= 3:1 for large/UI). |
| `--color-brand` | Primary brand anchor | Signature brand hue for primary actions and active states. |
| `--color-brand-contrast`| Text on brand fill | Ensures accessible reading on brand-colored buttons. |
| `--color-border` | Structural divider lines | Standard 1px perimeter boundaries. |
| `--color-border-subtle`| Soft inner dividers | Table row borders, subtle card splits. |
| `--color-accent-info` | Informational status | Endpoint indicators, info callouts. |
| `--color-accent-success`| Success status / positive | Completed builds, positive performance metrics. |
| `--color-accent-warning`| Warning status / caution | Rate limit alerts, deprecation notices. |
| `--color-accent-danger` | Error / Destructive action | Deletion buttons, failed test traces. |
| `--color-focus-ring` | Keyboard focus outline | High-visibility focus indicator for accessibility. |

---

## 2. Typography Token Scale

Typography tokens are governed by a mathematical modular scale calculated from a base font size ($16\text{px}$ or $1rem$).

### Standard Scale Multipliers
- **Minor Third ($1.200$)**: Recommended for high-density tools, dashboards, and complex web apps where space is tight.
- **Major Third ($1.250$)**: Recommended for standard marketing sites and balanced SaaS products.
- **Perfect Fourth ($1.333$)**: Recommended for editorial, portfolio, and high-impact marketing layouts with large display contrast.

### Token Scale Architecture

| Token Name | Scale Step | Base 16px (Major Third 1.250) | Line-Height | Letter-Spacing | Intended Semantic Assignment |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `--font-display-2xl`| Step +6 | `61px` / `3.81rem` | `0.90–0.98` | `-0.030em` | Hero visual anchor, single wordmark punchlines |
| `--font-display-xl` | Step +5 | `49px` / `3.05rem` | `1.00–1.05` | `-0.025em` | Page hero headlines (H1) |
| `--font-heading-lg` | Step +4 | `39px` / `2.44rem` | `1.10–1.15` | `-0.020em` | Section primary headers (H2) |
| `--font-heading-md` | Step +3 | `31px` / `1.95rem` | `1.20–1.25` | `-0.015em` | Subsection titles, feature headings (H3) |
| `--font-heading-sm` | Step +2 | `25px` / `1.56rem` | `1.30–1.35` | `-0.010em` | Card titles, modal headers (H4) |
| `--font-body-lg` | Step +1 | `20px` / `1.25rem` | `1.50–1.55` | `-0.005em` | Lead paragraphs, hero subheads |
| `--font-body` | Step 0 | `16px` / `1.00rem` | `1.55–1.65` | `normal` | Standard body copy, inputs, table content |
| `--font-body-sm` | Step -1 | `13px` / `0.80rem` | `1.45–1.50` | `+0.010em` | Navigation items, button text, secondary info |
| `--font-caption` | Step -2 | `11px` / `0.69rem` | `1.40–1.45` | `+0.030em` | Monospace tags, status timestamps, uppercase labels |

---

## 3. Spatial & Layout Tokens

Spacing follows a consistent $4\text{px}$ or $8\text{px}$ geometric unit:

```
--space-1:   4px
--space-2:   8px
--space-3:  12px
--space-4:  16px
--space-6:  24px
--space-8:  32px
--space-12: 48px
--space-16: 64px
--space-24: 96px
--space-32: 128px
```

### Layout Macro Tokens
- `--layout-max-width`: Maximum container constraint (e.g., `1200px`, `1440px`, or `100%`).
- `--layout-section-gap`: Vertical rhythm between major content sections (`64px` to `128px`).
- `--layout-card-padding`: Internal padding for content cards (`16px` compact, `24px` comfortable, `32px` spacious).
- `--layout-element-gap`: Spacing between adjacent UI controls (`8px` to `16px`).

---

## 4. Geometry & Elevation Tokens

### Border Radii
- `--radius-none`: `0px`
- `--radius-sm`: `4px` (tags, badge chips, code snippets)
- `--radius-md`: `8px` (inputs, buttons, select menus)
- `--radius-lg`: `12px` (cards, containers, table wrappers)
- `--radius-xl`: `16px` (modal dialogs, floating drawer sheets)
- `--radius-full`: `9999px` (pill badges, circular avatars, toggle switches)

### Elevation & Shadow Tokens
- `--shadow-flat`: `none`, relying strictly on `1px solid var(--color-border)`.
- `--shadow-subtle`: `0 1px 2px 0 rgba(0, 0, 0, 0.05)` (resting cards).
- `--shadow-elevated`: `0 4px 6px -1px rgba(0, 0, 0, 0.08), 0 2px 4px -2px rgba(0, 0, 0, 0.04)` (hover states, dropdown menus).
- `--shadow-modal`: `0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.05)` (modals, overlays).

---

## 5. Motion Tokens

- `--duration-instant`: `100ms` (checkbox toggle, button click press)
- `--duration-fast`: `150ms` (hover state color shifts, tooltip appearance)
- `--duration-normal`: `250ms` (dropdown expansion, accordion fold, modal fade)
- `--duration-slow`: `400ms` (page view transition, drawer slide-in)
- `--ease-standard`: `cubic-bezier(0.16, 1, 0.3, 1)` (snappy entry, natural settle)
- `--ease-out`: `cubic-bezier(0, 0, 0.2, 1)`
- `--ease-in-out`: `cubic-bezier(0.4, 0, 0.2, 1)`
