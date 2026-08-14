# Workflow: UI Component & Primitive Engineering

This workflow guides an agent through building or refining a reusable UI component primitive with complete state coverage, keyboard accessibility, and token discipline.

---

## Operational Recipe

```
[ Component Workflow ]
        │
        ├──────► STEP 1: Determine Taxonomy Tier (Primitive vs. Component vs. Compound)
        ├──────► STEP 2: Consult Token Registry (Map colors, typography, radii, and shadows)
        ├──────► STEP 3: Implement 12 Component States (:hover, :focus-visible, :active, disabled)
        ├──────► STEP 4: Enforce Keyboard & Focus (2px high-contrast focus ring with offset)
        ├──────► STEP 5: Touch Target Verification (Ensure min-height/width >= 44px on mobile)
        ├──────► STEP 6: Reduced Motion Fallback (@media prefers-reduced-motion respected)
        └──────► STEP 7: Export & Document Props (Ensure strict TypeScript typing)
```
