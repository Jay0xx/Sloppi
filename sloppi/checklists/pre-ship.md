# Sloppi Agent Checklist: Pre-Ship Quality Gate

Execute this final verification checklist before presenting work to the user or declaring task completion.

---

```markdown
## Pre-Ship Quality Gate

- [ ] **1. Functional Integrity Verified**: All buttons, links, forms, and interactive tabs operate without runtime errors.
- [ ] **2. Zero Horizontal Body Overflow**: `document.body.scrollWidth === window.innerWidth` across 390px, 768px, 1280px, 1920px.
- [ ] **3. Mobile Touch Ergonomics Verified**: All touch targets >= 44x44px; input font size >= 16px (no iOS auto-zoom).
- [ ] **4. Mathematical WCAG AA/AAA Contrast Passed**: Body text >= 4.5:1; primary text >= 7:1; UI borders >= 3:1.
- [ ] **5. Full Keyboard Navigation Verified**: Tab traversal reaches all controls; visible 2px focus ring; Escape closes modals.
- [ ] **6. Visual Hierarchy Clear**: Single unmistakable primary focal point per viewport; no Equal Loudness Syndrome.
- [ ] **7. Anti-Slop Audit Cleared**: All 26 review signals inspected; zero generic 3-card grid reflexes or gradient text blobs.
- [ ] **8. Distinctiveness & Thesis Verified**: Mistaken Identity Test passed; design reflects authentic domain mechanics.
- [ ] **9. Absolute Truthfulness Verified**: Zero "Lorem Ipsum", zero fake customer quotes, zero unsubstantiated statistics.
- [ ] **10. Zero Silent Design Drift**: All final tokens, typography scales, and component rules synchronized with `DESIGN.md`.
- [ ] **11. All 7 Stopping Criteria Satisfied**: Zero Blockers, zero High-severity defects, diminishing returns recognized.
```
