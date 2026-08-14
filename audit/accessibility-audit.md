# Sloppi Accessibility & Usability Audit

The Accessibility Audit inspects whether an interface is universally operable, perceivable, and robust across diverse motor abilities, screen readers, keyboard navigation, and cognitive contexts.

---

## 1. The 7-Point Accessibility Audit Checklist

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. SEMANTIC LANDMARKS & HEADINGS──► Single <h1>; sequential H2 → H3;   │
│                                    <header>, <main>, <nav>, <footer>.  │
│ 2. KEYBOARD OPERABILITY        ──► Full Tab traversal; Enter/Space on  │
│                                    buttons; Escape closes modals.      │
│ 3. MATHEMATICAL WCAG CONTRAST  ──► >= 4.5:1 on body; >= 7:1 on primary;│
│                                    >= 3:1 on UI component boundaries.  │
│ 4. FORM LABELS & ERROR STATES  ──► Explicit <label> htmlFor;           │
│                                    aria-invalid & aria-describedby.    │
│ 5. MOBILE TOUCH MINIMUMS       ──► Strictly >= 44px x 44px hit areas.  │
│ 6. SCREEN READER READABILITY   ──► Clean alt text; aria-label on icons;│
│                                    aria-hidden="true" on decor SVGs.   │
│ 7. REDUCED MOTION SUPPORT      ──► prefers-reduced-motion respected.   │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Accessibility Deficiency Catalog & Fixes

| Accessibility Flaw | Diagnostic Symptom | Severity | Sloppi Remediation |
| :--- | :--- | :--- | :--- |
| **Inaccessible Form Controls** | Input has no `<label>` or only a temporary placeholder that disappears on typing. | **BLOCKER** | Associate an explicit `<label htmlFor="id">` and persistent helper text. |
| **Keyboard Trap / Broken Modals**| Opening a modal does not trap focus or allow closing via the `Escape` key. | **BLOCKER** | Implement accessible modal primitive (e.g. Radix Dialog) with focus lock and Escape listener. |
| **Skipped Heading Levels** | DOM jumps directly from `<h1>` to `<h4>` without intermediate `<h2>` or `<h3>`. | **HIGH** | Re-sequence heading tags to follow strict document outline semantics. |
| **Unlabeled Icon-Only Buttons** | A search button `<button><svg/></button>` has no text, reading as *"button"* to screen readers. | **HIGH** | Add `aria-label="Search documentation"` or visually hidden `<span className="sr-only">`. |
| **Missing Alt Text on Diagrams**| System architecture SVG image lacks an `alt` description explaining the data pipeline. | **MEDIUM** | Provide descriptive `alt` attribute summarizing the architectural data flow. |
