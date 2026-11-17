# Workflow: Existing Codebase Redesign (Sloppi v2.0)

This workflow guides an agent through elevating or redesigning an existing frontend while preserving business logic and verifying visual improvements via **Before vs. After screenshot comparisons**.

---

## Operational Recipe

```
[ Redesign Workflow v2.0 ]
        │
        ├──────► STEP 1: Inspect Codebase & Capture "BEFORE" Screenshots
        │                • Inspect stack, routes, and state (`implementation/project-inspection.md`).
        │                • Render the current app via `Playwright` MCP (or browser subagent) and capture baseline "Before" screenshots (`390px` & `1280px`).
        │
        ├──────► STEP 2: Diagnose Both Gen-1 Slop & Gen-2 Wireframe Flaws
        │                • Screen against the 30 Signals in `audit/anti-slop-audit.md` (purple SaaS clichés
        │                  AND flat `1px`-bordered wireframe monotony) + `web-design-guidelines`.
        │
        ├──────► STEP 3: Route Live References & Diverge (3 Directions)
        │                • Route by design question ([research/source-routing.md] & [references/source-registry.md]),
        │                  open actual examples/clips, and log deep links + observed mechanics.
        │                • Propose 3 directions varying composition, typography, and interaction, and pass the Originality Gate
        │                  (consulting `frontend-design` if additional aesthetic range helps).
        │
        ├──────► STEP 4: Update `DESIGN.md` & Upgrade Fonts/Tokens/Effect Specs
        │                • Check `Context7` for current docs; discover/install compatible primitives via `shadcn` MCP / `Dissolve` MCP into target app.
        │                • Load expressive typography, semantic `:root` tokens, and stack-fit interaction specs.
        │
        ├──────► STEP 5: Refactor & Prototype Primary Composition First
        │                • Rebuild Hero / Primary Flow + any proposed motion inside the real primary composition;
        │                  verify with Before/After screenshots (layout) and recording/trace (timing/continuity) via `Playwright` MCP.
        │
        ├──────► STEP 6: Refactor Remaining Components & Interactions
        │                • Replace static card grids with domain-authentic structures, verified interaction states,
        │                  and `vercel-react-best-practices` (for React/Next.js) preserving business logic.
        │
        └──────► STEP 7: Side-by-Side Before/After Regression Audit & Ship
                         • Capture "After" screenshots via `Playwright` MCP at `390px` and `1280px`; run `web-design-guidelines`.
                         • Verify compositional improvement, WCAG contrast, ≥44px touch targets, and zero regressions.
```
