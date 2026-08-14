# Sloppi Refinement Prioritization & Impact × Cost Framework

The Prioritization Framework governs how an agent orders and schedules audit findings during iterative refinement, ensuring that critical structural, functional, and accessibility blockers are resolved before minor cosmetic polish is attempted.

---

## 1. The Impact × Cost Decision Matrix

Every finding identified during visual audit is plotted on the **Impact × Cost Matrix**:

```
                  HIGH IMPACT
                       ▲
                       │
       [ PLAN & FIX ]  │  [ FIX IMMEDIATELY ]
       High Impact     │  High Impact
       High Cost       │  Low Cost
                       │  (Top Priority)
───────────────────────┼───────────────────────►
                       │                       LOW COST
       [ USUALLY DEFER]│  [ PIGGYBACK FIX ]
       Low Impact      │  Low Impact
       High Cost       │  Low Cost
       (Bottom Priority)│  (Fix if in same file)
                       │
                       ▼
                  LOW IMPACT
```

### Action Rules
1. **High Impact + Low Cost**: Execute immediately in the current iteration pass.
2. **High Impact + High Cost**: Plan architectural refactoring carefully; isolate into a dedicated iteration.
3. **Low Impact + Low Cost**: Batch together or resolve only when modifying that specific file for a high-impact fix.
4. **Low Impact + High Cost**: Defer or accept as a documented trade-off; do not burn iteration cycles.

---

## 2. The 11-Tier Priority Ranking of Design Concerns

When multiple issues compete for developer attention, resolve them in strict priority order:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. FUNCTIONAL INTEGRITY    ──► Non-working controls, runtime crashes   │
│ 2. ACCESSIBILITY (WCAG)    ──► Contrast < 4.5:1, missing focus rings   │
│ 3. HIERARCHY & FOCAL POINT ──► Equal loudness, missing visual anchor   │
│ 4. COMPOSITION & RHYTHM    ──► Monotone cards, broken macro-layout     │
│ 5. RESPONSIVE ERGONOMICS   ──► Horizontal overflow, sub-44px targets   │
│ 6. TYPOGRAPHY & MEASURE    ──► Runaway line lengths (>75ch), orphans   │
│ 7. SPATIAL CADENCE         ──► Inconsistent padding, magic px numbers  │
│ 8. INTERACTION FEEDBACK    ──► Missing hover/active states             │
│ 9. SYSTEMIC CONSISTENCY    ──► Unmapped tokens, mixed icon strokes     │
│ 10. ANTI-SLOP & IDENTITY   ──► Generic AI defaults, buzzwords          │
│ 11. DECORATIVE POLISH      ──► Subtle hairline highlights, dividers    │
└────────────────────────────────────────────────────────────────────────┘
```

> **Warning**: Never spend an iteration adjusting subtle box-shadows or micro-animations while an accessibility failure or broken mobile layout exists.
