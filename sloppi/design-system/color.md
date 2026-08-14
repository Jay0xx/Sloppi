# Sloppi Semantic Color Architecture

In Sloppi, color is governed strictly by **semantic roles** rather than arbitrary raw color values. 

Coding agents often fail at color by scattering ad-hoc utility classes (`bg-blue-500`, `text-slate-800`, `border-gray-200`) across components. This creates visual fragmentation, violates accessibility, and makes systematic theming impossible.

---

## 1. Raw Values vs. Semantic Roles

Sloppi enforces a two-tier color architecture:

```
[ Primitive Palette (Raw Values) ]
   e.g., #0b0d13 (tungsten-950), #00d084 (emerald-500), #f4f4f5 (zinc-100)
                  │
                  ▼
[ Semantic Role Assignment (Functional Tokens) ]
   e.g., --color-canvas, --color-accent-success, --color-surface-hover
                  │
                  ▼
[ Component Application ]
   e.g., background-color: var(--color-canvas); color: var(--color-text-primary);
```

### The Rule of Semantic Consumption
- **Components never consume raw hex codes or primitive palette names directly.**
- Components consume only semantic tokens that describe the functional purpose of the color.

---

## 2. The Canonical Semantic Color Taxonomy

Every Sloppi design system defines tokens across seven functional categories:

```
1. CANVAS & GROUNDS     ──► --color-canvas, --color-canvas-alt
2. SURFACES & CONTAINERS ──► --color-surface, --color-surface-hover, --color-surface-active
3. TYPOGRAPHIC CONTRAST ──► --color-text-primary, --color-text-secondary, --color-text-muted, --color-text-inverse
4. BRAND SIGNATURE      ──► --color-brand, --color-brand-hover, --color-brand-contrast
5. FUNCTIONAL ACCENTS   ──► --color-accent-info, --color-accent-success, --color-accent-warning, --color-accent-danger
6. BORDERS & DIVIDERS   ──► --color-border, --color-border-subtle, --color-border-hover
7. FOCUS & ACCESSIBILITY ──► --color-focus-ring
```

### Semantic Color Matrix

| Semantic Token | Purpose & Contrast Target | Example Application |
| :--- | :--- | :--- |
| `--color-canvas` | Base ground plane of the entire application. | `<body>` background, main layout canvas. |
| `--color-canvas-alt` | Subtle alternating ground for section rhythm. | Secondary feature sections, footer background. |
| `--color-surface` | Elevated or resting card/container fill. | Dashboard cards, popovers, modal bodies. |
| `--color-surface-hover` | Interactive card or list-item hover feedback. | Clickable table rows, navigation links. |
| `--color-text-primary` | Main reading text (WCAG AAA $\ge 7:1$). | Headings, primary body paragraphs, active labels. |
| `--color-text-secondary`| High readability supporting copy (WCAG AA $\ge 4.5:1$). | Subheadings, card descriptions, input labels. |
| `--color-text-muted` | Lower contrast metadata (WCAG AA $\ge 3:1$ for UI). | Timestamps, monospace tags, inactive tab text. |
| `--color-text-inverse` | Text on dark/brand fills (WCAG AA $\ge 4.5:1$). | Text inside primary brand buttons, dark tooltips. |
| `--color-brand` | Primary brand anchor & core conversion trigger. | Primary CTA button background, active tab indicators. |
| `--color-brand-hover` | Interactive state for primary brand actions. | Primary button hover/focus. |
| `--color-brand-contrast`| Accessible text color resting on `--color-brand`. | Text/icons inside `--color-brand` elements. |
| `--color-border` | Standard 1px structural container boundaries. | Card perimeters, input borders, header divider. |
| `--color-border-subtle`| Soft inner dividers within containers. | Table row dividers, inner card horizontal rules. |
| `--color-accent-info` | Informational status indicators & endpoints. | Info badges, API parameter highlights. |
| `--color-accent-success`| Positive status, verification, completed jobs. | Success badges, uptime indicators, diff additions. |
| `--color-accent-warning`| Caution, rate limits, non-critical alerts. | Warning alerts, near-capacity progress bars. |
| `--color-accent-danger` | Critical errors, destructive actions, failed jobs. | Delete buttons, validation errors, diff removals. |
| `--color-focus-ring` | High-visibility keyboard focus outline. | `:focus-visible` rings on all interactive controls. |

---

## 3. The 5-Part Design Rationale Schema

Every important color decision in `DESIGN.md` must be documented using the 5-part rationale schema:

```markdown
### Color Definition: [Semantic Role Name]
- **Value**: `[Hex / OKLCH / HSL Value]`
- **Role**: [Exact functional purpose in the interface]
- **Rationale**: [Why this specific hue/luminance was chosen based on the Design Thesis]
- **Usage**: [Where this color MUST be applied]
- **Avoid**: [Where this color MUST NOT be applied]
```

### Real-World Rationale Examples

#### Example A: Brand Signature Color (Developer Observability Tool)
- **Value**: `#00d084` (Phosphor Emerald)
- **Role**: Primary conversion trigger and live active telemetry indicator.
- **Rationale**: Provides high optical luminescence against the midnight tungsten canvas (`#0b0d13`) without causing color fatigue. Evokes vintage terminal phosphor displays while maintaining crisp modern contrast.
- **Usage**: Primary CTA buttons, live uptime telemetry dots, active tab bottom indicator.
- **Avoid**: Large background fills, card containers, body text paragraphs, or non-interactive decorative borders.

#### Example B: Canvas Ground Color (Boutique Private Wealth Platform)
- **Value**: `#fbf9f5` (Warm Alabaster)
- **Role**: Base page canvas ground plane.
- **Rationale**: Softens harsh stark-white glare, creating a tactile physical broadsheet material feel that conveys calm fiduciary stewardship.
- **Usage**: Body background, main page container.
- **Avoid**: Pure digital `#000000` text (use `#111625` Navy Ink instead to maintain warm harmony).

---

## 4. Accessibility & Environmental Constraints

- **Contrast Verification**: Primary reading text must achieve $\ge 7:1$ (AAA); secondary copy and interactive controls must achieve $\ge 4.5:1$ (AA); UI boundaries and large text must achieve $\ge 3:1$.
- **Color Blindness Redundancy**: Never convey critical system state (e.g., error vs. success) through color alone. Always pair color with an icon glyph or text label.
- **Dark / Light Contexts**: When building dual-mode interfaces, define semantic roles for both modes independently. Do not simply invert hex values with a mathematical filter.
