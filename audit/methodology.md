# Sloppi Visual QA & Audit Methodology

The Visual QA & Anti-Slop Audit Engine is the critical evaluation subsystem of Sloppi. It enables a coding agent to inspect, critique, and validate what was actually rendered in the browser rather than assuming an implementation is successful simply because the code compiled without syntax errors.

```
┌────────────────────────────────────────────────────────────────────────┐
│                        THE AUDIT AXIOM                                 │
│                                                                        │
│ "A design decision is not validated until the rendered interface is    │
│  inspected. The agent must recognize when the code is technically      │
│  correct, but the design is wrong."                                    │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 1. The 3 Pillars of Audit Evaluation

Sloppi evaluates every rendered page at the intersection of three realities:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. DESIGN INTENT       ──► What did DESIGN.md and the Design Thesis    │
│                            intend to communicate and achieve?          │
│ 2. USER NEED           ──► What task, decision friction, or cognitive  │
│                            clarity does the user require?              │
│ 3. ACTUAL RENDERED UI  ──► What is the browser viewport physically     │
│                            displaying across typography, layout, & state│
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Four Independent Evaluation Dimensions

Sloppi explicitly separates four distinct qualities that are often conflated:

| Dimension | Core Question Asked | Common Failure Mode |
| :--- | :--- | :--- |
| **1. Fidelity** | *Does the code faithfully execute the tokens, layout, and copy specified in DESIGN.md?* | Implementation silently drifted from token values, introducing unmapped hex colors or altered spacing. |
| **2. Quality** | *Is the resulting interface well-proportioned, optically balanced, and comfortable to scan?* | Code followed tokens literally, but typography wrapping created awkward single-word orphans or unbalanced gaps. |
| **3. Usability** | *Can the user easily navigate, operate controls, read content, and achieve their goal?* | Interface looks clean, but contrast is too low (3:1 on body text), buttons lack focus rings, or mobile touch targets are under 44px. |
| **4. Distinctiveness** | *Does the interface express a specific visual identity rather than looking like an AI default?* | Interface is technically polished but uses generic SaaS card grids, centered heroes, and gradient text blobs. |

> **Principle**: A page can have **high fidelity but low quality** (literal token implementation with awkward spacing), or **high visual quality but low fidelity** (looks beautiful but violates the brand thesis). The audit must identify and resolve both.

---

## 3. The 11-Tier Audit Priority Ordering

When evaluating an interface, the agent must triage issues in strict priority order. An agent must never waste time adjusting subtle drop-shadows or border radiuses while functional or hierarchy failures exist:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. FUNCTIONAL FAILURE       ──► Broken links, non-working forms, errors│
│ 2. ACCESSIBILITY FAILURE    ──► Contrast violations, missing focus rings│
│ 3. HIERARCHY FAILURE        ──► No focal point, equal loudness syndrome│
│ 4. LAYOUT & COMPOSITION     ──► Broken containers, misaligned grids    │
│ 5. RESPONSIVE FAILURE       ──► Horizontal overflow, mobile truncation │
│ 6. TYPOGRAPHY FAILURE       ──► Unbalanced headings, unreadable lines  │
│ 7. SPATIAL CADENCE          ──► Inconsistent padding, disconnected gaps│
│ 8. INTERACTION FAILURE      ──► Missing hover/active states, dead UI   │
│ 9. VISUAL INCONSISTENCY     ──► Unmapped tokens, mixed icon weights    │
│ 10. DISTINCTIVENESS & SLOP  ──► Generic AI card reflex, decorative fluff│
│ 11. DECORATIVE POLISH       ──► Subtle hairline highlights, dividers   │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 4. The Audit Baseline Reference Set

The audit must never critique an interface in subjective isolation. The agent evaluates the rendered output against five concrete baseline artifacts:
1. **`DESIGN.md`**: The project's persistent design system contract.
2. **Content Architecture (`content/`)**: The 7-tier hierarchy and Section Justification log.
3. **Research Synthesis (`research/`)**: The Design Thesis and Reference Constellation.
4. **Project Inspection Log (`implementation/`)**: Stack constraints and maturity tier.
5. **Core User Journey**: The primary operational task and conversion goal.
