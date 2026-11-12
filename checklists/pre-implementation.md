# Sloppi v2.0 Agent Checklist: Pre-Implementation

Execute this gate right before writing frontend code.

---

```markdown
## Pre-Implementation Checklist (v2.0)

- [ ] **1. Streamlined 10-Section `DESIGN.md` Locked**: Winning Creative Direction (A/B/C), reference observations, font stack, semantic tokens, and interactive centerpiece are documented in `DESIGN.md`.
- [ ] **2. Distinctive Web Fonts Loaded**: Actual Google Fonts / web fonts (`next/font/google` or `@import`) configured for `--font-display`, `--font-sans`, and `--font-mono` (never falling back to raw `Inter` / `system-ui`).
- [ ] **3. Semantic Tokens Injected in `:root`**: Colors, fluid `clamp()` typography, surface materiality, and motion curves defined in global CSS.
- [ ] **4. Visual-First Build Order Planned**: Ready to build and render the **Primary Composition (Above-the-Fold Hero / Core Workspace) FIRST** and inspect it in the live browser before scaling remaining sections.
- [ ] **5. Motion & Headless Dependencies Ready**: `motion` (`framer-motion`) and single curated icon library (`lucide-react` or `@phosphor-icons/react`) configured with `prefers-reduced-motion` support.
```
