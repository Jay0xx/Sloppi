# Sloppi Agent Checklist: Pre-Render Code Integrity

Execute this checklist before launching the browser dev server or capturing visual screenshots.

---

```markdown
## Pre-Render Checklist

- [ ] **1. Semantic HTML Landmarks**: Page contains `<header>`, `<main>`, `<section>`, `<footer>`, and a single `<h1>`.
- [ ] **2. Zero Raw Hex Leaks**: All colors reference semantic CSS custom properties or Tailwind theme variables.
- [ ] **3. Zero Magic Spacing**: All margins, padding, and gaps consume the 4px/8px baseline token scale.
- [ ] **4. Responsive Breakpoint Rules**: Layout rules declared for Mobile (<640px), Tablet (768px), and Desktop (1024px+).
- [ ] **5. Body Line Length Constrained**: Paragraph text containers constrained to `max-width: 65ch`.
- [ ] **6. Focus Visibility Declared**: Universal `:focus-visible { outline: 2px solid var(--color-focus-ring); }` defined.
- [ ] **7. Touch Target Minimums**: All interactive elements measure `min-height: 44px; min-width: 44px;` for mobile.
- [ ] **8. Reduced Motion Fallback**: `@media (prefers-reduced-motion: reduce)` rules present in global CSS.
```
