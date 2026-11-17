# Sloppi v2.0 Agent Checklist: Pre-Ship Quality & Originality Gate

Execute this final verification gate before declaring task completion.

---

```markdown
## Pre-Ship Quality & Originality Gate (v2.0)

- [ ] **1. Primary Composition Visual & Timing Proof Passed**: Prototyped in the primary composition and verified via **screenshots** (layout, hierarchy, contrast) and **browser recording or interaction trace** (timing, continuity, anchoring, touch, keyboard, repeated activation, reduced motion—marking `[INFERRED]` if trace unavailable).
- [ ] **2. Dual Integrity & Materiality Test Passed**: Free of both Gen-1 AI slop (purple blur orbs, centered H1 + 2 pills, 3-card icon grids) AND Gen-2 wireframe clichés (sterile flat `1px`-bordered boxes everywhere, default `Inter`, repetitive `11px` mono eyebrows, or unexamined demo effects).
- [ ] **3. Multi-Viewport Ergonomics Verified (`390px`, `768px`, `1280px+`)**: Zero horizontal overflow (`document.body.scrollWidth <= window.innerWidth`), mobile touch targets >= 44x44px, and native-feeling mobile navigation.
- [ ] **4. Before/After Screenshot Regression Verified**: Any refinement iterations compared Before vs. After screenshots to confirm improved composition and zero collateral layout regressions.
- [ ] **5. WCAG AA/AAA Contrast & Keyboard Focus Verified**: Reading text >= 4.5:1 (7:1 primary), visible 2px `:focus-visible` rings on all controls, and `tabular-nums` on all dynamic figures.
- [ ] **6. Zero Console/Build Errors & Truthful Content**: Clean production build/render, zero "Lorem Ipsum" or fake testimonials, and `DESIGN.md` fully synchronized with final code.
```
