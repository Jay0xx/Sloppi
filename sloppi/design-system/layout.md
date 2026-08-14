# Sloppi Layout & Composition Architecture

Layout is the spatial architecture that organizes information, establishes scanning hierarchy, and guides the user through a digital interface.

A coding agent must never default to automatic centered layouts, generic 12-column grids, or repetitive 3-column card rows. Every layout structure must directly support the product's narrative, interaction model, or data density.

---

## 1. Structural Layout vs. Decorative Layout

Sloppi enforces a strict distinction between structural and decorative layout:

| Dimension | Structural Layout (Essential) | Decorative Layout (Slop) |
| :--- | :--- | :--- |
| **Definition** | Spatial grouping governed by reading hierarchy, user workflow, and data relationships. | Artificial boxes, floating widgets, and asymmetric tilts added purely to make a layout look "busy". |
| **Purpose** | Minimizes cognitive friction; directs focus to primary actions and key data points. | Disguises weak content; creates visual noise and misaligns reading order. |
| **Test** | If all colors and borders are removed, the layout remains completely clear and legible. | If borders are removed, the content becomes an unreadable jumble. |

---

## 2. Layout Grid Models by Product Archetype

Sloppi selects layout systems based on functional requirements:

```
1. ASYMMETRIC BENTO GRID   ──► Feature showcases, visual differentiators, product dashboards
2. DENSE MULTI-COLUMN DOCK ──► Developer terminals, IDEs, data analysis, spreadsheets
3. ASYMMETRIC 2-COLUMN     ──► Editorial essays, high-trust fintech, long-form narratives
4. SINGLE-COLUMN STREAM    ──► Linear onboarding, checkout funnels, focused distraction-free forms
```

### Grid Characteristics & Applications

#### 1. Asymmetric Bento Grid
- **Structure**: Unequal modular cells (e.g., 65% width hero cell + 35% auxiliary cell; two 50% bottom cells).
- **Application**: Landing page feature sections where one core capability deserves primary visual dominance over supporting features.
- **Rule**: Never use identical, repetitive card dimensions when the content within them has unequal importance.

#### 2. Dense Multi-Column Dock (HUD Layout)
- **Structure**: Fixed sidebar navigation ($240\text{px}–280\text{px}$) + flexible fluid canvas + collapsable inspector panel ($320\text{px}$).
- **Application**: Complex developer tools, telemetry dashboards, canvas editors.
- **Rule**: Maximize horizontal screen efficiency; lock viewport height ($100\text{vh}$) with internal scroll containers for tables and logs.

#### 3. Asymmetric 2-Column Editorial Grid
- **Structure**: 35% sticky left rail (headline, summary, anchor navigation) + 65% scrolling right column (deep narrative content, code examples, data breakdown).
- **Application**: Documentation portals, API guides, luxury portfolio storytelling, private banking overviews.

---

## 3. Section Composition & Narrative Rhythm

To prevent "section fatigue" (where every section looks like the previous one), Sloppi mandates **Section Modulation**:

```
[ Hero: High-Impact Visual Entry Point (Interactive Canvas or Terminal) ]
                               │
                               ▼
[ Chapter 1: Dense Comparative Proof (Benchmark Table / Architecture Flow) ]
                               │
                               ▼
[ Chapter 2: Spacious Editorial Break (Pull-Quote / Brand Philosophy) ]
                               │
                               ▼
[ Chapter 3: Interactive Sandbox / Feature Deep Dive (Tabbed Explorer) ]
                               │
                               ▼
[ Page Closure: High-Contrast Focused Action Container (CTA Anchor) ]
```

### Anti-Monotony Guardrails
- **No Consecutive Identical Grids**: Never stack two consecutive rows of 3-column cards. Follow a 3-column comparison with a full-width interactive demonstration or a 2-column asymmetric split.
- **Ground Tone Alternation**: Alternate section backgrounds between `--color-canvas` and `--color-canvas-alt` to establish natural chapter boundaries without relying on heavy horizontal lines.

---

## 4. Container Max-Widths & Alignment Rules

- **Application Canvas Max-Width**:
  - *Data Dashboards & Terminals*: `1440px` to `1600px` (or fluid `100%` with fixed margins).
  - *SaaS Marketing & Landing Pages*: `1200px` to `1280px`.
  - *Editorial & Long-Form Reading*: `720px` to `840px` (or `65ch` text measure).
- **Alignment Discipline**:
  - Default to **left-aligned** typography and section titles. Left-alignment creates a strong vertical optical anchor for Western reading patterns.
  - Reserve center-alignment strictly for standalone single-purpose utility modals, short status announcements, or minimal hero headlines. Never center-align long body paragraphs.
