# Sloppi Content & Composition Methodology

In Sloppi, **visual design, information architecture, narrative progression, and content are an indivisible, co-dependent system**.

A webpage can possess mathematically balanced typography, curated color tokens, and flawless layout grids, yet still look and feel like generic AI slop if:
- The copy is vague, inflated, and interchangeable.
- The information hierarchy is predictable and flat.
- Every page follows the same mechanical section sequence.
- Every hero uses a giant centered headline with two pill buttons and a floating dashboard.
- Every product gets the same 3-card feature grid with icons.
- Content is written after the layout instead of informing it.
- Sections exist merely because *"websites usually have them"*.
- CTAs are repeated thoughtlessly without understanding user intent.
- Headings say nothing falsifiable or specific.
- Fake metrics and fabricated testimonials are used to fill empty boxes.
- The interface is visually polished but narratively empty.

```
┌────────────────────────────────────────────────────────────────────────┐
│                        THE SLOPPI WORKFLOW                             │
│                                                                        │
│   Understand Product & Technical Reality                               │
│                    │                                                   │
│                    ▼                                                   │
│   Understand User Intent & Cognitive Friction                          │
│                    │                                                   │
│                    ▼                                                   │
│   Identify Information Hierarchy & Attention Budget                    │
│                    │                                                   │
│                    ▼                                                   │
│   Determine Cognitive Narrative Arc & Section Justification            │
│                    │                                                   │
│                    ▼                                                   │
│   Determine Required Content & Truthful Proof Assets                   │
│                    │                                                   │
│                    ▼                                                   │
│   Compose Page & Modulate Section Rhythm                               │
│                    │                                                   │
│                    ▼                                                   │
│   Design Visual Hierarchy & Map to Design System Tokens                │
│                    │                                                   │
│                    ▼                                                   │
│   Implement Semantic Markup & Token Discipline                         │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 1. Core Principle: Content Informs Composition, Composition Reinforces Content

Sloppi explicitly rejects the prevailing AI development anti-pattern:

```
[❌ The Lazy AI Workflow]
Choose Generic Template ──► Insert Filler Copy ──► Swap Brand Color ──► Ship Generic Slop
```

Instead, Sloppi enforces:
- **Content dictates layout container**: An architectural diff between two database models is composed as a side-by-side comparison matrix, never jammed into three rounded cards.
- **Content dictates typographic scale & leading**: A 4-word bold statement uses large display type ($56\text{px}$–$64\text{px}$) with compressed line-height ($0.95$); an 18-word technical explanation requires editorial headline sizing ($28\text{px}$–$32\text{px}$) with relaxed leading ($1.25$).
- **Content dictates spatial cadence**: Dense data tables require tight $8\text{px}$–$12\text{px}$ padding; an authoritative brand thesis demands $96\text{px}$–$128\text{px}$ macro-whitespace to establish gravity.
- **Composition reinforces cognitive takeaway**: Visual weight directly mirrors information priority. Primary differentiators dominate the viewport; secondary details sit quietly in lower-contrast containers.

---

## 2. The 7 Pre-Content Inquiries

Before writing a single headline, proposing section blocks, or selecting layout primitives, the agent must answer seven foundational inquiries:

1. **What does the user need to know?**
   What core mechanism, pricing model, system architecture, or operational reality is required to understand the product?
2. **What does the user need to believe?**
   What specific skepticism, risk anxiety, or friction exists in the user's mind (e.g., *"Will this break my database?"*, *"Is migration going to take months?"*, *"Is this actually secure?"*)?
3. **What does the user need to do?**
   What is the exact, immediate next action (e.g., run a CLI command, test an interactive SQL sandbox, inspect an open-source repository, schedule an architecture review)?
4. **What information reduces uncertainty?**
   What concrete technical specifications, live code samples, architecture diagrams, benchmark methodologies, or SLA terms eliminate hesitation?
5. **What information establishes credibility?**
   What verifiable proof (e.g., reproducible benchmark scripts, SOC2 Type II reports, open-source code, live telemetry) proves claims without relying on hollow marketing fluff?
6. **What information differentiates the product?**
   What single structural or philosophical choice sets this product apart from traditional incumbents?
7. **What information is unnecessary?**
   What generic marketing filler, bloated feature lists, decorative icons, or redundant sentences must be aggressively excised?

> **Rule**: Not every page must answer every question in the same depth. The answers depend strictly on the product archetype, user intent, and stage of the journey.

---

## 3. The 4 Content Density Modes

Content volume and granularity must be calibrated to user expertise, task frequency, and decision stakes:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. SPARSE / MINIMALIST                                                 │
│ Characteristics: Expansive negative space, massive display type,       │
│                  single-focus assertions, minimal visual clutter.      │
│ Optimal For: Luxury consumer goods, creative studios, high-concept     │
│              brand launches, single-action waitlists.                  │
├────────────────────────────────────────────────────────────────────────┤
│ 2. MODERATE / BALANCED                                                 │
│ Characteristics: Clear section cadence, structured typography,         │
│                  balanced copy-to-visual ratios, guided scannability.  │
│ Optimal For: Standard B2B SaaS overviews, consumer fintech, onboarding.│
├────────────────────────────────────────────────────────────────────────┤
│ 3. DENSE / HIGH-GRANULARITY                                            │
│ Characteristics: Monospaced telemetry, compact padding, detailed code   │
│                  walkthroughs, multi-parameter spec tables.            │
│ Optimal For: Developer infrastructure, API hubs, technical comparison  │
│              matrices, complex self-hosted software.                   │
├────────────────────────────────────────────────────────────────────────┤
│ 4. INFORMATION-HEAVY / HUD                                             │
│ Characteristics: Sub-8px grid spacing, tabular numeric figures, live   │
│                  telemetry streams, multi-pane docking panels.         │
│ Optimal For: Financial trading terminals, database telemetry monitors, │
│              cloud infrastructure observability, clinical consoles.   │
└────────────────────────────────────────────────────────────────────────┘
```

### Density Calibration Factors
- **User Task Frequency**: Daily power-users demand dense, instantaneous data density; first-time evaluators need moderate density with guided orientation.
- **Decision Complexity**: A $10/month developer utility needs rapid terminal proof; a $100,000 enterprise infrastructure migration requires comprehensive architecture diagrams, security specifications, and SLA documentation.
- **Cognitive Load Guardrail**: Never assume *"minimal = better"* or *"dense = better"*. Density must match the user's operational requirement.

---

## 4. The 9-Stage Composition Engine

A webpage is not an assembly of isolated components; it is a **coherent visual and cognitive composition**. Sloppi models page layout through nine spatial and structural layers:

```
Canvas ──► Container ──► Focal Point ──► Hierarchy ──► Supporting Elements ──► Whitespace ──► Rhythm ──► Transition ──► Closure
```

1. **Canvas**: The underlying ground plane (`--color-canvas`, texture, grid alignment).
2. **Container**: Max-width boundaries and spatial constraints (`1280px` standard vs. `1440px` wide vs. `768px` editorial measure).
3. **Focal Point**: The single dominant visual anchor in the viewport (e.g., interactive terminal, product canvas, display title).
4. **Hierarchy**: Clear optical distinction between Tier 1 assertions and Tier 6 secondary assurances.
5. **Supporting Elements**: Explanatory captions, telemetry chips, and architectural annotations framing the focal point.
6. **Whitespace**: Intentional negative space acting as cognitive punctuation and visual gravity.
7. **Rhythm**: Deliberate modulation of section heights, density, and ground contrast to eliminate reader fatigue.
8. **Transition**: Seamless visual and narrative connectors between sequential chapters (borders, hairline dividers, background shifts).
9. **Closure**: High-conviction final action container delivering decisive resolution.

---

## 5. Content + Design System Handoff

Content architecture directly feeds the Visual Design System and the resulting `DESIGN.md` contract:

```
Product Understanding & Research
              │
              ▼
        Design Thesis
              │
              ▼
    Content Architecture
(Hierarchy, Messaging, Page Architecture, CTAs)
              │
              ▼
     Visual Design System
(Typography Scale, Semantic Color, Spatial Baselines, Geometry)
              │
              ▼
          DESIGN.md
(Persistent Design Contract)
              │
              ▼
       Implementation
```

By ensuring content precedes and guides token definition, Sloppi guarantees that typography scales, spatial densities, and component primitives serve the communication goals of the product.
