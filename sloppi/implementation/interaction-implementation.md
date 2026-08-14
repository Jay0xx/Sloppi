# Sloppi Interaction & State Implementation

Interaction Implementation governs how interactive components communicate state, feedback, and keyboard navigation to the user.

A coding agent must never build static "dead" components that lack hover feedback, omit focus indicators, or invent chaotic animations that trigger cognitive fatigue.

---

## 1. The 12 Canonical Component States

Every interactive primitive (Button, Input, Card, Link, Tab, Modal) must account for its relevant states:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. RESTING / DEFAULT   ──► Clean base token styling                    │
│ 2. HOVER (:hover)      ──► Subtle brightness or surface tint shift     │
│ 3. FOCUS (:focus-visible) ─► 2px high-contrast focus ring with offset  │
│ 4. ACTIVE / PRESSED    ──► Subtle scale(0.98) tactile compression      │
│ 5. SELECTED / CURRENT  ──► Persistent active indicator (aria-selected) │
│ 6. DISABLED            ──► cursor: not-allowed; opacity: 0.45;         │
│ 7. LOADING / BUSY      ──► aria-busy="true"; inline spinner, disabled  │
│ 8. SUCCESS             ──► Transient green accent / checkmark fade-in  │
│ 9. ERROR / INVALID     ──► aria-invalid="true"; red border + message   │
│ 10. EXPANDED / OPEN    ──► aria-expanded="true"; height transition     │
│ 11. DRAG / ACTIVE HOLD ──► Elevated shadow-lg + cursor: grabbing       │
│ 12. FOCUSED WITHIN     ──► Container-level focus highlight             │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. The Focus Visibility Mandate

Keyboard accessibility is non-negotiable. Sloppi strictly prohibits removing focus outlines with `outline: none`:

```css
/* Universal High-Contrast Focus Ring Protocol */
:focus-visible {
  outline: 2px solid var(--color-focus-ring);
  outline-offset: 2px;
}

/* Button Component State Implementation Example */
.btn-primary {
  background-color: var(--color-brand);
  color: var(--color-brand-contrast);
  font-family: var(--font-body);
  font-size: var(--font-size-body-sm);
  font-weight: 600;
  padding: var(--space-2) var(--space-4);
  border-radius: var(--radius-md);
  border: 1px solid transparent;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--space-2);
  transition: background-color var(--duration-fast) var(--ease-snappy),
              transform var(--duration-fast) var(--ease-snappy),
              box-shadow var(--duration-fast) var(--ease-snappy);
}

.btn-primary:hover:not(:disabled) {
  background-color: var(--color-brand-hover);
  box-shadow: var(--shadow-sm);
}

.btn-primary:active:not(:disabled) {
  transform: scale(0.98);
}

.btn-primary:disabled {
  opacity: 0.45;
  cursor: not-allowed;
  pointer-events: none;
}
```

---

## 3. Purposeful Motion & Easing Curves

Motion in Sloppi exists to **orient the user, communicate state changes, and provide physical continuity**—never as decorative amusement.

### Motion Duration Standards
- **Micro-Interactions (Hovers, Toggles, Buttons)**: `120ms` (`--duration-fast`)
- **State Transitions (Tabs, Dropdowns, Accordions)**: `240ms` (`--duration-normal`)
- **Spatial Overlays (Drawers, Modals, Fullscreen Views)**: `350ms` (`--duration-slow`)

### Standard Easing Bezier
- **Snappy Settling Curve**: `cubic-bezier(0.16, 1, 0.3, 1)` (instant acceleration followed by smooth, natural deceleration).

### Reduced Motion Compliance
```css
@media (prefers-reduced-motion: reduce) {
  *, ::before, ::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```
