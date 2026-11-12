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
        ├──────► STEP 3: Inspect Live References & Diverge (3 Directions)
        │                • Inspect 2–3 fresh visual references (`godly.website`, `awwwards.com`, `minimal.gallery`).
        │                • Propose 3 distinct creative directions (A, B, C) and pass the Originality Gate.
        │
        ├──────► STEP 4: Update `DESIGN.md` & Upgrade Fonts/Tokens
        │                • Load expressive typography and semantic `:root` / Tailwind tokens.
        │
        ├──────► STEP 5: Refactor Primary Viewport First & Verify Live
        │                • Rebuild the Hero / Primary Workspace first; render and compare against the
        │                  "Before" screenshot to confirm dramatic visual improvement.
        │
        ├──────► STEP 6: Refactor Remaining Components & Choreography
        │                • Replace static card grids with domain-authentic interactive instruments and
        │                  spring-physics choreography while preserving existing business logic.
        │
        └──────► STEP 7: Side-by-Side Before/After Regression Audit & Ship
                         • Capture "After" screenshots at `390px` and `1280px`.
                         • Verify compositional improvement, WCAG contrast, ≥44px touch targets, and zero regressions.
```
