# Sloppi v2.0 Real Visual Regression Testing & Before/After Screenshot Comparison

Refinement is unproven until verified visually in the browser. A CSS change that fixes one element can easily flatten visual hierarchy, clip mobile text, or break an adjacent grid.

Sloppi v2.0 mandates **Before vs. After Screenshot Comparison** for visual refinements and redesign passes.

---

## 1. The Dual Verification Regression Protocol

Whenever executing a visual or interactive refinement iteration:

```
1. CAPTURE "BEFORE" PROOF (Screenshots at 390px & 1280px+ + Interaction Trace if animated)
                 │
                 ▼
2. APPLY TARGETED SINGLE-OBJECTIVE INTERVENTION
                 │
                 ▼
3. CAPTURE "AFTER" SCREENSHOTS (Layout/Hierarchy) & RECORDING/TRACE (Timing/Continuity)
                 │
                 ▼
4. INSPECT & COMPARE BEFORE vs. AFTER SIDE-BY-SIDE
                 │
                 ▼
5. VERIFY COMPOSITIONAL IMPROVEMENT + CONTINUITY + ZERO COLLATERAL REGRESSIONS
```

### Mandatory Comparison Questions
When inspecting the `After` artifacts against the `Before` artifacts (using `read_file` on captured screenshots or `browser` subagent recordings/traces), verify:
1. **Did Compositional Hierarchy Improve?** *(Via Screenshots)*: Is the primary focal point clearer, the typographic scale more commanding, and the negative space better balanced—or did the change merely add surface clutter?
2. **Did Timing, Anchoring & Continuity Hold?** *(Via Browser Recording or Interaction Trace)*: Does the trigger respond immediately, do unchanged anchors stay steady, does repeated activation stay safe, and does reduced motion preserve the state change? (Mark `[INFERRED]` if a trace/recording was unavailable.)
3. **Did Art Direction Strengthen?** Does the revision move closer to the chosen Creative Direction in `DESIGN.md` rather than regressing toward a generic card grid, flat wireframe, or gratuitous demo effect?
4. **Did Any Viewport Regress?** Check `390px` mobile and `1280px` desktop for horizontal overflow (`document.body.scrollWidth > window.innerWidth`), orphaned headline words, overlapped fixed bars, or lost contrast.

---

## 2. The 7-Point Regression Verification Checklist

1. [ ] **Primary Focal Weight**: Does each viewport still have one unmistakable visual anchor?
2. [ ] **Zero Horizontal Overflow**: `scrollWidth <= innerWidth` verified at `390px`, `768px`, and `1280px+`.
3. [ ] **WCAG AA/AAA Contrast**: Did any surface or text color tweak drop body contrast below `4.5:1`?
4. [ ] **Touch & Hit Ergonomics**: Are all mobile interactive controls still $\ge 44\times 44\text{px}$?
5. [ ] **Keyboard Focus Continuity**: Are `2px` `:focus-visible` rings still visible on all interactive elements?
6. [ ] **Interactive State Integrity**: Do interactive widgets, tabs, drawers, and live counters still function without console/runtime errors?
7. [ ] **Token Traceability**: Were all changes synced cleanly with `:root` tokens and `DESIGN.md`?
