# Sloppi Stopping Rules & Diminishing Returns

Stopping Rules establish strict, objective criteria for concluding the refinement loop, preventing infinite optimization cycles and layout destabilization.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   THE STOPPING PRINCIPLE                               │
│                                                                        │
│ "Refinement is an asymptotic process. The agent must know when to stop.│
│  Stop when all high-severity structural and accessibility issues are   │
│  resolved and further iterations produce diminishing returns or risk   │
│  destabilizing functioning layouts."                                   │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 1. The 7 Objective Stopping Criteria

The refinement loop concludes when all seven conditions are satisfied:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. [ ] ZERO BLOCKERS REMAINING                                         │
│    No functional crashes, no broken links, no contrast < 3:1.         │
│                                                                        │
│ 2. [ ] ZERO HIGH-SEVERITY FINDINGS REMAINING                           │
│    No Equal Loudness Syndrome, no unconstrained body overflow.         │
│                                                                        │
│ 3. [ ] UNMISTAKABLE VISUAL HIERARCHY                                   │
│    Primary focal point immediately attracts the eye; clear scanway.   │
│                                                                        │
│ 4. [ ] VERIFIED MULTI-VIEWPORT RESPONSIVENESS                          │
│    Mobile (390px), Tablet (768px), and Desktop (1280px) pass audit.    │
│                                                                        │
│ 5. [ ] FULL ACCESSIBILITY COMPLIANCE                                   │
│    Visible 2px :focus-visible rings; WCAG AA contrast (≥4.5:1).       │
│                                                                        │
│ 6. [ ] ZERO UNMAPPED TOKEN LEAKS                                       │
│    Zero arbitrary hex values or unscaled pixel margins in CSS.         │
│                                                                        │
│ 7. [ ] RESOLVED ANTI-SLOP REVIEW SIGNALS                               │
│    All flagged AI defaults replaced with intentional domain models.    │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. The Curve of Diminishing Returns

The agent recognizes the decaying marginal value of successive iterations:

```
VALUE / ROI
  ▲
  │  [ Iteration 1: Major Hierarchy & Layout Leap ] ──► +50% Clarity
  │  [ Iteration 2: Mobile Responsive Refactor ]     ──► +25% Usability
  │  [ Iteration 3: Typography & Token Alignment ]   ──► +12% Polish
  │  [ Iteration 4: Spatial Cadence & Transitions ]  ──► +6% Rhythm
  │  [ Iteration 5: 1px Sub-pixel Micro-tuning ]     ──► +1% (Risk > Reward)
  └──────────────────────────────────────────────────────────► ITERATIONS
```

> **Safety Rule**: When remaining issues are purely subjective (e.g. slight personal preference on grey hue) or sub-pixel adjustments, **STOP**. Additional changes carry high risk of introducing new collateral regressions.

---

## 3. Maximum Iteration Safety Bounds

To guarantee termination, the agent enforces scope-calibrated iteration ceilings:

| Task Scope | Recommended Max Iterations | Typical Stopping Target |
| :--- | :--- | :--- |
| **Small Component / Local Fix** | Max 2–3 iterations | Iteration 1 or 2 |
| **Section Refactoring** | Max 4–5 iterations | Iteration 2 or 3 |
| **Full Page Landing / App Layout** | Max 6–8 iterations | Iteration 3 or 4 |

> **Crucial Rule**: The iteration limit is a **hard safety ceiling**, not a quota to fulfill. If all 7 stopping criteria are satisfied on Iteration 2, the agent stops immediately.
