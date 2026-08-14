# Sloppi Product Messaging & Anti-Slop Copywriting

Product messaging defines how a product's technical mechanism, value proposition, operational reality, and competitive truth are articulated in language.

A coding agent must never generate vague, inflated marketing copy designed merely to fill empty layout containers. Sloppi enforces technical precision, verifiable claims, domain-specific vocabulary, and a disciplined separation between features, benefits, and outcomes.

---

## 1. The 10 Product Messaging Dimensions

Before drafting any customer-facing copy, the agent must articulate the product's reality across ten foundational vectors:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. PRODUCT        ──► What is it in plain, unambiguous technical terms?│
│ 2. AUDIENCE       ──► Who specifically uses it and in what environment?│
│ 3. PROBLEM        ──► What concrete, painful workflow friction exists? │
│ 4. SOLUTION       ──► How does this product eliminate that friction?   │
│ 5. MECHANISM      ──► What underlying architecture enables the solution│
│ 6. DIFFERENTIATOR ──► What structural choice sets it apart from legacy?│
│ 7. BENEFIT        ──► What immediate operational capability is gained? │
│ 8. PROOF          ──► What verifiable benchmark or artifact proves it? │
│ 9. OBJECTION      ──► What skepticism will the reader immediately have?│
│ 10. ACTION        ──► What is the lowest-friction first step?          │
└────────────────────────────────────────────────────────────────────────┘
```

### Detailed Vector Specifications

1. **Product**: What is it in plain, unambiguous technical terms?
   - *Example*: *"A self-hosted, multi-threaded cache engine written in Rust with native NVMe tiering and Redis wire-protocol compatibility."*
2. **Audience**: Who specifically uses it?
   - *Example*: *"Site reliability engineers and backend infrastructure teams operating distributed microservices with >50,000 requests/sec."*
3. **Problem**: What explicit, painful friction exists in their current workflow?
   - *Example*: *"In-memory cache clusters consume massive RAM budgets, suffer lock contention under spike loads, and risk multi-minute cold-start rebuilds during node restarts."*
4. **Solution**: How does this product eliminate that friction?
   - *Example*: *"Combines lock-free in-memory ring buffers with memory-mapped NVMe storage to deliver sub-millisecond reads at 1/5th the hardware cost."*
5. **Mechanism**: What is the underlying architectural reality that enables this solution?
   - *Example*: *"io_uring asynchronous I/O kernel polling paired with custom SIMD-accelerated dictionary compression."*
6. **Differentiator**: What single structural choice sets it apart from incumbents?
   - *Example*: *"Persists hot data to local NVMe drives without serialization penalties, allowing instant warm restarts with zero cache rebuild time."*
7. **Benefit**: What immediate operational capability does the user gain?
   - *Example*: *"Handle 5x traffic spikes on existing hardware while cutting AWS memory instance expenses by 70%."*
8. **Proof**: What verifiable benchmark or architecture artifact validates the claim?
   - *Example*: *"Open-source, reproducible benchmark harness on AWS c6i.16xlarge instances showing p99 latency under 450μs across 100M keys."*
9. **Primary Objection**: What skepticism will the reader immediately have?
   - *Example*: *"Is this a drop-in replacement for Redis client libraries, or will we have to rewrite our application code?"*
10. **Immediate Action**: What is the lowest-friction first step?
    - *Example*: *"Run `docker run -p 6379:6379 sloppicache/engine:latest` to test local throughput in 30 seconds."*

---

## 2. Feature vs. Benefit vs. Outcome

Sloppi agents must explicitly separate technical mechanics (Features) from direct capabilities (Benefits) and business impact (Outcomes):

| Level | Definition | Developer Infrastructure | Corporate Treasury Platform | Luxury Horology |
| :--- | :--- | :--- | :--- | :--- |
| **FEATURE**<br>*(Mechanism)* | What the technology or product physically does. | *"Dual-write shadow database replication with continuous CDC."* | *"Direct ISO 20022 banking API integration across 14 Tier-1 institutions."* | *"Free-sprung balance wheel with silicon hairspring oscillating at 28,800 vph."* |
| **BENEFIT**<br>*(Capability)* | What the user can directly execute. | *"Roll back breaking schema migrations in under 200ms without table locks."* | *"Consolidate multi-currency cash balances and corporate card limits in real time."* | *"Maintains chronometric precision within -2/+2 sec/day under magnetic fields up to 15,000 gauss."* |
| **OUTCOME**<br>*(Impact)* | The ultimate business or personal value. | *"Zero customer-facing downtime during production deployments."* | *"Close monthly global accounting books in 2 hours instead of 5 days."* | *"An heirloom instrument of enduring aesthetic and mechanical longevity."* |

### Copywriting Hierarchy Rule
- **Headline / Hook**: Lead with the **Benefit** or high-conviction **Outcome**.
- **Body / Supporting Explanation**: Ground the claim immediately with the specific **Feature / Mechanism** so technical evaluators understand *how* the claim is true.

---

## 3. The Empty Marketing Language Ban & Review Triggers

Sloppi establishes an explicit catalog of generic marketing clichés. When detected, these phrases act as **Review Triggers** requiring immediate replacement with precise, measurable, domain-grounded copy:

| ❌ Cliché / Review Trigger | ❌ Why It Fails | ✅ Sloppi Intentional Replacement |
| :--- | :--- | :--- |
| *"The future of [X]"* | Grandiose, unprovable, cliché. | *"Zero-config local Kubernetes development clusters that boot in <2 seconds."* |
| *"Revolutionize your workflow"* | Melodramatic marketing buzzword. | *"Query petabyte-scale Parquet data lakes using standard PostgreSQL SQL syntax."* |
| *"Transform your team collaboration"* | Generic corporate filler. | *"Real-time multiplayer canvas with CRDT conflict resolution for synchronous design reviews."* |
| *"Powerful, next-generation platform"* | Meaningless adjective stacking. | *"Distributed event broker processing 500,000 messages/sec with zero packet loss."* |
| *"Built for the modern enterprise"* | Vague enterprise cliché. | *"SOC2 Type II certified with SAML SSO, immutable audit logging, and custom RBAC policies."* |
| *"Seamless user experience"* | Hollow placeholder phrase. | *"Single-click OAuth login with automatic workspace provisioning and GitHub team sync."* |
| *"Unlock your full potential"* | Motivational poster language. | *"Automate manual CSV exports with recurring webhook schedules and webhook retries."* |
| *"All-in-one comprehensive solution"* | Signals bloated, unfocused software. | *"Unified monitoring for CPU telemetry, memory allocation, and slow query traces in one binary."* |
| *"Designed to empower..."* | Passive corporate jargon. | *"Compile TypeScript directly to WebAssembly with zero manual Rust configuration."* |
| *"Supercharge your productivity"* | Overused AI template hype. | *"Reduce cold build times from 4.5 minutes to 18 seconds using distributed remote caching."* |

---

## 4. The Absolute Prohibition Against Fabricated Proof

A coding agent must **NEVER** fabricate social proof or metrics under any circumstances:

```
┌────────────────────────────────────────────────────────────────────────┐
│ THE SLOPPI PROOF INTEGRITY MANDATE                                     │
│                                                                        │
│ 1. NEVER invent fake customer testimonials (e.g. "Sarah J., VP of      │
│    Engineering at TechCorp: 'This tool changed my life!'").            │
│ 2. NEVER invent fake customer logos (e.g. placing Google, Netflix,     │
│    Stripe logos without authentic authorization).                      │
│ 3. NEVER invent fake statistics (e.g. "99.9% faster", "10x ROI"        │
│    without reproducible benchmark context).                            │
│ 4. NEVER invent fake security certifications, awards, or partners.     │
│ 5. NEVER invent fictional product capabilities that do not exist.      │
└────────────────────────────────────────────────────────────────────────┘
```

### Honest Alternatives When Proof Is Early
If authentic customer quotes or enterprise logos do not yet exist, establish credibility honestly:
1. **Show Technical Architecture Diagrams**: Explain data pipelines, memory layouts, or security boundaries visually.
2. **Show Live Interactive Sandboxes / REPLs**: Allow the prospective user to test queries or API payloads directly in the browser.
3. **Show Transparent Benchmark Scripts**: Provide exact hardware specs, command lines, and reproducible open-source scripts.
4. **Show Quickstart Code Snippets**: Display copyable CLI commands (`npm install`, `brew install`, `docker pull`) that work immediately.
5. **Show Open-Source Transparency**: Highlight GitHub repository stars, commit history, and license specifications (Apache 2.0 / MIT).
