# Changelog

All notable changes to the **Sloppi** skill are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [2.0.0] - 2026-11-12

### Added
- **Creative Direction & 3-Direction Divergence (`doctrine/creative-direction.md`)**: Mandates generating 3 structurally and aesthetically orthogonal design directions (`Direction A`, `Direction B`, `Direction C`) differing across layout paradigm, font pairing, surface materiality, and 5-second interactive centerpiece before writing code.
- **Pre-Implementation Design Originality Gate**: Moves originality and anti-slop screening upstream before implementation, rejecting both Generation-1 AI SaaS templates and Generation-2 "anti-slop" wireframe clichés.
- **Mandatory Live Reference Inspection (`references/source-registry.md`, `research/protocol.md`)**: Added **Awwwards (`awwwards.com`)**, **Godly (`godly.website`)**, and **Dribbble (`dribbble.com`)** alongside `Minimal Gallery`, `60fps.design`, `SaaSPO`, and `Loadmo.re`. Enforces logging concrete visual observations (`OBSERVED` vs. `OFFLINE_SYNTHESIS`) rather than name-dropping sites from memory.
- **Visual-First Primary Composition Gate (`implementation/protocol.md`, `audit/visual-audit.md`)**: Requires building, rendering, and inspecting the primary above-the-fold composition in a live browser before scaling to the remaining sections.
- **Real Visual Regression Testing (`refinement/regression.md`)**: Mandates Before vs. After viewport screenshot comparisons (`390px`, `768px`, `1280px+`) to verify that refinements genuinely improve spatial composition and focal hierarchy.
- **30-Signal Dual Anti-Slop Audit (`audit/anti-slop-audit.md`)**: Expanded from 26 to 30 signals to catch Generation-2 overfit clichés (flat `1px`-bordered wireframes, default `Inter` + `JetBrains Mono`, automatic dark-green CLI terminals, automatic white/navy ledgers, `11px` uppercase mono eyebrow addiction, and cookie-cutter `8+4` bento grids) and replaced the naive "Strip the Effects" test with the **Dual Integrity & Materiality Test**.

### Changed
- **Expressive Typography & Multi-Archetype Tokens (`design-system/typography.md`, `implementation/token-implementation.md`)**: Removed the hardcoded `'Inter'` + `'JetBrains Mono'` and `#0c0e12` dark-green single template in favor of 6 curated expressive web font pairings, fluid `clamp()` scales, and 3 distinct multi-archetype token templates.
- **Dependency Policy (`implementation/dependency-policy.md`)**: Un-banned `motion` (`framer-motion`), interactive SVG/Canvas shaders, and headless accessible primitives (`@radix-ui`, `cmdk`, `vaul`) so interfaces achieve tactile spring choreography.
- **Streamlined 10-Section `DESIGN.template.md`**: Condensed the bureaucratic 25-section form into a high-signal 10-section Creative Direction & Design System contract.
- **Repository Cleanup**: Removed accidental duplicate nested `sloppi/sloppi/` directory and fixed all broken relative module links in `routing.md` and `research/protocol.md`.

---

## [0.1.0] - 2026-08-15

### Added
- Initial foundational doctrine, research protocol, 25-section `DESIGN.md` template, and visual audit checklists.
