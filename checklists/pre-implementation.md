# Sloppi v2.0 Agent Checklist: Pre-Implementation

Execute this gate right before writing frontend code.

---

```markdown
## Pre-Implementation Checklist (v2.0)

- [ ] **1. Streamlined 10-Section `DESIGN.md` Locked**: Winning Creative Direction (A/B/C), reference observations, font stack, semantic tokens, and interactive centerpiece are documented in `DESIGN.md`.
- [ ] **2. Distinctive Web Fonts Loaded**: Actual Google Fonts / web fonts (`next/font/google` or `@import`) configured for `--font-display`, `--font-sans`, and `--font-mono` (never falling back to raw `Inter` / `system-ui`).
- [ ] **3. Semantic Tokens Injected in `:root`**: Colors, fluid `clamp()` typography, surface materiality, and motion curves defined in global CSS.
- [ ] **4. Primary-Composition Prototyping Planned**: Ready to build and prototype the **Primary Composition** (plus any proposed effect) FIRST inside real layout constraints, verifying layout/hierarchy with **screenshots** and timing/continuity with a **browser recording or interaction trace**.
- [ ] **5. Stack-Fit Implementation, Cost & License Checked**: Any external primitive recommended fits the existing stack with inspected bundle/peer cost and licensing (never auto-importing demo packages); single curated icon family and `prefers-reduced-motion` support configured.
```
