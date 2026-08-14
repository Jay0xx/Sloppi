# Sloppi

> **Anti-AI Design Skill for Coding Agents**

Coding agents are very good at producing interfaces.  
They are also very good at producing the *same* interfaces.

**Sloppi** is an agentic design intelligence skill designed for coding environments (Codex, Claude Code, Antigravity, Cursor) that equips agents to research, reason, architect content, synthesize design systems, implement with token discipline, audit rendered outputs, and iteratively refine interfaces so they never default to generic AI-generated frontend patterns.

---

## The Problem

When a developer asks a coding agent to *"build a modern, premium SaaS landing page"*, the model almost invariably produces the exact same aesthetic archetype:
- A centered headline with an animated purple/blue mesh background gradient.
- Vague, unfalsifiable marketing buzzwords (*"Unleash the Power of Next-Gen Velocity"*).
- An obligatory 3-card feature grid with generic outline icons.
- Low-contrast pastel body text with missing keyboard focus outlines.
- Identical, repetitive *"Get Started"* CTAs placed without user intent.
- Decorative surface effects applied to mask weak structural hierarchy.

This happens because standard coding agents jump straight from raw prompt to local CSS tokens, bypassing structural design reasoning, domain content architecture, and rendered visual critique.

---

## What Sloppi Does

Sloppi transforms the coding agent from a passive template regurgitator into a disciplined, evidence-driven visual engineer:

1. **Translates Vague Prompts into Design Reasoning**: Deconstructs requests across 13 product dimensions before generating code.
2. **Routes Research with Intent**: Analyzes specialized reference galleries (e.g. `supahero.io` for heroes, `navbar.gallery` for navigation, `minimal.gallery` for minimal layouts) to extract transferable mathematical principles.
3. **Enforces Content Architecture**: Ensures layout and density emerge from authentic domain mechanics, real data, and falsifiable technical claims.
4. **Establishes `DESIGN.md` Contracts**: Authors a persistent 25-section design system contract before coding to prevent silent multi-session design drift.
5. **Executes Render-Driven Visual QA**: Inspects actual rendered browser viewports across Mobile, Tablet, Desktop, and Wide screens.
6. **Runs Anti-Slop Audits**: Screens rendered interfaces against 26 AI Default Review Signals and executes the *"Strip the Effects"* test.
7. **Drives Closed-Loop Refinement**: Traces defects through a 5-layer root-cause pipeline and executes surgical, single-objective minimal interventions with regression verification.

---

## Core Operational Doctrine

### Anti-Default, Not Anti-Style
Sloppi is **anti-default, not anti-style**. It has no single default visual aesthetic.
- A fintech dashboard should look like a high-density, authoritative telemetry HUD.
- A developer tool should look like a stark, precision monospace CLI/REPL.
- A luxury horology brand should look like a high-contrast editorial serif publication.
- A consumer product should look like an energetic, tactile, chromatic interface.

Sloppi does **not** forbid cards, gradients, border radii, or animations. Instead, **Sloppi demands that every visual decision has a product-specific reason.**

---

## The 14-Stage Closed-Loop Lifecycle

```
Understand ──► Research ──► Synthesize ──► Content Architecture ──► Design System ──► Generate DESIGN.md ──► Inspect Project ──► Implement ──► Render ──► Visual Audit ──► Anti-Slop Audit ──► Critique & Prioritize ──► Targeted Refinement ──► Regression Check ──► Accept / Re-Enter
```

The critical difference in Sloppi is the **feedback loop**: the agent does not assume code compilation equals design success. It renders the interface, audits the result against design principles, diagnoses root causes, and refines until objective stopping criteria are satisfied.

---

## Reference Ecosystem

Sloppi routes design inquiries to specialized reference channels:

| Gallery Channel | Domain Specialization |
| :--- | :--- |
| **`supahero.io`** | Hero section composition, typographic scale, and visual anchors. |
| **`navbar.gallery`** | Navigation architectures, search patterns, and mobile drawers. |
| **`cta.gallery`** | Action hierarchy, outcome-explicit copywriting, and conversion docks. |
| **`deck.gallery`** | Information density, tabular comparisons, and structural cadence. |
| **`minimal.gallery`** | Restrained typography, negative space, and editorial layouts. |
| **`60fps.design`** | Micro-interactions, physics-based springs, and motion timing. |
| **`saaspo.com`** | High-performing SaaS product workflows and onboarding screens. |
| **`loadmo.re`** | Mobile web composition, thumb-zone ergonomics, and responsive reflows. |
| **`styles.refero.design`** | AI-readable design token taxonomies and UI primitive catalogs. |

> **Selection Rule**: Sloppi selects references according to the specific design problem. It extracts mathematical ratios and structural principles; it **never** copies surface templates literally.

---

## Installation

Installing Sloppi makes the design skill immediately discoverable by your coding agent.

### 1. Codex Installation
Clone or copy the repository into your Codex skills directory:

```bash
# Global installation for Codex
git clone https://github.com/Jay0xx/Sloppi.git ~/.codex/skills/sloppi

# Or local workspace installation (project root)
mkdir -p .agents/skills
git clone https://github.com/Jay0xx/Sloppi.git .agents/skills/sloppi
```

### 2. Claude Code Installation
```bash
git clone https://github.com/Jay0xx/Sloppi.git ~/.claude/skills/sloppi
```

### 3. Antigravity / Cursor / Generic AI Agent Installation
```bash
# In your project root
mkdir -p .agents/skills
git clone https://github.com/Jay0xx/Sloppi.git .agents/skills/sloppi
```

### 4. Verification
Codex and other agents automatically discover Sloppi via the YAML frontmatter in [`SKILL.md`](SKILL.md):
```yaml
---
name: sloppi
description: Design intelligence skill for coding agents to prevent generic, repetitive AI frontend defaults...
---
```
When active, the agent recognizes the `sloppi` skill and can invoke its methodology during any design or frontend coding task.

---

## Usage & Examples

### Example 1: Greenfield Project
**Prompt**:
> *"Use the sloppi skill to design and build a landing page for an embedded NVMe key-value database. It should feel authoritative, technical, and precise without looking like generic AI SaaS."*

**Agent Execution**:
1. **Understand & Research**: Identifies systems engineer persona; queries `supahero.io` and `deck.gallery` for developer tools.
2. **Design Thesis**: Formulates *"Tungsten Machined Precision + Phosphor Terminal Telemetry"*.
3. **Content Architecture**: Eliminates buzzwords; crafts falsifiable IOPS throughput benchmarks and CLI commands.
4. **`DESIGN.md`**: Authors 25-section contract with Major Third typography (JetBrains Mono + Inter) and WCAG AAA contrast.
5. **Implementation & Audit**: Builds live CLI sandbox; captures 390px mobile viewport; detects 18px horizontal overflow; executes minimal CSS fix; verifies zero regressions; ships.

### Example 2: Existing Codebase Redesign
**Prompt**:
> *"Our current analytics dashboard looks like a generic Bootstrap template. Use sloppi to audit the page, fix the visual hierarchy, and refactor the feature section without breaking existing React components."*

**Agent Execution**:
1. **Inspection**: Evaluates stack (`implementation/project-inspection.md`) and maps existing Tailwind tokens.
2. **Audit**: Identifies Equal Loudness Syndrome and generic 3-card grid in `audit/anti-slop-audit.md`.
3. **Refinement**: Refactors cards into an asymmetric 8+4 bento grid with an interactive telemetry chart (`refinement/iteration.md`).

---

## Conflict Resolution Hierarchy

When constraints compete, Sloppi resolves decisions in strict priority order:

```
1. EXPLICIT USER REQUIREMENTS (User's intentional directives outrank defaults)
       ↓
2. CORE PRODUCT & FUNCTIONAL REQUIREMENTS (Task completion & business logic)
       ↓
3. ACCESSIBILITY & USABILITY STANDARDS (WCAG AA/AAA, keyboard focus, touch targets)
       ↓
4. EXISTING CODEBASE ARCHITECTURE & CONSTRAINTS (Framework & token maturity)
       ↓
5. PROJECT DESIGN.MD CONTRACT (Persistent design decisions & ratios)
       ↓
6. SYNTHESIZED RESEARCH EVIDENCE (Transferable principles from source registry)
       ↓
7. SLOPPI HEURISTIC GUIDELINES (Anti-default rules & layout best practices)
       ↓
8. AGENT PERSONAL PREFERENCE (Strictly lowest priority; never override requirements)
```

---

## Repository Structure

```
Sloppi/
├── SKILL.md                     # Skill orchestrator and agent entrypoint
├── README.md                    # Main documentation and installation guide
├── LICENSE                      # MIT Open Source License
├── principles.md                # 15 core design principles
├── routing.md                   # Task routing and 4-tier complexity scaling
├── artifacts.md                 # Artifact persistence and classification rules
├── failure-recovery.md          # 7 graceful degradation protocols and honesty rules
├── CONTRIBUTING.md              # Community contribution guide
├── CHANGELOG.md                 # Release history
├── ROADMAP.md                   # Prospective future explorations
├── .gitignore                   # Comprehensive git exclusions
├── .env.example                 # Example environment template
├── .github/                     # Issue templates and PR template
├── doctrine/                    # Foundational design principles and reasoning
├── research/                    # Design Research Protocol & synthesis engine
├── references/                  # Curated map of 15 specialized reference channels
├── content/                     # Content architecture, narrative & CTA intelligence
├── design-system/               # Design synthesis, token taxonomy & component rules
├── templates/                   # Canonical 25-section DESIGN.template.md
├── implementation/              # Framework-agnostic frontend build protocols
├── audit/                       # Visual QA, anti-slop engine & severity triage
├── refinement/                  # Critique, root-cause diagnosis & stopping rules
├── workflows/                   # Fast-path recipes (Greenfield, Redesign, Visual Fix, Component)
├── checklists/                  # Executable gates (Pre-Design, Pre-Code, Pre-Render, Pre-Ship)
└── examples/                    # Full developer infrastructure example artifact suite
```

---

## Design Principles Summary

1. **Design before code**: Formulate reasoning before generating CSS.
2. **Research before imitation**: Extract mathematical principles, not surface skins.
3. **Content informs composition**: Layout emerges from authentic domain data.
4. **Components follow meaning**: Use interactive terminals or diffs over lazy 3-card grids.
5. **Consistency is not monotony**: Enforce tokens while modulating spatial cadence.
6. **Minimalism is not emptiness**: Minimal design demands rigorous typographic contrast.
7. **Novelty is not quality**: Avoid unreadable layouts masquerading as distinctiveness.
8. **Effects require purpose**: Shadows and blurs communicate physical state, not decoration.
9. **Accessibility is baseline engineering**: WCAG AA/AAA contrast and 2px focus rings are mandatory.
10. **Rendered output outranks assumptions**: The design is unproven until inspected in the browser.
11. **Fix root causes, not symptoms**: Trace weaknesses through Content $\to$ Hierarchy $\to$ Tokens.
12. **Stop on diminishing returns**: Conclude refinement when blockers are resolved.
13. **Sloppi has no default aesthetic**: Adapts to any domain, audience, and brand.

---

## Contributing

We welcome contributions that improve design reasoning, expand reference channels, or refine audit rules. Please review [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a pull request.

---

## License

Sloppi is open-source software licensed under the [MIT License](LICENSE).
