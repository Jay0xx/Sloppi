# Sloppi Component Behavior & Primitive Rules

Component rules define how abstract design tokens and visual principles translate into concrete, deterministic UI primitives.

In Sloppi, component rules eliminate ad-hoc decision-making during implementation. Every component primitive must have clearly defined anatomy, variants, interactive states, responsive behavior, and accessibility bindings.

---

## 1. Button Primitive Rules

### Anatomy
`[Leading Icon (optional)] + [Action Label] + [Trailing Icon (optional)]` inside a bounded interactive container.

### Variants & Semantic Roles
- **Primary Action**: Background: `var(--color-brand)`, Text: `var(--color-brand-contrast)`. Single dominant action per viewport.
- **Secondary Action**: Background: `transparent`, Border: `1px solid var(--color-border)`, Text: `var(--color-text-primary)`.
- **Ghost / Tertiary**: Background: `transparent`, Border: `none`, Text: `var(--color-text-secondary)`. Hover: `var(--color-surface-hover)`.
- **Destructive**: Background: `var(--color-accent-danger)`, Text: `#ffffff`. Reserved for permanent deletions/cancellations.

### Interactive State Matrix
- **Resting**: Height: `40px` (standard) / `32px` (compact), Padding: `0 var(--space-4)`, Radius: `var(--radius-md)`.
- **Hover**: Background brightness shift ($+10\%$ light / $-10\%$ dark); transition: `background-color var(--duration-fast) var(--ease-standard)`.
- **Active / Pressed**: `transform: scale(0.98)`; transition: `transform var(--duration-instant) var(--ease-standard)`.
- **Focus**: `outline: 2px solid var(--color-focus-ring); outline-offset: 2px;`.
- **Disabled**: `opacity: 0.5; pointer-events: none; cursor: not-allowed;`.

---

## 2. Form Input & Field Primitive Rules

### Anatomy
`[Field Label]` + `[Input Container with Optional Leading/Trailing Glyphs]` + `[Helper Text / Validation Error]`.

### State Specifications
- **Resting**: Background: `var(--color-surface)`, Border: `1px solid var(--color-border)`, Radius: `var(--radius-md)`, Text: `var(--color-text-primary)`. Height: `40px`.
- **Focus**: Border: `1px solid var(--color-brand)`, Box-Shadow / Ring: `0 0 0 3px var(--color-brand-subtle)`.
- **Error**: Border: `1px solid var(--color-accent-danger)`, Error Text: `var(--color-accent-danger)` with `aria-invalid="true"`.
- **Disabled**: Background: `var(--color-canvas-alt)`, Border: `1px solid var(--color-border-subtle)`, Text: `var(--color-text-muted)`.

---

## 3. Card & Surface Primitive Rules

### Variants
- **Flush / Flat Card**: Background: `var(--color-surface)`, Border: `1px solid var(--color-border)`, Shadow: `none`.
- **Elevated Card**: Background: `var(--color-surface)`, Border: `1px solid var(--color-border)`, Shadow: `var(--elevation-1)`.
- **Interactive Action Card**: Elevates to `var(--elevation-2)` on hover with subtle border luminance transition.

### Internal Spacing
- Compact Density: Padding: `var(--space-3)` (`12px`)
- Comfortable Density: Padding: `var(--space-6)` (`24px`)
- Spacious Editorial: Padding: `var(--space-8)` (`32px`)

---

## 4. Navigation & Wayfinding Primitives

### Header Bar
- Height: `64px` desktop / `56px` mobile.
- Sticky Behavior: `position: sticky; top: 0; z-index: 50; backdrop-filter: blur(12px); background-color: var(--color-canvas-alpha); border-bottom: 1px solid var(--color-border);`.
- Link Spacing: Horizontal gap: `var(--space-6)` (`24px`). Active link: `color: var(--color-text-primary); font-weight: 600;`. Inactive link: `color: var(--color-text-secondary);`.

### Mobile Navigation Transformation
- Bottom-docked tab bar (`56px` height) with icon + micro-label or slide-up bottom drawer.

---

## 5. Tab & Segmented Control Primitives

### Variants
- **Segmented Pill Bar**: Encapsulated track (`background: var(--color-canvas-alt); padding: 4px; border-radius: var(--radius-full)`). Active pill: `background: var(--color-surface); box-shadow: var(--elevation-1); border-radius: var(--radius-full);`.
- **Underline Tabs**: Flush horizontal row. Active tab features a `2px` bottom border line in `var(--color-brand)`.

---

## 6. Modal Dialog & Drawer Primitives

### Anatomy
`[Scrim Overlay]` + `[Dialog Box: Header with Title & Close Icon] + [Body Container] + [Footer Action Bar]`.

### Behavior & Constraints
- Dialog Box: Max-width: `560px` (standard) / `720px` (wide), Radius: `var(--radius-xl)`, Shadow: `var(--elevation-3)`, Border: `1px solid var(--color-border)`.
- Animation: Backdrop fades in (`200ms ease-out`); Dialog scales up from `0.96` to `1.00` (`250ms cubic-bezier(0.16, 1, 0.3, 1)`).
- Accessibility: Focus trapped within dialog; `Esc` key dismisses; `aria-modal="true"`.

---

## 7. Data Table & Grid Primitives

- **Header Row**: Height: `36px`, Background: `var(--color-canvas-alt)`, Typography: `text-xs font-mono uppercase tracking-wider text-muted-foreground`, Border-bottom: `1px solid var(--color-border)`.
- **Data Rows**: Height: `44px` (comfortable) / `32px` (compact), Border-bottom: `1px solid var(--color-border-subtle)`.
- **Numeric Alignment**: All currency, percentage, and latency columns must be **right-aligned** with `font-variant-numeric: tabular-nums; font-family: var(--font-mono);`.

---

## 8. Badge & Status Chip Primitives

- **Geometry**: Height: `22px`, Padding: `0 8px`, Radius: `var(--radius-full)` or `var(--radius-xs)`, Typography: `text-xs font-mono font-medium`.
- **Semantic Tints**:
  - *Success*: Background: `rgba(0, 208, 132, 0.12)`, Text: `#00d084`.
  - *Warning*: Background: `rgba(255, 171, 0, 0.12)`, Text: `#ffab00`.
  - *Danger*: Background: `rgba(255, 77, 79, 0.12)`, Text: `#ff4d4f`.
  - *Neutral*: Background: `var(--color-canvas-alt)`, Text: `var(--color-text-secondary)`.

---

## 9. Empty State & Loading State Primitives

### Empty State
`[Illustration / Micro-HUD Icon]` + `[Clear Descriptive Headline]` + `[1-sentence explanation of what to do next]` + `[Primary Creation CTA]`.

### Loading States
- **Skeleton Loaders**: Muted placeholder shapes (`background: var(--color-surface-hover)`) with a subtle linear-gradient shimmer wave (`1.5s infinite`).
- **Disabled Actions**: Maintain layout dimensions; never collapse buttons during network operations.
