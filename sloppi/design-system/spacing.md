# Sloppi Spatial Architecture & Density Scale

Spacing is the mathematical grammar of visual rhythm. In Sloppi, spacing establishes hierarchical grouping, optical balance, and density calibration.

A coding agent must never use arbitrary magic numbers (`margin-top: 19px; padding: 27px; gap: 43px`). Every spatial offset must derive from a coherent geometric baseline scale calibrated to the project's required information density.

---

## 1. The 3 Spatial Density Archetypes

The spatial baseline and scaling factors are determined by the product's operational density model:

```
[ Compact Density ]      ──► 4px Base Unit (Data-dense tools, code consoles, spreadsheets)
[ Comfortable Density ]  ──► 8px Base Unit (Standard SaaS workflows, customer dashboards)
[ Spacious Density ]     ──► 8px/12px Base (Editorial broadsheets, luxury landing pages)
```

### Density Scale Comparison

| Spatial Dimension | Compact Density (4px base) | Comfortable Density (8px base) | Spacious Density (Editorial) |
| :--- | :--- | :--- | :--- |
| **Card Internal Padding** | `12px – 16px` | `24px` | `32px – 48px` |
| **Element Control Gap** | `4px – 8px` | `12px – 16px` | `16px – 24px` |
| **Section Vertical Gap** | `32px – 48px` | `64px – 80px` | `96px – 144px` |
| **Table Cell Padding** | `6px vertical / 12px horiz` | `12px vertical / 16px horiz` | `16px vertical / 24px horiz` |
| **Container Max-Width** | `100% / 1440px` | `1200px` | `1024px – 1200px` |

---

## 2. The Canonical Spacing Token Scale

Sloppi structures spatial tokens as multiples of the baseline unit. Below is the canonical 8px-based token progression (with sub-unit 4px/2px tokens for fine micro-spacing):

| Token Name | Value (px / rem) | Intended Semantic Assignment |
| :--- | :--- | :--- |
| `--space-0-5` | `2px / 0.125rem` | Micro border alignment, badge offsets |
| `--space-1` | `4px / 0.25rem` | Icon-to-text gap in compact badges, tight table paddings |
| `--space-2` | `8px / 0.50rem` | Element gap inside button groups, input internal vertical padding |
| `--space-3` | `12px / 0.75rem` | Form label-to-input gap, compact card padding |
| `--space-4` | `16px / 1.00rem` | Standard card internal padding, standard form field spacing |
| `--space-6` | `24px / 1.50rem` | Comfortable card padding, subsection gap, modal body padding |
| `--space-8` | `32px / 2.00rem` | Spacious card padding, inter-component stack gap |
| `--space-12` | `48px / 3.00rem` | Compact section gap, major feature block spacing |
| `--space-16` | `64px / 4.00rem` | Standard section vertical rhythm |
| `--space-24` | `96px / 6.00rem` | Spacious section vertical rhythm, hero top/bottom padding |
| `--space-32` | `128px / 8.00rem` | Major narrative chapter transitions |

---

## 3. The 5 Tiers of Spatial Application

To prevent spatial ambiguity, agents categorize spacing across five explicit architectural tiers:

```
1. MICRO SPACING (2px – 8px)      ──► Inside badges, between icon and label, input padding
2. COMPONENT SPACING (8px – 16px)  ──► Between buttons in a toolbar, between form fields
3. CONTENT SPACING (16px – 32px)   ──► Inside cards, between heading and paragraph
4. SECTION SPACING (48px – 96px)   ──► Vertical margin separating major content sections
5. PAGE SPACING (24px – 128px)     ──► Horizontal page gutters, viewport edge margins
```

---

## 4. Whitespace as an Active Structural Force

In Sloppi, whitespace is not empty unused canvas; it is an active structural tool that eliminates decorative clutter:
- **Macro-Whitespace**: Generous vertical spacing ($96\text{px}–128\text{px}$) between major narrative sections allows users to mentally reset between chapters without needing artificial horizontal divider lines.
- **Proximity Grouping**: Spacing between related items (e.g., an H3 title and its paragraph: $8\text{px}$) must always be significantly smaller than spacing to the next unrelated section ($32\text{px}$).
- **The Container Subtraction Rule**: If whitespace alone creates unambiguous visual grouping, delete the card border and background container.

---

## 5. Responsive Spacing Transitions

Spatial tokens must scale smoothly across viewport sizes. Section padding that feels generous on a $1440\text{px}$ desktop creates excessive empty scrolling on a $375\text{px}$ mobile screen:

```css
:root {
  --section-gap: var(--space-24); /* 96px on desktop */
  --page-gutter: var(--space-8);  /* 32px on desktop */
}

@media (max-width: 768px) {
  :root {
    --section-gap: var(--space-12); /* 48px on mobile */
    --page-gutter: var(--space-4);  /* 16px on mobile */
  }
}
```
