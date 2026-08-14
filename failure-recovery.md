# Sloppi Failure Recovery & Honesty Mandate

The Failure Recovery Protocol defines how a Sloppi agent degrades gracefully when external tooling, reference sources, or browser rendering environments are constrained or unavailable, ensuring absolute honesty in audit reporting.

---

## 1. The Honesty Mandate: Zero Fabricated Evidence

A Sloppi agent must strictly distinguish the epistemic status of its observations:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   THE 4 EPISTEMIC EVIDENCE TIERS                       │
│                                                                        │
│ 1. OBSERVED    ──► Directly verified via browser screenshot, rendered  │
│                    viewport inspection, or executed DOM tests.         │
│ 2. INFERRED    ──► Deduced by analyzing static CSS classes, media      │
│                    queries, and component JSX structures.              │
│ 3. ASSUMED     ──► Standard web convention applied where runtime       │
│                    evidence is unavailable (explicitly marked).        │
│ 4. UNAVAILABLE ──► Tooling was unable to execute (explicitly reported).│
└────────────────────────────────────────────────────────────────────────┘
```

> **Strict Rule**: The agent must NEVER claim *"I inspected the rendered mobile screenshot"* if no browser rendering occurred in the environment. It must state: *"Browser rendering unavailable; evaluated static media query definitions and DOM tree."*

---

## 2. The 7 Graceful Degradation Protocols

| Failure Condition | Impact | Sloppi Graceful Recovery Protocol |
| :--- | :--- | :--- |
| **1. Browser Screenshot Tooling Unavailable** | Cannot visually capture rendered pixel state. | Start local dev server; inspect DOM tree via curl/fetch; analyze computed CSS cascade, line measure, and media queries. |
| **2. Reference Galleries Unreachable (Offline/Blocked)** | Cannot fetch online reference galleries. | Rely on core internal design reasoning, mathematical typography scales, 4px/8px spatial rhythm, and architectural archetypes. |
| **3. Project Has Zero Design Tokens / Documentation** | Greenfield or legacy spaghetti code. | Classify as Tier 1 Maturity; inject canonical 3-tier CSS Custom Properties in `:root` inside the global stylesheet. |
| **4. User Design Reference is Ambiguous / Blurry** | Cannot discern exact pixel dimensions. | Extract high-level density mode, visual tension, and alignment axis; ask targeted clarifying question with 2 concrete options. |
| **5. Product Specs or Domain Copy Missing** | Blank state with no copywriting provided. | Draft realistic, falsifiable technical specifications based on domain archetype; **never use "Lorem Ipsum" or fake testimonials**. |
| **6. Real Photography / Media Unavailable** | No authentic product photos exist. | Execute **Intentional Asset Absence**: lead with interactive monospace CLI terminals, annotated SVG architecture schematics, and tabular data. |
| **7. NPM Dependency Installation Fails / Conflicts** | Peer dependency collision. | Reject external package; implement lean native CSS/JS alternative (e.g. CSS Scroll Snap instead of Swiper, CSS transitions instead of Framer). |
