# Sloppi Master Design Research Protocol

The Master Design Research Protocol defines the systematic methodology by which a Sloppi-enabled coding agent converts an abstract user prompt and product definition into actionable, original design intelligence.

Sloppi strictly rejects undirected inspiration browsing ("Find some cool websites"). Research exists exclusively to resolve concrete design questions and extract transferable principles.

---

## 1. The Core Research Pipeline

Every design research pass follows this linear progression:

```
PRODUCT UNDERSTANDING
        │
        ▼
DESIGN PROBLEM IDENTIFICATION
        │
        ▼
RESEARCH QUESTION FORMULATION
        │
        ▼
SOURCE ROUTING & SELECTION
        │
        ▼
DIVERSE REFERENCE SELECTION (Reference Constellation)
        │
        ▼
STRUCTURAL REFERENCE ANALYSIS
        │
        ▼
PRINCIPLE EXTRACTION (Rules vs. Surface Details)
        │
        ▼
CROSS-REFERENCE COMPARISON (Conventions vs. Defaults)
        │
        ▼
DESIGN SYNTHESIS & DESIGN THESIS
        │
        ▼
STANDARDIZED RESEARCH OUTPUT
```

---

## 2. Phase A: Understand the Product

Before opening a single gallery, querying a search engine, or inspecting a reference, the agent must define the product's operational parameters across 13 core dimensions:

1. **Product Category**: (e.g., Developer Infrastructure, Consumer Mobile, B2B Fintech, Creative Tool, Healthcare SaaS, Editorial).
   *Warning*: Never assume the category from the technology stack. A Next.js or React app can be an enterprise ledger or an avant-garde magazine.
2. **Target Users & Mental Model**: Who uses this product daily? What software environments do they inhabit (terminal, spreadsheet, social feeds, Figma)?
3. **Primary User Goal**: What is the single most critical task the user arrives to accomplish?
4. **Primary Conversion Action**: What constitutes immediate success (e.g., `Install via npm`, `Deploy Cloud Cluster`, `Upgrade to Pro`, `Book Demo`, `Join Waitlist`)?
5. **Secondary & Tertiary Actions**: Ancillary pathways (e.g., `Read Documentation`, `Inspect API Reference`, `View Changelog`, `Contact Sales`).
6. **Product Maturity**: Is this an experimental prototype, an emerging challenger brand, or an established enterprise system?
7. **Brand Personality**: 3–4 tonal anchors (e.g., `Industrial, Calm, Precise` vs. `Vibrant, Kinetic, Approachable`).
8. **Target Platform**: Desktop browser, mobile web, tablet canvas, or responsive multi-device.
9. **Information Density Requirement**:
   - *Compact / High Density*: Data tables, monitoring dashboards, code terminals.
   - *Comfortable Density*: Standard SaaS workflows, configuration panels.
   - *Spacious / Low Density*: Marketing landing pages, editorial essays, luxury commerce.
10. **Technical Complexity & Operational Stakes**: What are the consequences of user error (low stakes in social apps vs. critical stakes in financial transactions or server deployments)?
11. **Expected Usage Frequency**: Daily workflow tool (needs muscle-memory ergonomics) vs. occasional utility (needs instant obviousness).
12. **Accessibility Requirements**: Standard WCAG AA (4.5:1 contrast, keyboard navigation) vs. strict WCAG AAA (high-contrast clinical or government compliance).
13. **Responsive Adaptation Scope**: Pure desktop canvas vs. full mobile-first ergonomic experience.

---

## 3. Phase B: Identify the Design Questions

Convert the product understanding into 3 to 6 sharp, high-intent **Research Questions**.

An agent must not ask vague questions ("What should the site look like?"). It must interrogate specific visual and architectural problems:
- *Visual Identity Question*: What visual language establishes institutional credibility without feeling archaic?
- *Composition Question*: Should this interface prioritize modular bento-box density or asymmetric editorial whitespace?
- *Hierarchy Question*: How can typography establish clear reading order without wrapping every paragraph in a bordered card?
- *Navigation Question*: How should 24 distinct documentation sections be structured for rapid discovery?
- *Motion Question*: What state transitions will communicate successful data synchronization without adding latency?

*(Consult `sloppi/research/research-questions.md` for the question generation framework).*

---

## 4. Phase C: Route Questions to Sources

Route each formulated question to the most appropriate specialized primary and secondary sources.

- Match category questions to **SaaSPO** and **Recent.design**.
- Match whitespace and composition questions to **Minimal Gallery** and **Deck.Gallery**.
- Match token structure and system rules to **Refero Styles**.
- Match interaction and motion physics to **60fps.design**.
- Match mobile touch ergonomics to **Loadmo.re**.
- Match hero and CTA conversion questions to **Supahero** and **CTA Gallery**.

*(Consult `sloppi/research/source-routing.md` for the source prioritization model and routing matrix).*

---

## 5. Phase D: Select a Reference Constellation

Never select a single website to serve as the overall visual template. Require **Reference Diversity**:
- Select 2 to 5 distinct references, each chosen for a **different functional reason** (e.g., Ref A for hero narrative structure, Ref B for typography scale contrast, Ref C for navigation density, Ref D for motion feedback).
- Ensure references are not stylistic clones of one another.

*(Consult `sloppi/research/reference-selection.md` for the selection criteria and constellation architecture).*

---

## 6. Phase E: Structurally Analyze References

Inspect each reference structurally across 15 standard dimensions.
- Map the exact compositional skeleton, typographic scale ratios, color role assignments, geometric curvature, spatial rhythm, and interaction triggers.
- **Mandatory Requirement**: Explicitly split findings into **Transferable Principles** (underlying rules) and **Non-Transferable Details** (brand-specific artifacts, exact logos, superficial decorations).

*(Consult `sloppi/research/reference-analysis.md` for the analysis template and principle extraction rules).*

---

## 7. Phase F: Cross-Reference Comparison (Convention vs. Default)

Compare findings across all analyzed references:
1. **Identify Common Patterns**: What structural mechanisms do top-tier references share?
2. **Identify Divergences**: Where do they take radically different approaches, and why does their specific audience justify that divergence?
3. **Convention vs. Default Test**:
   - *Convention*: A pattern that exists because it solves a universal usability friction (e.g., sticky header with primary action on long-scroll pages).
   - *Default*: An unthinking cliché used simply because it is common (e.g., purple gradient blobs, 3 identical cards, generic floating badges).
4. **Identify Rejected Patterns**: Explicitly mark common industry defaults that this product will deliberately refuse to adopt.

---

## 8. Phase G: Synthesize & Formulate the Design Thesis

Synthesize the extracted principles, constraints, and opportunities into a cohesive whole:
1. **Map Visual Tensions**: Establish the dynamic balance (e.g., `Industrial + Warm`, `Dense + Legible`, `Minimal + Expressive`).
2. **Draft the Design Thesis**: Author a 1–2 sentence declaration stating:
   - What the product must feel like.
   - Why that feeling serves the user's mental model.
   - What visual principles create that feeling.
   - What generic conventions are deliberately rejected.

*(Consult `sloppi/research/synthesis.md` for the synthesis methodology).*

---

## 9. Phase H: Generate Standardized Research Output

Document the complete research findings in the standardized format specified in `sloppi/research/research-output.md`.

This document becomes the direct evidentiary foundation for the upcoming `DESIGN.md` contract.

---

## 10. Research Depth & Stopping Criteria

Match research depth strictly to task scope:

| Depth Mode | Trigger Conditions | Scope of Research |
| :--- | :--- | :--- |
| **Lightweight** | Minor component tweaks, single CTA adjustments, localized bug fixes on existing systems. | 1 targeted source (e.g., CTA Gallery), 1–2 focused questions, immediate token mapping. |
| **Standard** | New landing pages, new feature dashboards, significant section redesigns. | 2–3 sources, 3–4 questions, constellation of 3 references, structured analysis. |
| **Deep** | Greenfield product builds, complete rebrands, multi-page web applications. | 4–6 sources, 5–8 questions, constellation of 4–5 references, full cross-reference comparison. |

### The Stopping Rule
> **Stop researching the moment uncertainty falls below the threshold where additional research would materially alter the design thesis or token definitions.**

Do not collect references indefinitely. Do not turn a simple component build into a protracted research detour.
