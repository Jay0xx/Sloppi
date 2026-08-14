# Sloppi Design Token Implementation & Traceability

Design Token Implementation translates the mathematical scales and semantic mappings established in `DESIGN.md` into machine-executable CSS custom properties and framework theme bindings.

A coding agent must never scatter raw unmapped hex values (`#3b82f6`), magic pixel margins (`margin-top: 37px`), or arbitrary font sizes across component markup. Every visual property must be traceable to a semantic token.

---

## 1. The 3-Tier Token Architecture

Sloppi enforces a clean, three-tier token separation to ensure maintainability and theme switching:

```
┌────────────────────────────────────────────────────────────────────────┐
│ TIER 1: GLOBAL / PRIMITIVE PALETTE                                     │
│ Raw values with zero semantic intent.                                  │
│ e.g., --palette-slate-950: #020617;  --palette-emerald-500: #10b981;   │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 2: SEMANTIC TOKENS (The Core Abstraction)                         │
│ Mappings that convey functional meaning, ground roles, and contrast.   │
│ e.g., --color-canvas: var(--palette-slate-950);                        │
│       --color-brand: var(--palette-emerald-500);                       │
│       --color-text-primary: #f8fafc;                                   │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 3: COMPONENT SCOPED VARIABLES (Optional / Contextual)             │
│ Overrides local to a specific interactive primitive.                   │
│ e.g., --btn-bg: var(--color-brand);  --input-border: var(--color-border│
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Canonical Token Implementation Template (`globals.css`)

```css
:root {
  /* ==========================================================================
     1. COLOR TAXONOMY (SEMANTIC)
     ========================================================================== */
  --color-canvas: #0c0e12;
  --color-canvas-alt: #13171f;
  --color-surface: #191f2b;
  --color-surface-hover: #222a3a;
  --color-surface-active: #2b3548;

  --color-text-primary: #f1f5f9;      /* WCAG AAA >= 7:1 on canvas */
  --color-text-secondary: #94a3b8;    /* WCAG AA >= 4.5:1 on canvas */
  --color-text-muted: #64748b;        /* WCAG AA >= 4.5:1 on surface */
  --color-text-inverse: #0f172a;

  --color-brand: #00f59b;             /* Brand signature action */
  --color-brand-hover: #00dc8b;
  --color-brand-contrast: #042014;

  --color-border: #263042;
  --color-border-subtle: #1e2533;
  --color-border-hover: #3b4863;
  --color-focus-ring: #00f59b;

  --color-accent-info: #38bdf8;
  --color-accent-success: #34d399;
  --color-accent-warning: #fbbf24;
  --color-accent-danger: #f87171;

  /* ==========================================================================
     2. TYPOGRAPHY SCALES & LEADING
     ========================================================================== */
  --font-display: 'Inter', system-ui, sans-serif;
  --font-body: 'Inter', system-ui, sans-serif;
  --font-mono: 'JetBrains Mono', ui-monospace, monospace;

  --font-size-display-2xl: 3.815rem; /* 61.04px */
  --font-size-display-xl: 3.052rem;  /* 48.83px */
  --font-size-heading-lg: 2.441rem;  /* 39.06px */
  --font-size-heading-md: 1.953rem;  /* 31.25px */
  --font-size-heading-sm: 1.563rem;  /* 25.00px */
  --font-size-body-lg: 1.250rem;     /* 20.00px */
  --font-size-body: 1.000rem;        /* 16.00px */
  --font-size-body-sm: 0.813rem;     /* 13.00px */
  --font-size-caption: 0.688rem;     /* 11.00px */

  --leading-display: 0.95;
  --leading-heading: 1.15;
  --leading-body: 1.60;
  --leading-tight: 1.20;

  --tracking-tight: -0.025em;
  --tracking-normal: 0.000em;
  --tracking-wide: 0.030em;

  /* ==========================================================================
     3. SPATIAL BASELINE & GAPS
     ========================================================================== */
  --space-1: 0.25rem;  /* 4px */
  --space-2: 0.50rem;  /* 8px */
  --space-3: 0.75rem;  /* 12px */
  --space-4: 1.00rem;  /* 16px */
  --space-6: 1.50rem;  /* 24px */
  --space-8: 2.00rem;  /* 32px */
  --space-12: 3.00rem; /* 48px */
  --space-16: 4.00rem; /* 64px */
  --space-24: 6.00rem; /* 96px */
  --space-32: 8.00rem; /* 128px */

  /* ==========================================================================
     4. GEOMETRY & CORNER RADII
     ========================================================================== */
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-xl: 16px;
  --radius-full: 9999px;

  /* ==========================================================================
     5. ELEVATION & DEPTH SHADOWS
     ========================================================================== */
  --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.40);
  --shadow-md: 0 4px 12px -2px rgba(0, 0, 0, 0.50), 0 2px 4px -2px rgba(0, 0, 0, 0.30);
  --shadow-lg: 0 12px 24px -4px rgba(0, 0, 0, 0.60), 0 4px 8px -2px rgba(0, 0, 0, 0.40);

  /* ==========================================================================
     6. MOTION & EASING
     ========================================================================== */
  --duration-fast: 120ms;
  --duration-normal: 240ms;
  --duration-slow: 350ms;
  --ease-snappy: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-standard: cubic-bezier(0.4, 0, 0.2, 1);
}
```

---

## 3. The Token Traceability Pipeline

Every visual property rendered in the DOM must trace back to a specific design decision:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. DESIGN.md RATIONALE                                                 │
│    "Dark tungsten canvas with phosphor green brand accent"             │
│                         │                                              │
│                         ▼                                              │
│ 2. SEMANTIC TOKEN DECLARATION                                          │
│    --color-brand: #00f59b;  --color-brand-contrast: #042014;           │
│                         │                                              │
│                         ▼                                              │
│ 3. COMPONENT IMPLEMENTATION                                            │
│    .btn-primary { background: var(--color-brand); color: var(...); }  │
│                         │                                              │
│                         ▼                                              │
│ 4. RENDERED USER INTERFACE                                             │
│    Pixel-perfect, high-contrast, accessible button                     │
└────────────────────────────────────────────────────────────────────────┘
```

If a future agent or developer inspects an element and asks: *"Why is this border 1px solid #263042?"*, the token name `--color-border` immediately points back to Section 12 of `DESIGN.md`.
