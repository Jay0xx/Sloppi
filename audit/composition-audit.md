# Sloppi Composition & Spatial Cadence Audit

The Composition Audit inspects how elements, containers, whitespace, and structural chapters are arranged spatially across the entire vertical and horizontal canvas.

The goal is not to maximize visual complexity, but to ensure that **spatial composition directly reinforces narrative progression and eliminates visual monotony**.

---

## 1. The 6 Dimensions of Compositional Review

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. ALIGNMENT & STRUCTURAL AXIS ──► Strict left-aligned narrative anchor│
│                                    vs. centered standalone closures.   │
│ 2. ASYMMETRIC GRID BALANCE     ──► 12-column subgrid variations        │
│                                    (8+4 / 7+5 / 2-column split).       │
│ 3. SECTION RHYTHM & MODULATION ──► Dynamic alternation of height,      │
│                                    density, and ground tones.          │
│ 4. MACRO-WHITESPACE GRAVITY    ──► Purposeful negative space framing   │
│                                    critical assertions (96px–128px).   │
│ 5. MICRO-SPATIAL GROUPING      ──► Law of Proximity (related items     │
│                                    tighter than container boundaries). │
│ 6. SEAMLESS CHAPTER TRANSITIONS──► Refined 1px dividers, ground shifts,│
│                                    zero harsh jarring breaks.          │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Common Compositional Failure Modes & Fixes

| Compositional Flaw | Visual Diagnostic Indicator | Severity | Sloppi Remediation |
| :--- | :--- | :--- | :--- |
| **Section Cadence Monotony** | 4 consecutive sections all have identical 600px height, 64px padding, and identical gray backgrounds. | **HIGH** | Modulate section heights ($320\text{px} \longleftrightarrow 850\text{px}$), alternate ground planes (`--color-canvas` $\longleftrightarrow$ `--color-canvas-alt`), and vary container widths. |
| **Monolithic Symmetry** | Every section uses a centered heading with a 3-column symmetrical card grid underneath. | **HIGH** | Introduce asymmetric bento layouts (1 dominant hero card + 3 micro tiles) or 2-column editorial splits. |
| **Violated Law of Proximity** | Headline is closer to the previous section border (80px) than to its own supporting paragraph (96px). | **MEDIUM** | Enforce spatial grouping: paragraph gap = `var(--space-4)` (16px); section header gap = `var(--space-16)` (64px). |
| **Dead Space / Visual Void** | A massive 240px vertical gap separates two elements with no intentional gravitas or narrative reason. | **MEDIUM** | Tighten macro-gap to `var(--space-24)` ($96\text{px}$) and verify that negative space functions as deliberate punctuation. |
| **Cramped Content Traps** | Data tables or terminal code blocks squeezed into small card containers with $8\text{px}$ padding. | **MEDIUM** | Expand data containers to wide layout measure (`max-w-7xl` or full-bleed) with comfortable $24\text{px}$ internal padding. |
