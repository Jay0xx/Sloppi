# Sloppi Artifact Lifecycle & Persistence Governance

This document defines the complete catalog of artifacts produced across the Sloppi lifecycle, classifying their required vs. optional status and establishing strict persistence boundaries to prevent repository pollution.

---

## 1. The Artifact Classification Matrix

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. PERSISTENT CODEBASE ARTIFACTS (Stored in Project Root)              │
│    • `DESIGN.md`: The canonical 25-section design system contract.     │
│      Status: MANDATORY for non-micro projects. Stored permanently.     │
├────────────────────────────────────────────────────────────────────────┤
│ 2. OPTIONAL PROJECT ARTIFACTS (Stored in `docs/design/` if requested)  │
│    • `research-synthesis.md`: Transferable principles & thesis.        │
│    • `content-architecture.md`: Section justification & attention map. │
│      Status: PERSISTENT ONLY IF PROJECT DOCUMENTATION IS REQUESTED.    │
├────────────────────────────────────────────────────────────────────────┤
│ 3. SESSION / EPHEMERAL ARTIFACTS (Stored in IDE Brain / Scratch)       │
│    • `implementation_plan.md`: Step-by-step build order.               │
│    • `audit-output.md`: 9-field audit finding log.                     │
│    • `refinement-log.md`: Multi-pass iteration diffs & regressions.    │
│      Status: EPHEMERAL. Stored in agent brain; deleted upon ship.      │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Artifact Production & Handoff Table

| Lifecycle Stage | Generated Artifact | Scope & Audience | Persistence Rule |
| :--- | :--- | :--- | :--- |
| **Stage 4: Synthesis** | `research-synthesis.md` | Internal agent reasoning & design thesis formulation. | Ephemeral (Stored in brain artifact folder). |
| **Stage 5: Content** | `content-architecture.md`| Section justification log and copy contracts. | Ephemeral (Merged into `DESIGN.md`). |
| **Stage 7: Design System**| `DESIGN.md` | Persistent contract between human, agents, and codebase. | **PERSISTENT** (Committed in project root or `.agents/`). |
| **Stage 8: Inspection** | `project-inspection.md` | Stack classification & token mapping strategy. | Ephemeral (Session memory). |
| **Stage 11: Audit** | `audit-output.md` | Category status dashboard & 9-field findings. | Ephemeral (Consumed by refinement loop). |
| **Stage 13: Refinement**| `refinement-log.md` | Iteration diffs, comparative checks, regressions. | Ephemeral (Session memory). |

---

## 3. Anti-Pollution Governance

- **Never Commit Scratch Critiques**: Do not leave temporary audit findings or intermediate CSS diff notes checked into user git repositories.
- **Single Source of Truth**: All permanent architectural, typographic, spatial, and color decisions reside exclusively in **`DESIGN.md`**.
