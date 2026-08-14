# DESIGN.md: StrataDB Developer Infrastructure Landing

## 1. Product & Domain Context
- **Product**: StrataDB — Embedded, Globally Replicated NVMe Key-Value Storage Engine.
- **Audience**: Systems engineers, backend architects, database platform teams.
- **Operational Stakes**: High-stakes database infrastructure; data loss is fatal.
- **Primary Conversion**: `curl -sSL https://get.stratadb.dev | sh` & Deploy Cluster.

## 2. Design Thesis & Visual Tension
- **Thesis**: *"Tungsten Machined Precision meets Phosphor Terminal Telemetry."*
- **Visual Tension**: Dense, authoritative technical typography paired with an unhurried, calm monochromatic canvas.

## 3. Visual Language & Density
- **Personality Axes**: Restrained (9/10), Technical (10/10), Precise (10/10), Calm (8/10).
- **Density Mode**: Dense HUD (compact padding, high information density, tabular metrics).

## 4. Mathematical Typography Scale (Major Third — 1.250)
- `font-mono`: `'JetBrains Mono', 'Fira Code', monospace`
- `font-sans`: `'Inter', -apple-system, sans-serif`
- `--font-size-hero`: `clamp(2.5rem, 5vw, 4.0rem)` (Leading: `1.05`, `tracking: -0.03em`)
- `--font-size-h1`: `2.441rem` (`39px`, Leading: `1.15`)
- `--font-size-h2`: `1.953rem` (`31px`, Leading: `1.20`)
- `--font-size-body`: `1.0rem` (`16px`, Leading: `1.55`, `max-width: 65ch`)
- `--font-size-caption`: `0.8rem` (`12.8px`, Leading: `1.40`)

## 5. Semantic Color Roles & WCAG Rationale
- `--color-bg-canvas`: `#0B0D11` (Deep dark tungsten base)
- `--color-bg-surface`: `#14171F` (Elevated card/terminal surface)
- `--color-text-primary`: `#F0F3F8` (14.2:1 contrast against canvas — WCAG AAA)
- `--color-text-secondary`: `#9BA3AF` (5.6:1 contrast against canvas — WCAG AA)
- `--color-accent`: `#22C55E` (Phosphor Green — 4.9:1 contrast for terminal prompt)
- `--color-border-subtle`: `#222733` (Razor 1px structural grid lines)
- `--color-focus-ring`: `#60A5FA` (2px high-contrast electric blue outline)

## 6. Spatial Baseline (4px/8px System)
- `--space-1`: `4px`
- `--space-2`: `8px`
- `--space-3`: `12px`
- `--space-4`: `16px`
- `--space-6`: `24px`
- `--space-8`: `32px`
- `--space-12`: `48px`
- `--space-16`: `64px`

## 7. Geometry & Concentric Radii
- `--radius-outer`: `8px` (Outer terminal window)
- `--radius-inner`: `4px` (Inner code blocks & buttons — Formula: $R_{outer} - P$)
- `--radius-badge`: `2px` (Precision technical labels)

## 8. Elevation & Depth
- Ambient subtle border definition with layered drop shadows:
  `box-shadow: 0 4px 20px -2px rgba(0, 0, 0, 0.5), 0 0 0 1px var(--color-border-subtle);`

## 9. Content Architecture & Section Cadence
1. **Hero**: Left-aligned headline + Live Interactive CLI REPL (Direct Interactive Sandbox).
2. **Telemetry Matrix**: Real benchmark IOPS throughput counter against RocksDB/LMDB.
3. **Architecture Section**: 8+4 Asymmetric Bento (SVG dataflow schematic + Consensus state machine).
4. **Code Integration**: Tabbed Python/Rust/Go SDK quickstart snippets.
5. **Footer**: Clean technical index with cluster status latency badge.

## 10. Accessibility & Interaction Guardrails
- Universal `:focus-visible { outline: 2px solid var(--color-focus-ring); outline-offset: 2px; }`.
- Mobile touch targets $\ge 44\times 44\text{px}$.
- Body paragraph measure strictly capped at $65\text{ch}$.
- Zero generic 3-card grid reflexes; zero vague buzzwords.
