# Sloppi Page Architecture & Section Justification

Page Architecture defines the structural sequence of chapters on a page.

A coding agent must never default to the mechanical AI SaaS template:

$$\text{Hero} \longrightarrow \text{Logo Cloud} \longrightarrow \text{3-Card Feature Grid} \longrightarrow \text{Fake Testimonials} \longrightarrow \text{Pricing Cards} \longrightarrow \text{Generic CTA} \longrightarrow \text{Footer}$$

This unthinking sequence ignores the product's unique narrative, user skepticism, technical complexity, and conversion mechanics. In Sloppi, page architecture is constructed dynamically based on user intent and information requirements.

---

## 1. The 6-Part Section Justification Framework

Every major section proposed on a page must pass the **Section Justification Test**:

```markdown
### Section Justification: [Section Name]
1. **PURPOSE**: What exact communicative or conversion job does this section perform?
2. **USER NEED**: What specific user question, skepticism, or task requirement does it resolve?
3. **CONTENT**: What concrete, domain-specific information or data does it present?
4. **EXPECTED ACTION**: What is the user expected to do, think, or feel upon reading it?
5. **RELATIONSHIP TO PREVIOUS SECTION**: How does this logically flow from the preceding idea?
6. **RELATIONSHIP TO NEXT SECTION**: How does this set up the argument for the following idea?
```

> **Mandatory Rule**: If a section exists only because *"websites usually have them"* or *"it fills empty vertical space"*, it must be deleted immediately.

---

## 2. Common Sections Subject to Justification

| Section Type | When Justified (✅ Retain & Style) | When Unjustified / Slop (❌ Eliminate) |
| :--- | :--- | :--- |
| **Testimonials** | Real quotes from verifiable engineers detailing concrete problems and technical results. | Fabricated quotes with stock avatars (*"Sarah J."*) and vague buzzwords (*"This tool changed my life!"*). |
| **Customer Logos** | Verifiable enterprise customers, ecosystem partners, or active open-source integrations. | Fake tech logos (Google, Netflix, Stripe) placed on an unlaunched project. |
| **Statistics** | Concrete benchmark data with transparent test parameters ($p99 < 12\text{ms}$ under $50\text{k}$ req/sec). | Unsubstantiated claims (*"10x Faster"*, *"99.9% Developer Productivity"*). |
| **Feature Grid** | Grouping 4–6 heterogeneous capabilities of equal architectural importance. | Splitting a single simple product into 3 arbitrary cards to fill layout space. |
| **Pricing Table** | Self-serve checkout with clear tier limits, feature matrix, and monthly/annual toggle. | Enterprise-only high-touch contracts where all tiers say *"Contact Sales"*. |
| **FAQ Accordion** | Resolving complex technical edge cases, security compliance, and migration friction. | Fluff questions created solely to pad the page (*"Why is this tool so amazing?"*). |
| **Newsletter** | Engineering research blogs, open-source changelogs, or specialized technical publications. | SaaS tools where product signup is the primary goal (distracts user attention). |
| **Comparison Matrix** | Transparent, falsifiable parameter-by-parameter analysis against known alternatives. | Biased checkmark grids where the product gets all green checks and rivals get all red crosses. |
| **Product Screenshot**| High-fidelity software UI showing authentic data states and real workflows. | Generic placeholder wireframes with squiggly lines or tilted decorative angles. |
| **Integrations Cloud**| Active, functional SDKs, plugins, and webhooks with version numbers. | 20 company logos with no functional API integration. |
| **Team / About** | High-trust consulting, security audits, or private fiduciary management. | Anonymous stock photos on a developer CLI tool. |

---

## 3. Hero Section Intelligence: 10 Structural Paradigms

A hero section must not automatically be: *giant heading + paragraph + two buttons + floating dashboard + gradient background*.

Sloppi selects from 10 distinct hero architectures based on the product's primary cognitive requirement:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. DEMONSTRATION-FIRST ──► Immediate live interactive widget, sandbox, │
│                            or REPL operating directly above the fold.  │
│ 2. PRODUCT-FIRST       ──► High-fidelity software UI occupying 70%+ of │
│                            the initial viewport.                       │
│ 3. SPLIT COMPOSITION   ──► Left: Value hook + CTA; Right: Live         │
│                            interactive terminal or working canvas.     │
│ 4. TEXT-FIRST / EDITORIAL ─► Authoritative display typography and bold  │
│                            thesis statement with zero UI clutter.      │
│ 5. INTERACTION-FIRST   ──► Direct search bar, URL input, or diagnostic │
│                            tool ready for instant query execution.     │
│ 6. DENSE INFORMATION / HUD ─► Live telemetry streams, server status,    │
│                            and real-time system metrics.               │
│ 7. MINIMAL STATEMENT   ──► Stark single-line punchline, primary action,│
│                            and expansive negative space.               │
│ 8. VISUAL IDENTITY-FIRST ──► Expressive brand motif, tactile geometric │
│                            materials, or sculpted wordmark leading.    │
│ 9. ASYMMETRIC BENTO    ──► Primary hero assertion paired with modular  │
│                            micro-proof tiles and benchmark chips.      │
│ 10. IMMERSIVE CANVAS   ──► Fullscreen interactive 3D visualizer, sound │
│                            canvas, or spatial modeling workspace.      │
└────────────────────────────────────────────────────────────────────────┘
```

### Hero Architecture Selection by Product Archetype

| Product Archetype | Recommended Hero Architecture | Why This Structure |
| :--- | :--- | :--- |
| **Developer API / CLI** | **Split Composition** (Headline + Terminal CLI) | Developers want to see the exact `npm i` or `curl` command before reading marketing text. |
| **Private Wealth Advisory** | **Text-First / Editorial** | Conveys fiduciary gravity and intellectual depth through typography rather than SaaS widgets. |
| **Generative Video Studio** | **Demonstration-First** | Output quality must be seen in motion within 2 seconds to prove fidelity. |
| **Cloud Observability Engine**| **Dense Information / HUD** | Proves the tool's live monitoring capabilities by streaming real system telemetry in the hero. |
| **Domain Security Scanner** | **Interaction-First** | Allows prospective users to input a domain and get immediate value without signing up. |
| **Bespoke Horology / Luxury** | **Visual Identity-First** | Prioritizes craftsmanship, material texture, and mechanical precision over SaaS conversion metrics. |

---

## 4. Dynamic Feature Presentation Models (8 Models)

Instead of automatically building 3 identical rectangular cards with icons, Sloppi selects from 8 functional presentation patterns:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. SEQUENTIAL WORKFLOW TIMELINE                                        │
│ Connected step-by-step narrative (Step 1 → Step 2 → Step 3) with       │
│ active state progress indicators and code snippets.                    │
├────────────────────────────────────────────────────────────────────────┤
│ 2. INTERACTIVE TABBED SANDBOX / REPL                                   │
│ Users toggle between language tabs (TypeScript, Go, Python) or query   │
│ modes to test real inputs and inspect outputs live in the browser.     │
├────────────────────────────────────────────────────────────────────────┤
│ 3. ANNOTATED INTERFACE BLUEPRINT                                       │
│ Full-bleed software screenshot surrounded by interactive callout pins  │
│ that reveal technical architecture explanations on hover/click.        │
├────────────────────────────────────────────────────────────────────────┤
│ 4. SIDE-BY-SIDE ARCHITECTURAL DIFF                                     │
│ Direct contrast showing "Legacy / Manual Bottleneck" vs. "Our Product  │
│ Automated Solution" with highlighted syntax diffs.                     │
├────────────────────────────────────────────────────────────────────────┤
│ 5. ASYMMETRIC BENTO MATRIX                                             │
│ 1 dominant hero card for the primary differentiator + 3 smaller        │
│ micro-proof tiles for secondary capabilities.                          │
├────────────────────────────────────────────────────────────────────────┤
│ 6. TECHNICAL DATA COMPARISON TABLE                                     │
│ Multi-row specification grid with exact throughput numbers, latency    │
│ bounds, memory limits, and hardware compatibility checks.              │
├────────────────────────────────────────────────────────────────────────┤
│ 7. CODE SYNTAX WALKTHROUGH                                             │
│ Syntax-highlighted code editor paired with line-by-line explanatory    │
│ annotations and execution outputs.                                     │
├────────────────────────────────────────────────────────────────────────┤
│ 8. EDITORIAL DEEP-DIVE CHAPTERS                                        │
│ Long-form narrative blocks with pull-quotes, system flow diagrams,     │
│ and in-depth engineering rationale for technical decision-makers.      │
└────────────────────────────────────────────────────────────────────────┘
```
