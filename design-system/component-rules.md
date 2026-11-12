# Sloppi v2.0 Adaptive Component Anatomy & State Rules

Component primitives must **embody your project's Creative Direction**, never force every website into the same `40px`-tall, `8px`-rounded wireframe box.

While **accessibility and state completeness are universal**, **silhouette, surface physics, and typography must adapt** to your winning direction in `DESIGN.md`.

---

## 1. Adaptive Component Silhouettes by Art Direction

| Primitive | Editorial Broadsheet / Monograph | Tactile Industrial / Hardware | Kinetic Poster / Neo-Brutalist | Atmospheric Spatial Canvas |
| :--- | :--- | :--- | :--- | :--- |
| **Primary Trigger / Button** | Sharp or subtle pill (`0px` or `9999px`), high-contrast ink fill, italicized serif or crisp grotesque label, directional arrow motion. | Beveled physical key (`6px–10px` radius), `inset 0 1px 0 rgba(255,255,255,0.4)` top specular edge, tactile `active:translate-y-[1px]`. | Bold chromatic block, `0px` or pill radius, `2px solid` ink border, hard offset shadow (`4px 4px 0 #111`) that collapses on press. | Luminous surface fill with subtle perimeter glow or refractive border, magnetic hover physics (`scale(1.02)` / `active:scale(0.98)`). |
| **Containers & Surfaces** | Borderless whitespace grouping, fine `1px` column hairlines, or recessed warm paper wells (`--color-canvas-alt`). | Recessed dark telemetry wells (`inset 0 2px 4px rgba(0,0,0,0.35)`) inside brushed metallic or matte panels. | Exposed architectural grid cells (`gap-px`) or overlapping sticker cards with crisp `2px` outlines. | Multi-layered tonal depth with `1px` top specular highlight and subtle SVG noise grain. |
| **Section Introductions** | Large italicized serif chapter numerals (`I`, `II` or `01`) + flush-left editorial running heads. | Laser-etched coordinate indices (`[SYS.01]`) + LED status indicator dot. | Oversized bleed display typography or vertical rotated margin headers. | Subtle optical index + fluid scroll-linked reveal headline. |

---

## 2. Universal 6-State Interactive Matrix (Mandatory for Every Control)

Regardless of aesthetic archetype, every interactive primitive (`Button`, `Input`, `Tab`, `Select`, `Row`, `Card Trigger`) must implement six deterministic states:

1. **Resting**: Clear affordance signaling interactivity through contrast, surface elevation, or border definition.
2. **Hover (`:hover`)**: Immediate optical response (`120ms–180ms` or spring)—surface luminance shift, directional icon translation, or border contrast elevation.
3. **Keyboard Focus (`:focus-visible`)**: Unmistakable `2px solid var(--color-focus-ring)` with `2px` `outline-offset`. Never `outline: none` without a high-contrast replacement.
4. **Active / Pressed (`:active` / `whileTap`)**: Physical tactile response (`scale(0.98)` or `translateY(1px)`).
5. **Loading / Pending**: Preserves exact button/container dimensions (`min-width`) with inline spinner or progress trace; prevents double-submission.
6. **Disabled (`:disabled` / `aria-disabled`)**: Lowered contrast (`opacity: 0.45`), `cursor: not-allowed`, no hover lift.

---

## 3. Navigation, Wayfinding & Mobile Transformation

- **Desktop Wayfinding**: Match navigation geometry to content architecture—editorial masthead with date/edition coordinates, compact floating command island, persistent studio sidebar dock, or Swiss architectural top bar.
- **Mobile Ergonomics (`< 768px`)**:
  - Never cram 6 desktop links into a tiny wrapping header.
  - Transform into a **thumb-zone bottom navigation dock** (`60px–68px` height) or a **physics-driven bottom sheet / full-screen editorial index drawer** with $\ge 44\times 44\text{px}$ tap targets.

---

## 4. Data Visualization, Schematics & Tables

- **Bespoke SVG Schematics Over Generic Icon Boxes**: When explaining a product mechanism, build an interactive SVG schematic, scrubbable chart, or live parameter control rather than three static icon cards.
- **Numeric Discipline**: Enforce `font-variant-numeric: tabular-nums` and right-alignment on all dynamic counters, financial columns, latency readouts, and axis labels so live updates never cause horizontal layout jitter.
