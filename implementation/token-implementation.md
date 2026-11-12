# Sloppi v2.0 Design Token Implementation & Multi-Archetype Templates

Design tokens translate your chosen **Creative Direction** (`DESIGN.md`) into CSS custom properties and framework theme bindings.

> **CRITICAL RULE (v2.0)**:
> Never copy-paste a single default palette (`#0c0e12` dark tungsten + `#00f59b` green) or default font (`Inter` + `JetBrains Mono`) across projects. Your `:root` tokens must reflect the specific **Direction (A, B, or C)** that won your 3-Direction Divergence pass.

---

## 1. The Semantic Token Contract

Every component consumes semantic variables (`var(--color-canvas)`, `var(--font-display)`) rather than hardcoded hex codes. Define tokens across 6 pillars:
1. **Canvas, Surfaces & Materiality** (`--color-canvas`, `--color-canvas-alt`, `--color-surface`, `--color-surface-elevated`, `--surface-highlight`, `--surface-grain-opacity`)
2. **Typographic Contrast Tiers** (`--color-text-primary`, `--color-text-secondary`, `--color-text-muted`, `--color-text-inverse`)
3. **Brand Signature & Chromatic Accents** (`--color-brand`, `--color-brand-hover`, `--color-brand-contrast`, `--color-accent-1`, `--color-accent-2`)
4. **Structural Hairlines, Specular Bevels & Focus** (`--color-border`, `--color-border-strong`, `--color-focus-ring`)
5. **Expressive Font Stacks & Fluid `clamp()` Scales** (`--font-display`, `--font-sans`, `--font-mono`, `--text-hero`, `--text-h1`, etc.)
6. **Spatial Rhythm, Geometry & Spring Motion** (`--radius-*`, `--shadow-*`, `--ease-out-expo`, `--ease-spring`)

---

## 2. Three Reference Token Palettes (Adapt, Never Blindly Copy)

### Archetype I: Archival Editorial & Scientific Monograph (Warm Vellum + Cobalt + Vermilion)
```css
:root {
  --color-canvas: #F6F3EC;
  --color-canvas-alt: #EDE8DD;
  --color-surface: #FAF8F3;
  --color-surface-hover: #F0ECE1;

  --color-text-primary: #141413;      /* 15.8:1 AAA on canvas */
  --color-text-secondary: #4A4842;    /* 7.4:1 AAA on canvas */
  --color-text-muted: #767268;        /* 4.6:1 AA on canvas */
  --color-text-inverse: #F6F3EC;

  --color-brand: #0038A8;             /* Archival Blueprint Cobalt */
  --color-brand-hover: #002B80;
  --color-brand-contrast: #FFFFFF;
  --color-signal: #D9381E;            /* Oxidation Vermilion focal signal */

  --color-border: #D8D2C5;
  --color-border-strong: #141413;
  --color-focus-ring: #0038A8;

  --font-display: var(--font-instrument-serif), 'Playfair Display', Georgia, serif;
  --font-sans: var(--font-space-grotesk), system-ui, sans-serif;
  --font-mono: var(--font-commit-mono), 'IBM Plex Mono', monospace;
}
```

### Archetype II: Tactile Industrial Hardware (Anodized Aluminum + Carbon Wells + Amber Signal)
```css
:root {
  --color-canvas: #E4E6EB;
  --color-canvas-alt: #D6D9E0;
  --color-surface: #EEF0F4;
  --color-surface-recessed: #181A1F;  /* Recessed LED/Oscilloscope well */

  --color-text-primary: #111317;
  --color-text-secondary: #454B54;
  --color-text-muted: #68707C;
  --color-text-inverse: #F3F4F6;

  --color-brand: #FF4F00;             /* Industrial International Orange */
  --color-brand-hover: #E04500;
  --color-brand-contrast: #FFFFFF;

  --color-border: #C5C9D3;
  --surface-specular: inset 0 1px 0 0 rgba(255, 255, 255, 0.75);
  --shadow-tactile: 0 2px 4px rgba(17, 19, 23, 0.10), 0 1px 1px rgba(17, 19, 23, 0.06);
  --color-focus-ring: #FF4F00;

  --font-display: var(--font-syne), 'Space Grotesk', sans-serif;
  --font-sans: var(--font-ibm-plex-sans), system-ui, sans-serif;
  --font-mono: var(--font-jetbrains-mono), monospace;
}
```

### Archetype III: Atmospheric Optical Obsidian (Deep Perceptual Dark + Specular Glass + Warm Gold/Coral)
```css
:root {
  --color-canvas: #09080C;
  --color-canvas-alt: #111017;
  --color-surface: #171520;
  --color-surface-hover: #211E2E;

  --color-text-primary: #F5F2EB;
  --color-text-secondary: #B0A99F;
  --color-text-muted: #7C756D;
  --color-text-inverse: #09080C;

  --color-brand: #F26440;             /* Warm Solar Coral */
  --color-brand-hover: #FF7857;
  --color-brand-contrast: #09080C;

  --color-border: rgba(245, 242, 235, 0.10);
  --surface-specular: inset 0 1px 0 0 rgba(245, 242, 235, 0.14);
  --color-focus-ring: #F26440;

  --font-display: var(--font-fraunces), Georgia, serif;
  --font-sans: var(--font-dm-sans), system-ui, sans-serif;
  --font-mono: var(--font-geist-mono), monospace;
}
```

---

## 3. Universal Fluid Scale & Motion Tokens

Include fluid typography and easing variables in `:root` so layout rhythm and interactive choreography stay cohesive across all components:

```css
:root {
  /* Fluid Typographic Scale */
  --text-hero: clamp(2.75rem, 6.5vw + 1rem, 5.75rem);
  --text-h1: clamp(2.25rem, 4.5vw + 0.75rem, 4.00rem);
  --text-h2: clamp(1.75rem, 2.8vw + 0.5rem, 2.75rem);
  --text-h3: clamp(1.35rem, 1.8vw + 0.4rem, 1.85rem);
  --text-body-lg: clamp(1.125rem, 0.5vw + 0.95rem, 1.30rem);
  --text-body: 1rem;
  --text-sm: 0.875rem;
  --text-meta: 0.75rem;

  /* Choreographed Motion Curves */
  --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-in-out-quart: cubic-bezier(0.76, 0, 0.24, 1);
  --duration-fast: 150ms;
  --duration-normal: 280ms;
  --duration-cinematic: 600ms;
}
```
