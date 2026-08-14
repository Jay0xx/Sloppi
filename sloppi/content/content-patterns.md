# Sloppi Content Patterns & Component Mapping

Content Patterns are proven architectural structures for organizing specific communicative and functional tasks.

In Sloppi, content patterns are **structural guides, not rigid visual templates**. An agent must choose the pattern that best matches the user's immediate cognitive task and map each content type to its optimal visual representation.

---

## 1. Content-to-Component Mapping Matrix

A primary failure mode of AI coding agents is the **"Universal Card Reflex"**—mapping every single concept to `card + icon + heading + paragraph`. Sloppi enforces functional, content-informed representation:

| Content Type | ❌ Lazy AI Default Reflex | ✅ Sloppi Intentional Component Mapping |
| :--- | :--- | :--- |
| **Comparative Capabilities** | 3 separate identical cards with bullet points | **Structured Comparison Table** with parameter rows and clear check/cross indicators. |
| **Step-by-Step Sequence** | 3 floating cards with numbers 1, 2, 3 | **Connected Narrative Timeline** with active state progress indicators and code snippets. |
| **Dense Numerical Data** | Arbitrary circular pie charts in cards | **Monospaced Data Grid** with tabular figure alignment and sortable headers. |
| **Technical Architecture** | Generic marketing illustration of a server | **Annotated SVG System Flow Diagram** showing real data packet trajectories. |
| **Interactive Code Usage** | Static image of a code editor | **Interactive Tabbed REPL / Terminal** allowing copy-paste and language switching. |
| **Long-Form Analysis** | Multi-card grid with truncated snippets | **Asymmetric Editorial Layout** with sticky chapter navigation and pull-quotes. |
| **Pricing & Limits** | 3 identical cards with no limit context | **Transparent Tier Matrix** with monthly/annual toggle and explicit usage boundaries. |
| **Live Telemetry Streams** | 3 metric cards with static numbers | **Dense Status HUD** with live flashing pulse dots, latency sparks, and terminal logs. |

---

## 2. Catalog of 12 Core Content Patterns

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. TECHNICAL PRODUCT EXPLANATION                                       │
│ 2. FEATURE DEEP-DIVE & ARCHITECTURE MECHANISM                          │
│ 3. COMPETITIVE COMPARISON MATRIX                                       │
│ 4. TRANSPARENT PRICING & USAGE LIMITS                                  │
│ 5. DEVELOPER ONBOARDING & INTERACTIVE QUICKSTART                       │
│ 6. TECHNICAL DOCUMENTATION & API HUB                                   │
│ 7. OPERATIONAL DASHBOARD & TELEMETRY HUD                               │
│ 8. EDITORIAL CASE STUDY & ENGINEERING POST-MORTEM                      │
│ 9. CREATIVE PORTFOLIO & WORK SHOWCASE                                  │
│ 10. LUXURY COMMERCE & EDITORIAL PRODUCT STORY                          │
│ 11. HIGH-TOUCH ENTERPRISE FIDUCIARY ADVISORY                           │
│ 12. SINGLE-PURPOSE HIGH-INTENT CONVERSION FLOW                         │
└────────────────────────────────────────────────────────────────────────┘
```

---

### Pattern 1: Technical Product Explanation
- **When to Use**: Introducing a complex developer tool, API, database engine, or infrastructure component.
- **Problem Solved**: Explaining the underlying system mechanism to an audience that distrusts generic marketing claims.
- **Typical Information Hierarchy**:
  1. High-level architecture thesis statement.
  2. Visual system architecture flow diagram.
  3. Interactive terminal / code quickstart block.
  4. Core mechanism breakdown (memory model, protocol, latency bounds).
- **Potential Alternatives**: Interactive browser sandbox or split CLI composition.
- **Common AI Defaults**: Showing a fake dashboard screenshot with squiggly placeholder lines.
- **Failure Modes**: Over-simplifying technical mechanisms into consumer buzzwords.

---

### Pattern 2: Feature Deep-Dive & Architecture Mechanism
- **When to Use**: Highlighting a single proprietary innovation (e.g. custom lock-free memory ring buffer).
- **Problem Solved**: Providing deep technical substantiation for why the product outperforms incumbents.
- **Typical Information Hierarchy**:
  1. Mechanism title & primary metric assertion ($p99 < 500\mu\text{s}$).
  2. Explanatory schematic diagram.
  3. Code snippet / configuration example.
  4. Verifiable benchmark telemetry graph.
- **Potential Alternatives**: Side-by-side before/after code diff.
- **Common AI Defaults**: 3 cards with lightbulb and gear icons.
- **Failure Modes**: Explaining *what* it is without explaining *how* it works.

---

### Pattern 3: Competitive Comparison Matrix
- **When to Use**: Explicitly addressing migration friction and contrasting against legacy tools (e.g., Redis, Kafka).
- **Problem Solved**: Helping technical buyers evaluate trade-offs with factual rigor.
- **Typical Information Hierarchy**:
  1. Comparison premise (*"Why we built X instead of using Y"*).
  2. Side-by-side specification table (Latency, RAM usage, NVMe persistence, license).
  3. Migration guide (*"Zero-downtime proxy bridge in 3 steps"*).
- **Potential Alternatives**: Annotated architecture diff diagram.
- **Common AI Defaults**: Unsubstantiated checkmark grid where the product gets all green checks and rivals get all red crosses.
- **Failure Modes**: Biased, unprovable claims that destroy technical credibility.

---

### Pattern 4: Transparent Pricing & Usage Limits
- **When to Use**: Self-serve developer tools, SaaS platforms, cloud infrastructure APIs.
- **Problem Solved**: Eliminating unexpected overage anxiety and hidden enterprise contract friction.
- **Typical Information Hierarchy**:
  1. Billing toggle (Monthly vs. Annual with explicit discount percentage).
  2. 2–4 distinct tiers with explicit persona headers (*"Individual Engineers"*, *"Production Teams"*).
  3. Transparent numeric limits (API calls, data retention, seats).
  4. Outcome-explicit CTA (*"Create Free Developer Workspace"*, *"Deploy Production Cluster"*).
  5. Deep feature comparison accordion underneath.
- **Potential Alternatives**: Usage-based slider calculator.
- **Common AI Defaults**: Floating cards with arbitrary badges (*"Most Popular"*) and hidden limit boundaries.
- **Failure Modes**: Hiding overage fees or forcing all business tiers into *"Contact Sales"*.

---

### Pattern 5: Developer Onboarding & Interactive Quickstart
- **When to Use**: First-time developer evaluation, getting-started guides.
- **Problem Solved**: Reducing time-to-first-successful-run to under 60 seconds.
- **Typical Information Hierarchy**:
  1. 1-line installation command with instant copy button.
  2. Tabbed configuration examples (Docker, Helm, Homebrew).
  3. Live terminal output simulator verifying success.
  4. Next-step SDK integration links.
- **Potential Alternatives**: Embedded WebAssembly terminal sandbox.
- **Common AI Defaults**: Multi-step wizard hidden behind a mandatory email signup wall.
- **Failure Modes**: Broken copy-paste commands that fail due to unstated prerequisites.

---

### Pattern 6: Technical Documentation & API Hub
- **When to Use**: SDK references, endpoint parameters, developer guides.
- **Problem Solved**: Enabling engineers to look up and test endpoints in under 3 minutes.
- **Typical Information Hierarchy**:
  1. Sticky left-rail table of contents + `Cmd+K` command palette.
  2. Center column: Sequential quickstart and endpoint breakdown.
  3. Sticky right-rail: Code panel with language tabs (TypeScript, Go, Python) and live JSON response.
- **Potential Alternatives**: Single-column expandable accordions.
- **Common AI Defaults**: Unindexed text blobs with static non-copyable code images.
- **Failure Modes**: Disconnected layout where code examples are 5 scrolls away from parameter tables.

---

### Pattern 7: Operational Dashboard & Telemetry HUD
- **When to Use**: System monitoring, real-time observability, trading terminals.
- **Problem Solved**: Enabling power-users to monitor high-frequency telemetry at a glance.
- **Typical Information Hierarchy**:
  1. Top telemetry ribbon with global system health and p99 metrics.
  2. Multi-pane grid with tabular logs, memory distribution sparks, and active connections.
  3. Anomaly alert drawer with diagnostic timestamps.
- **Potential Alternatives**: Fullscreen single-chart inspector with time-scrubber.
- **Common AI Defaults**: Centered cards with arbitrary colorful circular donut charts.
- **Failure Modes**: Low data density, non-tabular font numbers that jitter on re-render.

---

### Pattern 8: Editorial Case Study & Engineering Post-Mortem
- **When to Use**: Enterprise customer proof, architecture retrospectives.
- **Problem Solved**: Demonstrating how the software resolved massive production bottlenecks.
- **Typical Information Hierarchy**:
  1. Executive summary & verified metric (*"How Acme Corp handled 12M req/sec during Black Friday"*).
  2. The Pre-Existing Architecture & Failure Point.
  3. The Implementation Blueprint (with network diagram).
  4. Verified Telemetry Outcomes & Senior Architect Quote.
- **Potential Alternatives**: Interactive Before/After architecture slider.
- **Common AI Defaults**: 3-sentence testimonial card with stock avatar face.
- **Failure Modes**: Pure marketing praise with zero architectural or operational details.

---

### Pattern 9: Creative Portfolio & Work Showcase
- **When to Use**: Independent studios, design engineers, creative directors.
- **Problem Solved**: Demonstrating aesthetic taste, craft, and interactive excellence.
- **Typical Information Hierarchy**:
  1. Minimal, high-concept thesis statement.
  2. Asymmetric full-bleed project gallery with interactive video previews on hover.
  3. Case study deep-dives with role breakdown and interactive prototypes.
  4. Direct contact anchor.
- **Potential Alternatives**: Chronological archive grid or 3D project carousel.
- **Common AI Defaults**: 3-column card grid with generic mockup frames.
- **Failure Modes**: Slow-loading unoptimized media and cookie-cutter grid templates.

---

### Pattern 10: Luxury Commerce & Editorial Product Story
- **When to Use**: Bespoke mechanical goods, high-end audio hardware, artisanal craft.
- **Problem Solved**: Conveying tactile material quality, heritage, and physical desirability.
- **Typical Information Hierarchy**:
  1. Full-bleed macro imagery of material finishes.
  2. Philosophical manifesto on craftsmanship.
  3. Exploded technical diagram of internal components.
  4. Precise physical specifications table (weight, tolerance, alloy).
  5. Discreet bespoke inquiry action.
- **Potential Alternatives**: Interactive 360-degree exploded mechanism visualizer.
- **Common AI Defaults**: Neon discount banners and aggressive countdown timers.
- **Failure Modes**: Treating high-craft luxury items like generic drop-shipped commodity goods.

---

### Pattern 11: High-Touch Enterprise Fiduciary Advisory
- **When to Use**: Private wealth management, institutional corporate treasury, risk audit.
- **Problem Solved**: Establishing deep fiduciary credibility, security governance, and compliance trust.
- **Typical Information Hierarchy**:
  1. Quiet, authoritative headline conveying capital stewardship.
  2. Institutional capabilities breakdown (custody, liquidity management, audit trails).
  3. Regulatory disclosures and institutional partner verifications.
  4. Direct consultation scheduling with senior partners.
- **Potential Alternatives**: Split editorial layout with partner letters.
- **Common AI Defaults**: Startup SaaS pricing tiers with animated checkmark animations.
- **Failure Modes**: Flashy gradients and startup jargon that signal amateurism to institutional CFOs.

---

### Pattern 12: Single-Purpose High-Intent Conversion Flow
- **When to Use**: Beta waitlists, webinar registrations, specialized CLI installers.
- **Problem Solved**: Maximizing single-action completion by removing all extraneous cognitive distraction.
- **Typical Information Hierarchy**:
  1. Stark, single-focus headline.
  2. 1-sentence value proposition.
  3. Direct inline email/command input + primary CTA.
  4. 3 brief assurance chips underneath.
- **Potential Alternatives**: Modal overlay or terminal quick-entry.
- **Common AI Defaults**: Adding full global navigation headers and massive footer link directories that bleed user attention.
- **Failure Modes**: Forcing multi-page navigation when a single focused screen achieves the objective.
