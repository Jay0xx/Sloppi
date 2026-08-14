# Workflow: Visual Fix & Anti-Slop Cleanup

This workflow guides an agent through diagnosing and repairing broken visual hierarchy, mobile layout overflow, or generic AI slop in an existing interface.

---

## Operational Recipe

```
[ Visual Fix Workflow ]
        │
        ├──────► STEP 1: Inspect Rendered Defect (Capture viewport screenshot / DOM state)
        ├──────► STEP 2: Root-Cause Trace (Trace symptom through 5-layer diagnostic model)
        ├──────► STEP 3: Prioritize Fix (Plot on Impact × Cost matrix; isolate 1 objective)
        ├──────► STEP 4: Minimal Intervention (Apply targeted code diff; DO NOT rewrite whole page)
        ├──────► STEP 5: Re-Render & Compare (Verify problem improved in viewport)
        ├──────► STEP 6: Regression Audit (Verify adjacent layouts, touch targets, and contrast)
        └──────► STEP 7: Conclude (Record diff in Refinement Log)
```
