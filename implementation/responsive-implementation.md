# Sloppi Responsive Implementation & Viewport Ergonomics

Responsive Implementation translates the responsive design rules from `DESIGN.md` into adaptive, touch-ergonomic frontend code.

Sloppi rejects the naive AI definition of responsive design (*"just set width to 100% and stack everything into a single column"*). Responsive design is **compositional and ergonomic refactoring**.

---

## 1. The 5 Core Responsive Transformation Types

When transitioning across viewport breakpoints, the agent must execute intentional structural transformations:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. NAVIGATION TRANSFORMATION                                           │
│ Desktop: Horizontal top navigation bar with search & actions.          │
│ Mobile:  Compact top header + fixed bottom action dock / drawer.       │
├────────────────────────────────────────────────────────────────────────┤
│ 2. DATA TABLE TRANSFORMATION                                           │
│ Desktop: 6-column tabular comparison matrix with sticky headers.       │
│ Mobile:  Stacked key-value specification cards with accordion details. │
├────────────────────────────────────────────────────────────────────────┤
│ 3. ASYMMETRIC BENTO TRANSFORMATION                                     │
│ Desktop: 12-column subgrid (col-span-8 hero tile + col-span-4 metrics).│
│ Mobile:  1-column vertical sequence with horizontal scrollable chips.  │
├────────────────────────────────────────────────────────────────────────┤
│ 4. CODE WALKTHROUGH TRANSFORMATION                                     │
│ Desktop: Side-by-side (Left: Narrative explanation; Right: REPL code).  │
│ Mobile:  Stacked tabs (Tab 1: Narrative; Tab 2: Terminal Output).      │
├────────────────────────────────────────────────────────────────────────┤
│ 5. HERO LAYOUT TRANSFORMATION                                          │
│ Desktop: Split 50/50 headline and live interactive terminal.           │
│ Mobile:  Headline + primary CTA $\rightarrow$ condensed terminal demo. │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Standard Breakpoint System

```css
/* Mobile First Breakpoint Scale */
/* Mobile Base: < 640px (Default CSS rules) */

@media (min-width: 640px) {
  /* Tablet / Small Screen: >= 640px (sm) */
}

@media (min-width: 768px) {
  /* Tablet Landscape: >= 768px (md) */
}

@media (min-width: 1024px) {
  /* Desktop Standard: >= 1024px (lg) */
}

@media (min-width: 1280px) {
  /* Desktop Wide: >= 1280px (xl) */
}

@media (min-width: 1536px) {
  /* Ultrawide Displays: >= 1536px (2xl) */
}
```

---

## 3. Fluid Typography & Clamp Formulas

To eliminate abrupt text jumps between breakpoints, apply mathematical CSS `clamp()` functions for major display titles:

```css
/* Fluid Display Headline: Scales smoothly from 32px (mobile) to 61px (desktop) */
.text-display-fluid {
  font-size: clamp(2.00rem, 1.25rem + 3.75vw, 3.815rem);
  line-height: var(--leading-display);
  letter-spacing: var(--tracking-tight);
}

/* Fluid Body Lead: Scales from 18px (mobile) to 20px (desktop) */
.text-body-fluid {
  font-size: clamp(1.125rem, 1.00rem + 0.625vw, 1.250rem);
  line-height: var(--leading-body);
}
```

---

## 4. Mobile Ergonomics & Thumb Reach Zones

On mobile viewports ($<640\text{px}$), the human thumb naturally reaches the **lower half of the screen**:

- **Touch Target Rule**: All interactive elements (buttons, nav icons, input fields, checkboxes) must measure **at least $44\text{px} \times 44\text{px}$** of touchable surface area (`min-height: 44px; min-width: 44px;`).
- **Critical Action Docking**: Key conversion triggers (*"Create Free Workspace"*, *"Deploy"*) must pin to a fixed bottom drawer on mobile rather than remaining buried 8 scrolls down the page.
- **Form Input Zoom Prevention**: Mobile iOS automatically forces a disruptive browser zoom if text input font sizes are under $16\text{px}$. Always ensure mobile text inputs use `font-size: 16px;` (`1rem`).
