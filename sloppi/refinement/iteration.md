# Sloppi Iteration Model & State Machine

The Iteration Model enforces disciplined single-objective execution cycles during frontend refinement, ensuring that every code change has a clear cause-and-effect relationship and can be validated without collateral confusion.

---

## 1. The "One Iteration = One Objective" Mandate

A coding agent must never attempt to fix five unrelated design defects across six different components in a single iteration pass.

```
┌────────────────────────────────────────────────────────────────────────┐
│               THE "ONE ITERATION = ONE OBJECTIVE" RULE                 │
│                                                                        │
│ Each refinement iteration must have EXACTLY ONE primary objective:     │
│ • "Iteration 1: Resolve mobile horizontal scroll overflow."            │
│ • "Iteration 2: Re-architect features section into asymmetric bento."  │
│ • "Iteration 3: Establish 61px hero typography contrast & balance."    │
│ • "Iteration 4: Enforce 2px focus-visible rings across all buttons."   │
│                                                                        │
│ Mixing unrelated objectives makes regression diagnosis impossible.     │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. The Iteration State Machine

The agent operates inside a formal state machine that prevents improvisation:

```
                          [ READY ]
                              │
                              ▼
                        [ IMPLEMENT ]
                              │
                              ▼
                         [ RENDER ]
                              │
                              ▼
                          [ AUDIT ]
                              │
                              ▼
                        [ PRIORITIZE ]
                              │
                              ▼
                          [ REFINE ]
                              │
                              ▼
                       [ RENDER AGAIN ]
                              │
                              ▼
                          [ COMPARE ]
                              │
       ┌──────────────────────┴──────────────────────┐
       │ (Quality Met & Zero Regressions)            │ (Defects Remain)
       ▼                                             ▼
  [ ACCEPT ]                                   [ ROUTE STATE ]
                                                     │
                        ┌────────────────────────────┼────────────────────────────┐
                        ▼                            ▼                            ▼
              [ RESEARCH_REQUIRED ]        [ CONTENT_REQUIRED ]        [ DESIGN_SYSTEM_REQ ]
                        │                            │                            │
                        └────────────────────────────┼────────────────────────────┘
                                                     ▼
                                            [ RE-ENTER CYCLE ]
```

---

## 3. Iteration Memory & Anti-Rediscovery Protocol

The agent maintains working memory of past iterations within the task session:
- **Never Re-Discover the Same Defect**: If an issue was already investigated, documented, and triaged as `ACCEPT` (intentional trade-off) in Iteration 1, the agent must not re-flag it in Iteration 3.
- **Persistent Traceability**: Each iteration records its `Objective`, `Finding ID`, `File Diffs`, `Actual Rendered Effect`, and `Regression Status` in the Refinement Log.
