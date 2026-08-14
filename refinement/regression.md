# Sloppi Regression Verification & Trade-off Governance

Regression Verification ensures that targeted refinements in one component do not inadvertently damage adjacent layouts, responsive ergonomics, accessibility, or visual hierarchy.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   THE REGRESSION PRINCIPLE                             │
│                                                                        │
│ "Every visual refinement carries collateral risk.                      │
│  Increasing heading size improves desktop hierarchy but may break      │
│  mobile wrapping. Removing cards reduces repetition but may destroy    │
│  visual grouping. Never conclude an iteration without a systematic     │
│  regression audit across all viewports."                               │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 1. The 7-Point Regression Verification Checklist

After executing any code modification, the agent scans for collateral regressions:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. HIERARCHY REGRESSION CHECK  ──► Did the change create competing     │
│                                    focal points or weaken the primary? │
│ 2. RESPONSIVE REGRESSION CHECK ──► Did the change cause horizontal     │
│                                    overflow or clipped text on mobile? │
│ 3. ACCESSIBILITY REGRESSION    ──► Did new background tints drop       │
│                                    contrast below WCAG AA (4.5:1)?     │
│ 4. LAYOUT / WRAP REGRESSION    ──► Did expanding a container squeeze   │
│                                    an adjacent sidebar or table?       │
│ 5. STATE / INTERACTION CHECK   ──► Did CSS property changes remove     │
│                                    the visible :focus-visible ring?    │
│ 6. TOKEN CONSISTENCY CHECK     ──► Were new hardcoded pixel values     │
│                                    accidentally introduced?            │
│ 7. CONTENT MEASURE CHECK       ──► Did paragraph line length exceed    │
│                                    the strict 65ch maximum?            │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. The 4-Tier Regression Severity Classification

| Severity Tier | Definition & Impact | Action Required |
| :--- | :--- | :--- |
| **1. BLOCKING REGRESSION** | Core functionality, navigation, form submission, or mobile viewport broken. | **Roll back or fix immediately** in the current iteration pass. |
| **2. MAJOR REGRESSION** | Significant usability degradation, failing contrast ratio, or broken layout grid. | **Prioritize as FIX NOW** in the immediate next step. |
| **3. MINOR REGRESSION** | Slight 2px alignment mismatch or micro-spacing asymmetry. | **Batch into next refinement pass** or adjust if touching same file. |
| **4. ACCEPTABLE TRADEOFF** | Deliberate minor compromise justified by a major structural improvement. | **Document in Refinement Log** and proceed without looping. |

---

## 3. Documenting Acceptable Trade-offs

Sloppi distinguishes unintended defects from intentional engineering trade-offs:

```markdown
### Documented Trade-off Example
- **Component**: `src/sections/BenchmarkSection.tsx`
- **Modification**: Switched from a 4-column responsive grid to a 2-column wide specification table.
- **Benefit**: Dramatically improved technical legibility and allowed side-by-side comparison of p99 latency metrics.
- **Trade-off**: Requires users on 768px tablet screens to scroll vertically an additional 180px.
- **Classification**: ACCEPTABLE TRADEOFF (Justified by core user comprehension).
```
