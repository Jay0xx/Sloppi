# Changelog

All notable changes to the **Sloppi** skill are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [2.1.0] - 2026-11-17

### Added
- **Expanded Reference Source Registry (`references/source-registry.md`, `research/source-routing.md`)**: Added 12 curated sources (`cosmos.so`, `eyecannndy.com`, `hoverstat.es`, `typewolf.com`, `unsection.com`, `spottedinprod.com`, `deadsimplesites.com`, `designeng.tools`, `libraries.dev/waves`, `dissolve.rselmi.com`, `oxyn.space`, `wobli.space`) with question-driven routing and live browser-verified mechanics/licensing notes.
- **Deep-Link, Motion 4-Tuple & `[INFERRED]` Research Logging (`research/protocol.md`, `research/reference-analysis.md`, `research/research-output.md`)**: Requires opening actual examples/clips, recording deep links, observed composition/behavior, adaptable principle, and product fit, capturing `Trigger`, `What Moves`, `What Stays Anchored`, and `How It Settles`, tagging inferred details `[INFERRED]`, and recording inaccessible-demo fallbacks.
- **Behavior-First Motion & Effect Contract (`implementation/interaction-implementation.md`, `implementation/dependency-policy.md`, `audit/interaction-audit.md`)**: Added stack-fit escalation, dependency cost and license checks, anti-auto-dependency guardrails for reference demos, a 7-field Proposed Effect Specification (`Moment`, `Trigger`, `End State & Anchors`, `Touch`, `Keyboard`, `Repeated Activation`, `Reduced Motion`), primary-composition prototyping, and dual verification (screenshots for layout/hierarchy + browser recording or interaction trace for timing/continuity).

### Changed
- **Quiet vs. Motion-Led 3-Direction Synthesis (`research/synthesis.md`, `doctrine/creative-direction.md`, `audit/anti-slop-audit.md`)**: Clarified that directions vary across composition, typography, and interaction—allowing quiet directions to win on hierarchy and spacing while motion-led directions must name the product moment improving feedback, orientation, or continuity.
- **Discoverability & Module Alignment (`SKILL.md`, `routing.md`, `templates/DESIGN.template.md`, `workflows/*`, `checklists/*`)**: Surfaced `research/source-routing.md`, `research/research-output.md`, `design-system/motion.md`, and `audit/interaction-audit.md` directly in `SKILL.md` and synchronized checklists/templates.

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
