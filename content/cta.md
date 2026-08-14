# Sloppi Call-to-Action (CTA) Intelligence & Hierarchy

Call-to-Action (CTA) Intelligence governs how interactive decision points are framed, worded, and visually weighted across an interface. Grounded in empirical patterns from **CTA Gallery**, CTAs are treated as the culmination of cognitive conviction, not decorative button spam.

A coding agent must never repeat generic labels (*"Get Started"*, *"Learn More"*, *"Click Here"*) across every section without understanding the user's immediate intent and stage in the decision journey.

---

## 1. The 5 Vectors of CTA Intelligence

Before placing, styling, or copywriting any button or link, the agent must evaluate five behavioral vectors:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. USER INTENT         ──► What specific task did the user arrive      │
│                            to perform?                                 │
│ 2. DECISION CONFIDENCE ──► Has the page provided enough proof to justify│
│                            the requested action?                       │
│ 3. STAGE OF JOURNEY    ──► Is the user exploring architecture or ready │
│                            for immediate deployment?                   │
│ 4. ACTION CONSEQUENCE  ──► What exact technical event happens          │
│                            immediately upon clicking?                  │
│ 5. FRICTION BARRIER    ──► What hesitation (e.g., credit card, sales   │
│                            call, data migration) must be alleviated?   │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. The 3-Tier Action Hierarchy

Sloppi enforces strict visual and cognitive separation across three action tiers:

```
┌────────────────────────────────────────────────────────────────────────┐
│ PRIMARY ACTION (Tier 1)                                                │
│ Visual: var(--color-brand) solid fill, high contrast, prominent weight.│
│ Role: The single most valuable next step on the page.                  │
│ Rule: Exactly ONE primary button per visible viewport.                 │
├────────────────────────────────────────────────────────────────────────┤
│ SECONDARY ACTION (Tier 2)                                              │
│ Visual: 1px solid var(--color-border) outline, transparent ground.     │
│ Role: Alternative path for users who need deeper technical proof.      │
│ Examples: "Inspect Documentation", "View Live Demo", "Compare Plans".  │
├────────────────────────────────────────────────────────────────────────┤
│ TERTIARY ACTION (Tier 3)                                               │
│ Visual: Plain text with hover underline or arrow link (font-mono).     │
│ Role: Auxiliary links, secondary documentation, changelog references.  │
│ Examples: "See benchmark methodology →", "Inspect GitHub repo →".      │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Outcome-Explicit Action Copywriting

Button labels must state the **concrete, immediate consequence** of interaction rather than vague generic commands:

| ❌ Generic / Lazy CTA | ❌ Why It Fails | ✅ Sloppi Outcome-Explicit Replacement |
| :--- | :--- | :--- |
| *"Get Started"* | Vague; triggers anxiety about hidden sign-up friction. | *"Create Free Workspace"* or *"Deploy PostgreSQL Cluster"* |
| *"Learn More"* | Passive; does not indicate what will be learned. | *"Read Database Migration Guide"* |
| *"Try Now"* | Ambiguous; could mean a sales demo or local install. | *"Test Live SQL Sandbox in Browser"* |
| *"Submit"* | Cold, bureaucratic data-entry command. | *"Send Invitation to Team"* |
| *"Contact Us"* | High friction; signals an aggressive sales pitch. | *"Schedule 15-Min Technical Architecture Review"* |
| *"Download"* | Missing file context, architecture, and version. | *"Download macOS Universal Binary (v2.4.0)"* |
| *"Sign Up"* | Generic utility label. | *"Start 14-Day Full-Feature Trial"* |
| *"Explore"* | Directionless browsing prompt. | *"Browse 40+ Pre-Built Pipeline Templates"* |

---

## 4. Inline Assurance Elements (Friction Reducers)

High-converting CTAs pair the primary action button with adjacent, low-contrast assurance micro-copy:

```
┌────────────────────────────────────────────────────────────────────────┐
│  [ Create Free PostgreSQL Instance (Primary CTA Button) ]              │
│                               │                                        │
│                               ▼                                        │
│  [ 🔒 No credit card required · 14-day full tier · Instant setup in 60s]
└────────────────────────────────────────────────────────────────────────┘
```

### Proven Assurance Formulas by Product Archetype
- **Developer Tools & Infrastructure**: *"Open-source Apache 2.0 · Self-hostable via Docker · Zero telemetry"*
- **B2B SaaS & Fintech**: *"SOC2 Type II certified · End-to-end encrypted · Cancel anytime in 1 click"*
- **Enterprise Platforms**: *"Dedicated VPC deployment · 99.99% uptime SLA · SAML SSO supported"*
- **Luxury Goods & Advisory**: *"Complimentary insured global courier · 5-year manufacture warranty"*

---

## 5. CTA Placement & Frequency Discipline

- **Hero Anchor**: Place the primary action directly adjacent to supporting technical proof.
- **Sticky Navigation Header**: Display a compact secondary conversion trigger once the hero CTA scrolls out of view.
- **Contextual In-Section Triggers**: Provide deep-dive links (e.g. *"Inspect Python SDK docs →"*) only where relevant features are actively discussed.
- **Final Page Closure (The Closing Ask)**: End the narrative with a high-contrast, distraction-free conversion container summarizing the core value proposition.
- **Anti-Spam Guardrail**: Never insert full-width floating modal popups or repetitive signup blocks between every single paragraph.
