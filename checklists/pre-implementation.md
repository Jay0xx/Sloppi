# Sloppi v2.0 Agent Checklist: Pre-Implementation

Execute this gate right before writing frontend code.

---

```markdown
## Pre-Implementation Checklist (v2.0)

- [ ] **1. Streamlined 10-Section `DESIGN.md` Locked**: Winning Creative Direction (A/B/C), reference observations, font stack, semantic tokens, and interactive centerpiece are documented in `DESIGN.md`.
- [ ] **2. Distinctive Web Fonts Loaded**: Actual Google Fonts / web fonts (`next/font/google` or `@import`) configured for `--font-display`, `--font-sans`, and `--font-mono` (never falling back to raw `Inter` / `system-ui`).
- [ ] **3. Semantic Tokens Injected in `:root`**: Colors, fluid `clamp()` typography, surface materiality, and motion curves defined in global CSS.
- [ ] **4. Primary-Composition Prototyping Planned**: Ready to build and prototype the **Primary Composition** (plus any proposed effect) FIRST inside real layout constraints, verifying layout/hierarchy with **screenshots** (`Playwright` MCP / browser) and timing/continuity with a **browser recording or interaction trace**.
- [ ] **5. Stack-Fit Integration, Cost & License Checked**: Verified package setup via `Context7` / `shadcn` MCP / `Dissolve` MCP when installing external primitives into the target app; checked peer/NativeWind/WebGL2/Metal prerequisites and license; single curated icon family and `prefers-reduced-motion` configured.
```
