# Sloppi Color Taxonomy & Contrast Audit

The Color Audit verifies that rendered colors strictly follow the two-tier semantic taxonomy established in `DESIGN.md`, pass mathematical WCAG contrast thresholds, and avoid chaotic accent overuse.

---

## 1. The 6-Point Color Audit Checklist

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. WCAG CONTRAST VERIFICATION  ──► Body text >= 4.5:1 (AA);            │
│                                    Primary text >= 7:1 (AAA).          │
│ 2. STRICT SEMANTIC ROLES       ──► Brand color strictly for primary    │
│                                    actions; muted text for metadata.   │
│ 3. ZERO ACCENT OVERUSE         ──► Brand/accent color occupies <= 5%   │
│                                    of total viewport surface area.     │
│ 4. GROUND PLANE HIERARCHY      ──► Clear alternation between Base      │
│                                    (--color-canvas) & Alt grounds.     │
│ 5. ZERO UNMAPPED RAW HEX CODES ──► Zero ad-hoc #3b82f6 codes in CSS.   │
│ 6. FUNCTIONAL ACCENT DISCIPLINE──► Red/Amber/Green used strictly for   │
│                                    real status/alerts, not decoration. │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Color Deficiency Catalog & Fixes

| Color Flaw | Diagnostic Symptom | Severity | Sloppi Remediation |
| :--- | :--- | :--- | :--- |
| **Failing Text Contrast** | Secondary text on dark surface has contrast ratio of $2.8:1$, failing WCAG AA. | **BLOCKER** | Lighten text token to `--color-text-secondary` with verified $\ge 4.5:1$ contrast. |
| **Accent Saturation Fatigue** | Brand emerald green is used for buttons, card borders, badge fills, icons, and titles. | **HIGH** | Restrain brand color strictly to Tier 4 Primary CTA and active indicator chips. |
| **Unmapped Inline Hex Codes** | Developer inserted `color: #6366f1` directly in a component instead of a design token. | **MEDIUM** | Replace with semantic variable `var(--color-brand)` or `var(--color-accent-info)`. |
| **Muddy Ground Planes** | Card surface (`--color-surface`) has identical hex code to backdrop canvas, losing depth. | **MEDIUM** | Adjust surface fill to be distinctly elevated (e.g. Canvas `#0c0e12` $\longrightarrow$ Surface `#191f2b`). |
| **Rainbow Alert Clutter** | A single card uses 5 different accent colors (purple, pink, cyan, green, yellow). | **MEDIUM** | Consolidate to a disciplined monochrome palette with a single semantic accent. |
