# Sloppi Design Critique & Refinement Methodology

The Refinement Subsystem transforms Sloppi from a static design protocol into an active, self-correcting visual engineering loop. It governs how a coding agent diagnoses visual flaws, isolates root causes, executes surgical code modifications, and validates results against regression.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   THE REFINEMENT AXIOM                                 │
│                                                                        │
│ "Implementation creates the interface. Refinement improves an already  │
│  functioning interface. When a defect is discovered, never rewrite     │
│  the entire page. Diagnose the root cause, isolate the element,        │
│  execute the smallest meaningful modification, and verify."            │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 1. The Closed-Loop Iterative Lifecycle

Refinement operates as a disciplined closed-loop feedback system:

```
┌────────────────────────────────────────────────────────────────────────┐
│                                                                        │
│   BUILD / IMPLEMENT                                                    │
│          │                                                             │
│          ▼                                                             │
│   RENDER IN VIEWPORT (Browser / Dev Server / DOM)                      │
│          │                                                             │
│          ▼                                                             │
│   INSPECT (Mobile, Tablet, Desktop, Wide)                              │
│          │                                                             │
│          ▼                                                             │
│   CRITIQUE (Symptom vs. Root Cause Diagnosis)                          │
│          │                                                             │
│          ▼                                                             │
│   PRIORITIZE (Impact vs. Cost Matrix · FIX NOW / FIX NEXT)             │
│          │                                                             │
│          ▼                                                             │
│   TARGETED MODIFICATION (Single Objective · Minimal Intervention)      │
│          │                                                             │
│          ▼                                                             │
│   RENDER AGAIN & COMPARATIVE INSPECTION (Before vs. After)             │
│          │                                                             │
│          ▼                                                             │
│   REGRESSION CHECK (Hierarchy, Responsive, Accessibility)              │
│          │                                                             │
│     ┌────┴──────────────────────────┐                                  │
│     │                               │                                  │
│     ▼                               ▼                                  │
│   ACCEPT                       RE-ENTRY ROUTE                          │
│   (Stopping Criteria Met)      ├──► RESEARCH RE-ENTRY                  │
│                                ├──► CONTENT RE-ENTRY                   │
│                                └──► DESIGN SYSTEM RE-ENTRY             │
│                                                                        │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Implementation vs. Refinement

| Attribute | Implementation Phase | Refinement Phase |
| :--- | :--- | :--- |
| **Primary Goal** | Translate `DESIGN.md` into functioning components and pages. | Optimize visual rhythm, typography balance, and ergonomics based on rendered reality. |
| **Scope of Work** | Broad: scaffolding, component structures, data contracts, and token pipelines. | Narrow: isolated CSS classes, padding adjustments, typographic measure, and layout subgrids. |
| **Execution Risk** | Medium: building new files. | High: accidental visual or functional regressions across adjacent elements. |
| **Code Strategy** | Architectural 5-layer dependency build order. | Targeted surgical diffs; zero full-file rewrites. |

---

## 3. The 5 Rules of Refinement Safety

1. **Never Rewrite Stable Code**: Do not regenerate entire component files or page layouts to resolve a localized padding or contrast issue.
2. **Never Add Decorative Complexity as a Fix**: If an interface feels generic or flat, diagnose composition, typography, and hierarchy. Never slap on background gradient meshes, glassmorphism, or floating 3D blobs.
3. **Preserve the Design Thesis**: Every modification must deepen alignment with the project's Design Thesis. Reject changes that look visually flashy but weaken the core product identity.
4. **Isolate Scope**: Refine one component, section, or token mapping at a time to maintain clear cause-and-effect visibility.
5. **Continuous Verification**: Never conclude an iteration without re-rendering and executing a regression check.
