# Sloppi Canonical DESIGN.md Specification

This document defines the canonical specification and section structure for a project-specific `DESIGN.md`.

A `DESIGN.md` file functions as a persistent, machine-executable and human-reasoned design contract. It must be generated and approved **before** any frontend implementation begins. It records the project's concrete design decisions, content architecture, token models, and implementation guardrails.

---

## Canonical DESIGN.md Section Architecture

A complete `DESIGN.md` contract consists of 25 structured sections organized into two symbiotic tiers:

```
┌────────────────────────────────────────────────────────────────────────┐
│ PART I: FOUNDATION, INTENT & CONTENT ARCHITECTURE                      │
│ 1. Design Thesis                                                       │
│ 2. Product Context & Operational Stakes                                │
│ 3. Design Personality Profile                                          │
│ 4. Content Principles                                                  │
│ 5. Messaging & Value Architecture                                      │
│ 6. Information & Attention Hierarchy                                   │
│ 7. Page Architecture & Section Cadence                                 │
│ 8. CTA Rules & Action Hierarchy                                        │
│ 9. Content Density & Text Measure                                      │
├────────────────────────────────────────────────────────────────────────┤
│ PART II: VISUAL DESIGN SYSTEM & COMPONENT SPECIFICATION                │
│ 10. Visual Principles & Layout Philosophy                              │
│ 11. Typography Architecture & Modular Scale                            │
│ 12. Color Taxonomy & Semantic Roles                                    │
│ 13. Spacing, Baseline & Density System                                 │
│ 14. Layout, Grids & Container Symmetry                                 │
│ 15. Geometry, Radius Progression & Borders                             │
│ 16. Elevation, Shadows & Depth Strategy                                │
│ 17. Imagery, Diagrams & Media Standards                                │
│ 18. Iconography Architecture                                           │
│ 19. Motion, Easing Curves & Micro-Interactions                         │
│ 20. Responsive & Mobile Ergonomics                                     │
│ 21. Accessibility & WCAG Verification                                  │
│ 22. Component Primitive Rules                                          │
│ 23. Anti-Patterns & Deliberately Rejected Defaults                     │
│ 24. Design Decision Rationale Log                                      │
│ 25. Curated Reference Constellation & Code Integration Notes           │
└────────────────────────────────────────────────────────────────────────┘
```

---

## Detailed Section Schema

```markdown
# [Product Name] — Design System Specification (DESIGN.md)

## 1. Design Thesis
- 1–3 sentence core visual point of view, material metaphor, and density model.
- Explains what the product feels like, why, and what industry conventions it deliberately rejects.

## 2. Product Context & Operational Stakes
- Operational Stakes: [Low / Medium / High & Mission-Critical]
- User Persona & Mental Model: [Target audience cognitive habits and operational environment]
- Core Conversion Objective: [Primary user journey and task completion metric]

## 3. Design Personality Profile
- Diagnostic Axes: [e.g., Technical (90%), Restrained (85%), Dense (80%), Geometric (90%)]
- Tonal Anchors: [4 key tonal words with concrete visual manifestations]

## 4. Content Principles
- Truthfulness Standard: Strict prohibition against fabricated logos, fake testimonials, or unsubstantiated metrics.
- Vocabulary Standard: Plain technical verbs and domain nouns over vague marketing adjectives.
- Communication Rule: Copy length governed by communication needs; zero filler box padding.

## 5. Messaging & Value Architecture
- 10 Messaging Dimensions: Product, Audience, Problem, Solution, Mechanism, Differentiator, Benefit, Proof, Objection, Action.
- Feature vs. Benefit vs. Outcome mapping for core product capabilities.
- Banned Marketing Clichés: Explicit list of purged buzzwords and their concrete replacements.

## 6. Information & Attention Hierarchy
- 7-Tier Attention Budget: Tier 1 Display Hook → Tier 2 Supporting Subhead → Tier 3 Evidentiary Proof → Tier 4 Action → Tier 5 Mechanics → Tier 6 Assurance → Tier 7 Metadata.
- Single Focal Point Mandate: Exactly one primary visual focal point per viewport.

## 7. Page Architecture & Section Cadence
- Section Justification Log: Every section justified by Purpose, User Need, Content, Action, and Contextual Flow.
- Hero Architecture Paradigm: [1 of 10 Paradigms, e.g., Demonstration-First, Split CLI Composition, Dense HUD, Text-First Editorial].
- Feature Presentation Models: [e.g., Asymmetric Bento, Interactive Sandbox, Annotated Blueprint, Side-by-Side Diff].
- Section Rhythm Modulation: Dynamic variation of section height, density, ground color, and media texture to eliminate reader fatigue.

## 8. CTA Rules & Action Hierarchy
- Action Tiers: Primary (var(--color-brand) solid fill), Secondary (1px border outline), Tertiary (monospace text link).
- Outcome-Explicit Labels: Concrete action consequence (e.g., "Create Free Workspace", "Deploy Cluster in 2 Mins").
- Inline Assurance Micro-Copy: Friction reducers adjacent to primary triggers ("No credit card required · Instant setup").

## 9. Content Density & Text Measure
- Density Mode: [Sparse / Moderate / Balanced / Dense / Information-Heavy]
- Reading Constraints: Max 65ch measure for body paragraphs; max 12 words with `text-wrap: balance` for display headings.

## 10. Visual Principles & Layout Philosophy
- 4 to 6 structural rules governing the product's execution (e.g., Asymmetric rhythm, Typographic hierarchy before boxes, Purposeful state motion).

## 11. Typography Architecture & Modular Scale
- Font Families: Display, Body/UI, and Monospace families with explicit fallback chains.
- Type Scale: Mathematical ratio (e.g., Minor Third 1.200), exact pixel sizes, line-height proportions, letter-spacing offsets, and semantic roles.
- Leading & Tracking Inversion: Compressed leading on display type; open leading on body text; positive tracking on uppercase labels.

## 12. Color Taxonomy & Semantic Roles
- Canvas Grounds: `--color-canvas`, `--color-canvas-alt`
- Surfaces: `--color-surface`, `--color-surface-hover`, `--color-surface-active`
- Typographic Contrast: `--color-text-primary` (AAA), `--color-text-secondary` (AA), `--color-text-muted` (AA), `--color-text-inverse`
- Brand Signature: `--color-brand`, `--color-brand-hover`, `--color-brand-contrast`
- Functional Accents: `--color-accent-info`, `--color-accent-success`, `--color-accent-warning`, `--color-accent-danger`
- Borders & Dividers: `--color-border`, `--color-border-subtle`, `--color-border-hover`
- Focus Indicator: `--color-focus-ring`

## 13. Spacing, Baseline & Density System
- Baseline Unit: [4px or 8px]
- Scale Tokens: Step values (`2px`, `4px`, `8px`, `12px`, `16px`, `24px`, `32px`, `48px`, `64px`, `96px`, `128px`).
- Layout Padding Standards: Section gap, container max-width, card padding, control gap.

## 14. Layout, Grids & Container Symmetry
- Grid Models: [Asymmetric bento, dense multi-column dock, 2-column editorial, full-bleed canvas]
- Alignment Discipline: Left-aligned narrative anchoring vs. centered standalone modals.

## 15. Geometry, Radius Progression & Borders
- Corner Radii Progression: `--radius-xs` (2px), `--radius-sm` (4px), `--radius-md` (8px), `--radius-lg` (12px), `--radius-xl` (16px), `--radius-full` (9999px).
- Concentric Radius Rule: Inner radius = Outer radius - Padding.
- Border Stroke Standards: 1px subtle hairline vs. 2px brand emphasis.

## 16. Elevation, Shadows & Depth Strategy
- Depth Model: [Pure flat border-driven vs. multi-layer ambient occlusion vs. hard tactile offset]
- Elevation Tokens: Level 0 (flat), Level 1 (resting), Level 2 (hover/dropdown), Level 3 (modal overlay).

## 17. Imagery, Diagrams & Media Standards
- UI Screenshot Rules: Real domain data, syntactically valid code, 16:10 aspect ratio, minimal window chrome.
- Diagram Standards: Clean SVG linework, consistent stroke weights, semantic flow arrows.
- Anti-Slop Filter: Zero arbitrary floating 3D spheres, unverified stock testimonials, or unlabeled graphs.

## 18. Iconography Architecture
- Library Selection: [Single curated library, e.g., Lucide, Phosphor]
- Stroke Weight: [Uniform 1.5px or 2.0px]
- Sizing Scale: XS (12px), SM (16px), MD (20px), LG (24px) paired with typography scale.

## 19. Motion, Easing Curves & Micro-Interactions
- Duration Scale: Instant (100ms), Fast (150ms), Normal (240ms), Slow (350ms).
- Easing Curves: Standard snappy settle (`cubic-bezier(0.16, 1, 0.3, 1)`).
- Reduced Motion: Universal `@media (prefers-reduced-motion: reduce)` fallback protocol.

## 20. Responsive & Mobile Ergonomics
- Breakpoints: Mobile (<640px), Tablet (640–1024px), Desktop (1024–1440px), Ultrawide (>1440px).
- Structural Transformations: Desktop tables → stacked narrative cards; top headers → bottom tab bar/drawers.
- Touch Minimums: Strictly $\ge 44\text{px} \times 44\text{px}$ touch targets within natural thumb reach zones.

## 21. Accessibility & WCAG Verification
- Contrast Verification: Mathematical validation for all text and UI boundaries (WCAG AA/AAA).
- Keyboard Navigation: Visible high-contrast `:focus-visible` rings on all interactive elements.
- Semantic HTML: Single `<h1>` per page, proper landmark hierarchy, descriptive ARIA attributes.

## 22. Component Primitive Rules
- Behavioral, variant, and state rules for Buttons, Inputs, Cards, Navigation, Tabs, Modals, Tables, Badges, and Empty States.

## 23. Anti-Patterns & Deliberately Rejected Defaults
- List of 5–10 specific industry defaults explicitly banned for this project with rationale.

## 24. Design Decision Rationale Log
- 5-part rationale entries (Value, Role, Rationale, Usage, Avoid) for all major color, typography, and layout choices.

## 25. Curated Reference Constellation & Code Integration Notes
- Table of external references analyzed from the Reference Constellation, documenting what principle was extracted from each.
- CSS custom properties naming conventions, token import paths, and framework integration guidelines.
```
