# Sloppi Geometry & Shape Architecture

Geometry defines the physical curvature, border weight, and silhouette of user interface elements. In Sloppi, geometry reinforces the brand's tactile metaphor and visual language.

A coding agent must never blindly apply a single arbitrary radius (e.g., `rounded-2xl` on everything) without understanding the geometric hierarchy between nested components.

---

## 1. The 3 Geometric Archetypes

The overarching geometry model derives from the product's visual language and operational stakes:

```
[ Sharp / Industrial ] ──► 0px – 4px Radii (Terminals, trading consoles, brutalist editorial)
[ Balanced / Precision ]──► 6px – 12px Radii (Modern SaaS, enterprise workflows, productivity)
[ Soft / Tactile ]      ──► 16px – 9999px Radii (Consumer social, playful audio, casual mobile)
```

### Geometric Archetype Breakdown

| Dimension | Sharp / Industrial | Balanced / Precision | Soft / Tactile |
| :--- | :--- | :--- | :--- |
| **Tags & Badges** | `0px – 2px` | `4px` | `9999px` (Pill) |
| **Buttons & Inputs** | `2px – 4px` | `6px – 8px` | `9999px` (Pill) or `12px` |
| **Cards & Panels** | `4px` | `10px – 12px` | `20px – 28px` |
| **Modal Dialogs** | `6px` | `14px – 16px` | `28px – 36px` |
| **Border Stroke** | `1px solid` crisp hairline | `1px solid` subtle tone | `1px – 2px` hand-cut carbon outline |

---

## 2. The Nested Geometry Proportionality Rule

A fundamental geometric flaw in AI-generated interfaces is setting identical corner radii on nested containers (e.g., placing a 16px rounded button inside a 16px rounded card). This causes optical corner crowding and visual distortion.

### The Concentric Radius Formula
When an inner element sits inside an outer container with padding $P$:

$$\text{Radius}_{\text{inner}} = \max\left(0, \text{Radius}_{\text{outer}} - P\right)$$

*Example*: If an outer card has a border radius of $16\text{px}$ and internal padding of $12\text{px}$, the nested image or button should have a corner radius of $4\text{px}$ ($16 - 12 = 4\text{px}$). This maintains perfect concentric visual curvature.

---

## 3. The Canonical Geometry Token Scale

Sloppi structures border radii into a standard semantic scale:

| Token Name | Balanced Value | Purpose & Application |
| :--- | :--- | :--- |
| `--radius-none` | `0px` | Full-bleed sections, flush table borders, sharp dividers |
| `--radius-xs` | `2px` | Micro status dots, fine code tags, compact checkboxes |
| `--radius-sm` | `4px` | Monospace tags, status pills, inline code wrappers |
| `--radius-md` | `8px` | Form inputs, standard buttons, select menus, dropdowns |
| `--radius-lg` | `12px` | Standard cards, content containers, table wrappers |
| `--radius-xl` | `16px` | Floating drawer panels, modal dialogs, popovers |
| `--radius-full`| `9999px` | Pill badges, circular user avatars, switch toggles |

---

## 4. Border Thickness & Stroke Logic

- **1px Hairline (`1px solid var(--color-border)`)**: The standard structural boundary for 90% of professional interfaces. Defines clean separation without adding visual weight.
- **2px Accent Stroke (`2px solid var(--color-brand)`)**: Reserved strictly for active selection states, focused input outlines, or intentional tactile/sticker-book art direction.
- **Subtle Dividers (`1px solid var(--color-border-subtle)`)**: Used for interior table rows and list dividers; rendered with lowered opacity (e.g., `rgba(255,255,255,0.08)` or `rgba(0,0,0,0.06)`).
