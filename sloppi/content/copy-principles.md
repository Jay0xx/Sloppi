# Sloppi Copywriting Principles & Truthfulness Standards

Copywriting in Sloppi is a fundamental structural discipline of interface design. Line length, text measure, vocabulary precision, and typographic wrapping directly govern layout stability, readability, and user trust.

A coding agent must never generate filler copy, insert placeholder "Lorem ipsum", or invent fabricated customer testimonials to satisfy a visual container.

---

## 1. The 6 Core Copywriting Principles

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. PLAIN TECHNICAL VERBS OVER VAGUE ADJECTIVES                         │
│ 2. COPY LENGTH GOVERNED BY COMMUNICATION NEEDS (NO FILLER BOX PADDING) │
│ 3. STRICT TEXT MEASURE & BALANCED LINE WRAPPING (45–75 CHARACTERS)     │
│ 4. AUDIENCE-CALIBRATED DOMAIN VOCABULARY                               │
│ 5. SINGLE FALSIFIABLE ASSERTION PER HEADING                            │
│ 6. TRANSPARENT PRICING & HARD USAGE LIMITATIONS                        │
└────────────────────────────────────────────────────────────────────────┘
```

### Principle 1: Plain Technical Verbs Over Vague Adjectives
Lead with the concrete mechanical action executed by the system:
- ❌ *"Experience seamless, intelligent database orchestration."*
- ✅ *"Provision automated read replicas in AWS, GCP, and Azure with one CLI command."*

### Principle 2: Copy Length Governed by Communication, Not Box Padding
- Never write four redundant sentences simply to make a visual card match the height of an adjacent card.
- If an idea is fully communicated in 8 words, write 8 words and allow clean whitespace to frame it.
- **Strict Ban on "Lorem Ipsum"**: Final implementations must use real, domain-accurate text or explicitly marked temporary wireframe tokens (`[Temporary: Real Benchmark Data Pending]`).

### Principle 3: Strict Text Measure & Line Length
- **Display Headlines**: Constrain to 6–12 words. Always apply `text-wrap: balance` to prevent awkward single-word line wraps (orphans).
- **Body Paragraphs**: Constrain line lengths strictly to **45 to 75 characters** (`max-width: 65ch;`). Lines exceeding 80 characters cause severe eye-tracking fatigue; lines under 35 characters fragment reading comprehension.
- **Feature Descriptions**: Keep card descriptions between 12 and 24 words to ensure optical harmony across multi-column grids.

### Principle 4: Audience-Calibrated Domain Vocabulary
- **Software Engineers & DevOps**: Precise systems terms (`p99 latency`, `gRPC streams`, `ACID transactions`, `eBPF probes`, `SIMD vectorization`).
- **Corporate Treasurers & CFOs**: Authentic fiscal terms (`GAAP compliance`, `real-time ledger reconciliation`, `ISO 20022 settlement`, `SAML audit trails`).
- **Creative & Audio Directors**: Tactile visual and sonic terms (`sub-sample phase alignment`, `non-destructive spline vectors`, `10-bit wide color gamut`).
- **Luxury Horology & Craft**: Fiduciary and artisanal terms (`silicon balance hairspring`, `hand-chamfered bridges`, `chronometric certification`).

### Principle 5: Single Falsifiable Assertion per Heading
Every heading must make **one clear, verifiable assertion**. Avoid compound marketing run-ons:
- ❌ *"We empower developers to ship faster while cutting cloud expenses and elevating security posture across global infrastructure."*
- ✅ *"Cut cloud memory expenses by 70% without sacrificing sub-millisecond p99 read latency."*

### Principle 6: Transparent Pricing & Limitation Copy
High-trust interfaces explicitly define both what a tier includes and what its boundaries are:
- *"Developer Tier: Free forever · Up to 50,000 monthly events · 1-day log retention · Community Discord support."*
- *"Production Tier ($89/mo): 10M monthly events · 30-day retention · 99.9% uptime SLA · Dedicated Slack connect."*

---

## 2. Truthfulness & Verification Standards for Social Proof

Sloppi enforces strict ethical rules governing social proof, metrics, and customer endorsements:

```
┌────────────────────────────────────────────────────────────────────────┐
│ THE SLOPPI SOCIAL PROOF CODE OF CONDUCT                                │
│                                                                        │
│ • TESTIMONIALS: Must feature real names, real verified roles, and real  │
│   concrete technical outcomes. Never use AI-generated avatar faces.    │
│ • CUSTOMER LOGOS: Must represent authentic, authorized clients or      │
│   active open-source ecosystem integrations.                           │
│ • STATISTICS: Must state the exact test benchmark, hardware specs,     │
│   and testing methodology. Never use unsubstantiated "10x" claims.     │
│ • CERTIFICATIONS: Must reflect verified SOC2, HIPAA, or ISO audits.    │
└────────────────────────────────────────────────────────────────────────┘
```

### What to Do When Real Social Proof Is Unavailable
When developing a new product, early-stage prototype, or open-source tool:
1. **Replace Testimonial Cards with Annotated Architecture Diagrams**: Illustrate data pipelines, memory indexing, or security boundaries.
2. **Replace Logo Clouds with Live Quickstart Terminals**: Display copyable CLI installation commands that work immediately.
3. **Replace Vague Statistics with Hardware-Specific Benchmarks**: Share reproducible test harnesses with transparent machine configurations.
4. **Replace Marketing Badges with Open-Source Verification**: Display GitHub commit activity, release version tags, and Apache 2.0 / MIT licensing.

---

## 3. The Content-to-Typography Pipeline

Content decisions must directly inform typographic choices in the Design System:

| Content Attribute | Typographic Treatment Required |
| :--- | :--- |
| **Short Display Hook (3–6 words)** | Large display scale ($56\text{px}$–$64\text{px}$), ultra-tight line height ($0.95$), negative tracking (`-0.03em`). |
| **Long Editorial Thesis (15–25 words)** | Subdued headline scale ($28\text{px}$–$34\text{px}$), relaxed line height ($1.25$), normal tracking. |
| **Numerical Financial Telemetry** | Monospace font with tabular lining figures (`font-variant-numeric: tabular-nums`). |
| **Command Line / API Endpoints** | Monospace font with distinct background tint, 1px border, and copy button. |
| **Regulatory Disclosures / Footnotes** | Compact caption scale ($11\text{px}$–$12\text{px}$), muted contrast, relaxed line height ($1.40$). |
