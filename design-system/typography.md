# Sloppi v2.0 Expressive Typography & Scale Architecture

Typography is the single fastest way to establish an unmistakable visual identity—and the #1 place where coding agents default to generic mediocrity.

> **THE ANTI-MONOCULTURE FONT RULE (v2.0)**:
> Never blindly default to `'Inter'`, `'Roboto'`, `'Plus Jakarta Sans'`, or `system-ui` paired with `'JetBrains Mono'` and `11px uppercase tracking-widest` labels on every project.
> Your font pairing must actively express your chosen **Creative Direction**.

---

## 1. Curated High-Character Font Pairings by Art Direction

Load Google Fonts / web fonts explicitly in the project layout (`next/font/google` or `@import` / `<link>`) so your typography actually renders with character:

| Art Direction Archetype | Display / Headline Font (`--font-display`) | UI / Body Font (`--font-sans`) | Monospace / Data Font (`--font-mono`) | Visual Character & Ideal Domain |
| :--- | :--- | :--- | :--- | :--- |
| **1. Editorial Broadsheet & Institutional Luxury** | `Instrument Serif`, `Newsreader`, or `Playfair Display` (with expressive italics) | `Plus Jakarta Sans` or `DM Sans` | `IBM Plex Mono` | High-contrast literary authority; ideal for wealth/fintech subversions, research labs, cultural platforms, luxury commerce. |
| **2. Swiss Neo-Brutalist & Kinetic Poster** | `Syne`, `Unbounded`, or `Archivo Black` | `Space Grotesk` or `Switzer` | `Space Mono` or `JetBrains Mono` | Monumental geometric weight & poster tension; ideal for creative studios, Web3 protocols, design tools, bold launches. |
| **3. Industrial Precision & Hardware Instrument** | `Space Grotesk`, `Chakra Petch`, or `Rajdhani` | `IBM Plex Sans` or `Inter Tight` | `JetBrains Mono` or `Fira Code` | Machined technical clarity; ideal for hardware interfaces, audio synths, robotics, telemetry workbenches. |
| **4. Warm Humanist & Tactile Studio** | `Fraunces` (variable optical size/softness) or `Bricolage Grotesque` | `Work Sans` or `Figtree` | `Commit Mono` or `Inconsolata` | Warm, approachable, human-crafted; ideal for consumer apps, health/wellness, editorial SaaS, education, creator tools. |
| **5. Contemporary Geometric & Architectural** | `Outfit`, `Sora`, or `Manrope` | `DM Sans` or `Geist` | `Geist Mono` or `IBM Plex Mono` | Crisp modern architectural geometry without generic Bootstrap vibes; ideal for modern workflows, spatial canvases, cloud platforms. |
| **6. Scientific Monograph & Cartographic** | `Cormorant Garamond` or `EB Garamond` | `Source Sans 3` or `Public Sans` | `Source Code Pro` or `IBM Plex Mono` | Archival Bell-Labs / academic monograph aesthetic; ideal for AI research, cryptography, climate tech, deep-tech engines. |

---

## 2. Dynamic Scale Ratios (Never Lock Every Site to 1.250)

Choose a mathematical scale multiplier that matches your spatial composition—and use fluid `clamp()` sizing so display typography commands real presence on desktop while adapting cleanly to `390px` mobile:

- **High-Density Workbench / HUD ($1.150 - 1.200$ Minor Third)**: Compact control surfaces where viewport real estate is sacred.
- **Balanced Application & Product Flow ($1.250$ Major Third)**: Multi-screen web apps and interactive dashboards.
- **Editorial, Poster & High-Impact Storytelling ($1.333$ Perfect Fourth to $1.500$ Perfect Fifth)**: Dramatic scale contrast between monumental display anchors (`clamp(3.25rem, 7.5vw, 6.5rem)`) and disciplined `16px` body copy.

### Fluid Typographic Scale Reference

| Semantic Role | Fluid CSS `clamp()` Formula | Line-Height (`leading`) | Letter-Spacing (`tracking`) | Usage Guidance |
| :--- | :--- | :--- | :--- | :--- |
| `--font-display-hero` | `clamp(2.75rem, 6.5vw + 1rem, 5.75rem)` | `0.90 – 0.98` | `-0.035em` to `-0.045em` | Primary viewport visual anchor; sculpted tight leading. |
| `--font-display-xl` | `clamp(2.25rem, 4.5vw + 0.75rem, 4.00rem)` | `0.98 – 1.05` | `-0.025em` to `-0.035em` | Major chapter statements, oversized data readouts. |
| `--font-heading-lg` | `clamp(1.75rem, 2.8vw + 0.5rem, 2.75rem)` | `1.08 – 1.15` | `-0.020em` | Section primary headings (H2) with `text-wrap: balance`. |
| `--font-heading-md` | `clamp(1.35rem, 1.8vw + 0.4rem, 1.85rem)` | `1.18 – 1.25` | `-0.015em` | Feature sub-anchors and interactive panel titles (H3). |
| `--font-body-lg` | `clamp(1.125rem, 0.5vw + 0.95rem, 1.30rem)` | `1.50 – 1.60` | `-0.005em` | Lead narrative paragraphs (`max-width: 60ch`). |
| `--font-body` | `1rem` (`16px`) | `1.55 – 1.65` | `normal` | Sustained reading copy and form inputs (`max-width: 65ch`). |
| `--font-body-sm` | `0.875rem` (`14px`) | `1.45` | `+0.005em` | Interactive controls, compact table rows, secondary notes. |
| `--font-meta` | `0.75rem` (`12px`) | `1.35` | `+0.02em` to `+0.06em` | Coordinates, footnotes, status badges (do NOT overuse on every heading!). |

---

## 3. Expressive Typographic Choreography

Instead of treating text as static paragraphs inside boxes, use typography as an active visual medium:
1. **Mixed-Voice Headlines**: Combine roman grotesque with an italicized high-contrast serif keyword or an inline interactive pill/sparkline inside the H1 itself.
2. **Index & Coordinate Framing**: Frame sections with large editorial numerals (`01`, `02`), margin citations, or live data coordinates rather than repetitive pill badges.
3. **Tabular Numeric Discipline (`tabular-nums`)**: Enforce `font-variant-numeric: tabular-nums` on all live counters, scrubbable charts, clocks, and financial figures so interactive updates never jitter horizontally.
4. **Optical Line Balancing**: Apply `text-wrap: balance` to headings and `text-wrap: pretty` to body copy, strictly capping reading measure at `60ch–68ch`.
