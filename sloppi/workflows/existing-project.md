# Workflow: Extending an Established System

This workflow guides an agent through adding new pages, views, or features to a mature project with an existing design system without causing design fragmentation.

---

## Operational Recipe

```
[ Established System Workflow ]
        │
        ├──────► STEP 1: Inspect Established Infrastructure (Tokens, Primitives, Components)
        ├──────► STEP 2: Consult DESIGN.md (Verify semantic color roles and spacing scales)
        ├──────► STEP 3: Reuse Existing Primitives (Use project's Button, Input, Modal; DO NOT duplicate)
        ├──────► STEP 4: Build New Domain Feature (Compose existing primitives into domain layout)
        ├──────► STEP 5: Content Architecture (Apply 7-tier hierarchy and outcome-explicit copy)
        ├──────► STEP 6: Render & Visual QA (Verify integration with global header/footer)
        ├──────► STEP 7: Regression Check (Verify zero style bleeding into existing pages)
        └──────► STEP 8: Complete & Verify (Ensure zero unmapped tokens)
```
