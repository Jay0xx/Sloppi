# Sloppi Design System Methodology

The Design System Methodology establishes how a coding agent transforms upstream design research, extracted principles, and the project's Design Thesis into a concrete, machine-readable, and human-reasoned design system encoded in `DESIGN.md`.

Sloppi strictly forbids jumping directly from visual inspiration to styling code. The design system acts as the explicit, persistent bridge between abstract design reasoning and deterministic UI implementation.

```
RESEARCH & PRINCIPLES ──► DESIGN THESIS ──► VISUAL LANGUAGE ──► SEMANTIC TOKENS ──► COMPONENT RULES ──► DESIGN.md ──► IMPLEMENTATION
```

---

## 1. The 9 Pre-Token Inquiries

Before defining a single color, font size, spacing step, or corner radius, the agent must formulate explicit answers to nine foundational inquiries:

1. **What is the product?** What is its core mechanism, domain, and operational reality?
2. **Who is it for?** What is the user's primary mental model, tools of daily habit, and cognitive load?
3. **What should it feel like?** What emotional calibration and material metaphor govern the interface?
4. **What should it NOT feel like?** What common industry tropes or adjacent category clichés must be actively avoided?
5. **What visual principles emerged from research?** What mathematical and ergonomic rules were extracted during reference analysis?
6. **What conventions were rejected?** What standard defaults (e.g., 3-card rows, purple gradient orbs, badge inflation) were intentionally excluded?
7. **What visual tensions were selected?** What paired contrasting qualities (e.g., `Technical + Warm`, `Dense + Spacious`) give the design its distinctive character?
8. **What characteristics must remain strictly consistent throughout the interface?** (e.g., token scales, border stroke widths, focus ring indicators, font families).
9. **What characteristics should vary by context?** (e.g., section density alternating between compact data and spacious editorial pauses; surface ground tones alternating across chapters).

---

## 2. The 4-Tier Architectural Separation

A critical failure of AI coding agents is treating principles, characteristics, tokens, and component rules as interchangeable. Sloppi enforces strict separation across four distinct tiers:

```
┌─────────────────────────────────────────────────────────────────────────┐
│ TIER 1: PRINCIPLE (The "Why")                                           │
│ Abstract rule governing user experience and communication intent.        │
│ Example: "The interface should feel precise, calm, and audit-grade."    │
├─────────────────────────────────────────────────────────────────────────┤
│ TIER 2: CHARACTERISTIC (The "What")                                     │
│ Observable visual and spatial manifestation of the principle.           │
│ Example: "High typographic contrast, compact data density, crisp 1px    │
│ borders, and zero ambient drop shadows."                                │
├─────────────────────────────────────────────────────────────────────────┤
│ TIER 3: TOKEN (The "Value & Role")                                      │
│ Machine-readable variable with an explicit semantic assignment.         │
│ Example: `--font-heading-xl: 39px; --color-accent: #00d084;`            │
├─────────────────────────────────────────────────────────────────────────┤
│ TIER 4: COMPONENT RULE (The "Application")                              │
│ Concrete behavioral, structural, and interactive state logic.           │
│ Example: "Primary CTA uses --color-accent with 1px border; hover shifts  │
│ brightness by 10%; active scale is 0.98."                               │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Design System vs. Component Library

Sloppi explicitly distinguishes a **Design System** from a **Component Library**:

| Dimension | Design System (Sloppi's Core Concern) | Component Library (Implementation Layer) |
| :--- | :--- | :--- |
| **Focus** | Principles, visual language, semantic roles, tokens, component behavior, accessibility rules, design rationale. | Reusable code implementations (React components, Web Components, HTML/CSS partials). |
| **Output** | `DESIGN.md` (persistent conceptual and token contract). | `Button.tsx`, `Card.jsx`, `styles.css`. |
| **Coupling** | Framework-agnostic, persistent across agent sessions. | Tied to specific frameworks (React, Vue, Svelte, Tailwind, Vanilla CSS). |
| **Role** | Directs *why* and *how* things are styled. | Executes the actual DOM rendering. |

Sloppi produces the **Design System**. Coding agents use that system to construct whatever component library or UI markup the user's project demands.

---

## 4. Design System Validation Checklist

Before an agent begins implementing application UI code, it must validate the drafted design system by answering the following 10 questions. If the answer to any question is "No", the design system is incomplete:

1. [ ] **Visual Language**: Can I describe the project's visual language in observable, concrete terms rather than vague adjectives?
2. [ ] **Typography**: Can I explain the mathematical modular scale, line-height proportions, and font pairing rationale?
3. [ ] **Color Hierarchy**: Can I explain the semantic roles for all colors (canvas, surfaces, text tiers, brand anchor, functional accents)?
4. [ ] **Spacing Rhythm**: Can I explain the base spatial unit ($4\text{px}$ or $8\text{px}$) and how layout padding scales across densities?
5. [ ] **Layout & Alignment**: Can I explain the grid system, container bounds, section rhythm, and asymmetric modulation?
6. [ ] **Geometry & Elevation**: Can I explain the border-radius progression and whether depth relies on borders, shadows, or surface shifts?
7. [ ] **Component Rules**: Can I explain the states, variants, and anatomy of every primitive component required for this task?
8. [ ] **Interaction & Motion**: Can I explain transition durations, easing curves, and spatial continuity rules?
9. [ ] **Responsive Transformation**: Can I explain how complex desktop layouts transform ergonomically on mobile viewports?
10. [ ] **Anti-Default Guardrails**: Can I list the exact industry clichés that this project has deliberately rejected?

---

## 5. Design System Handoff & Task Complexity

The detail of the design system must correspond directly to task scope:

- **Lightweight Tasks** (e.g., adding an alert banner, modifying a single modal): Extract or update only the relevant component rules and tokens inside `DESIGN.md`; do not rewrite the entire system.
- **Standard Tasks** (e.g., building a new landing page or feature dashboard): Generate a full `DESIGN.md` defining typography, color taxonomy, spacing, geometry, hero structure, and core component rules.
- **Deep Tasks** (e.g., greenfield multi-page application, complete rebrand): Generate a comprehensive `DESIGN.md` containing all 22 canonical sections, token mappings, motion physics, responsive tables, and full component behavior specifications.
