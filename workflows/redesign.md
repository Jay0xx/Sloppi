# Workflow: Existing Codebase Redesign (Sloppi v2.0)

This workflow guides an agent through elevating or redesigning an existing frontend while preserving business logic and verifying visual improvements via **Before vs. After screenshot comparisons**.

---

## Operational Recipe

```
[ Redesign Workflow v2.0 ]
        │
        ├──────► STEP 1: Inspect Codebase & Capture "BEFORE" Screenshots
        │                • Inspect stack, routes, and state (`implementation/project-inspection.md`).
        │                • Render the current app and capture baseline "Before" screenshots (`390px` & `1280px`).
        │
        ├──────► STEP 2: Diagnose Both Gen-1 Slop & Gen-2 Wireframe Flaws
        │                • Screen against the 30 Signals in `audit/anti-slop-audit.md` (purple SaaS clichés
        │                  AND flat `1px`-bordered wireframe monotony).
        │
        ├──────► STEP 3: Route Live References & Diverge (3 Directions)
        │                • Route by design question ([research/source-routing.md] & [references/source-registry.md]),
        │                  open actual examples/clips, and log deep links + observed mechanics.
        │                • Propose 3 directions varying composition, typography, and interaction, and pass the Originality Gate.
        │
        ├──────► STEP 4: Update `DESIGN.md` & Upgrade Fonts/Tokens/Effect Specs
        │                • Load expressive typography, semantic `:root` tokens, and stack-fit interaction specs.
        │
        ├──────► STEP 5: Refactor & Prototype Primary Composition First
        │                • Rebuild Hero / Primary Flow + any proposed motion inside the real primary composition;
        │                  verify with Before/After screenshots (layout) and recording/trace (timing/continuity).
        │
        ├──────► STEP 6: Refactor Remaining Components & Interactions
        │                • Replace static card grids with domain-authentic structures and verified interaction
        │                  states (touch, keyboard, repeated activation, reduced motion) preserving business logic.
        │
        └──────► STEP 7: Side-by-Side Before/After Regression Audit & Ship
                         • Capture "After" screenshots at `390px` and `1280px`.
                         • Verify compositional improvement, WCAG contrast, ≥44px touch targets, and zero regressions.
```
