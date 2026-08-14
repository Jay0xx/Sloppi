# Sloppi Implementation Handoff & Completion Contract

Implementation Handoff defines the strict entry prerequisites required before coding begins, and the concrete verification deliverables produced upon completion.

---

## 1. Pre-Implementation Entry Prerequisites

A Sloppi agent must not begin generating frontend code until all five prerequisites are verified:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   PRE-IMPLEMENTATION ENTRY CHECKLIST                   │
│                                                                        │
│ 1. [ ] APPROVED DESIGN.MD CONTRACT                                     │
│    All 25 canonical sections defined (Tokens, Hierarchy, Layout, CTA). │
│                                                                        │
│ 2. [ ] VALIDATED CONTENT ARCHITECTURE                                  │
│    All sections justified; real domain copy written; no placeholders.  │
│                                                                        │
│ 3. [ ] RESEARCH SYNTHESIS & DESIGN THESIS                              │
│    Clear material metaphor, density mode, and visual tension chosen.   │
│                                                                        │
│ 4. [ ] PROJECT INSPECTION LOG                                          │
│    Framework, styling system, icon library, and design maturity known. │
│                                                                        │
│ 5. [ ] LAYERED IMPLEMENTATION PLAN                                     │
│    5-layer dependency build sequence established.                      │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Implementation Deliverables Contract

Upon completing implementation, the agent must deliver a production-ready frontend meeting five core standards:

```
┌────────────────────────────────────────────────────────────────────────┐
│                  IMPLEMENTATION DELIVERABLES CONTRACT                  │
│                                                                        │
│ 1. TOKEN FIDELITY & TRACEABILITY                                       │
│    All colors, typography scales, radii, and spacing mapped to tokens. │
│    Zero raw unmapped hex values or magic pixel numbers.                │
│                                                                        │
│ 2. SEMANTIC HTML & LANDMARKS                                           │
│    Single <h1> per page; proper <header>, <main>, <section>, <footer>. │
│    Clean heading hierarchy without skipping levels.                    │
│                                                                        │
│ 3. RESPONSIVE COMPOSITIONAL FIDELITY                                   │
│    Tested across Mobile (<640px), Tablet (768px), and Desktop (1280px).│
│    Zero horizontal body overflow; touch targets >= 44px on mobile.     │
│                                                                        │
│ 4. ACCESSIBILITY & STATE FEEDBACK                                      │
│    Visible 2px focus rings on all interactive elements.                │
│    Active states, disabled states, and hover feedback functional.      │
│    prefers-reduced-motion respected.                                   │
│                                                                        │
│ 5. DOCUMENTED IMPLEMENTATION LOG                                       │
│    All intentional deviations from DESIGN.md recorded and justified.   │
└────────────────────────────────────────────────────────────────────────┘
```
