# Workflow: Visual Fix & Anti-Slop Cleanup (Sloppi v2.0)

This workflow guides an agent through diagnosing and repairing weak visual hierarchy, mobile layout overflow, generic AI slop, or sterile wireframe flatness in an existing interface.

---

## Operational Recipe

```
[ Visual Fix Workflow v2.0 ]
        │
        ├──────► STEP 1: Capture "BEFORE" Viewport Screenshot
        │                • Render via `Playwright` MCP (or browser subagent) and capture baseline at `390px` & `1280px`.
        │
        ├──────► STEP 2: 5-Layer Root-Cause Trace
        │                • Trace symptom through Content → Hierarchy → Composition → Art Direction/Materiality → CSS.
        │                • Check whether the page fell into the Polish Trap (blur blobs) OR the Wireframe Trap
        │                  (flat `1px` boxes with `Inter` and zero depth).
        │
        ├──────► STEP 3: Formulate High-Craft Structural Intervention
        │                • Isolate 1 primary objective per iteration (`refinement/iteration.md`).
        │                • Apply targeted typographic, spatial, material, or interactive improvement
        │                  (applying `web-design-guidelines` / `vercel-react-best-practices` if relevant).
        │
        ├──────► STEP 4: Re-Render & Compare BEFORE vs. AFTER Screenshots
        │                • Capture the "After" screenshot via `Playwright` MCP at identical viewports (plus trace if animated).
        │                • Verify that composition, focal hierarchy, and visual craft genuinely improved.
        │
        └──────► STEP 5: 7-Point Regression Check & Conclude
                         • Verify zero horizontal overflow (`scrollWidth <= innerWidth`), ≥44px touch targets,
                           WCAG AA/AAA contrast, and visible `:focus-visible` outlines.
```
