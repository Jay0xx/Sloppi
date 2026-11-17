# Workflow: Greenfield New Project (Sloppi v2.0)

This workflow guides an agent through designing and building a complete new web application or landing page with **bold art direction, 3-direction creative divergence, and visual-first verification**.

---

## Operational Recipe (8-Stage Creative Director Loop)

```
[ Greenfield Workflow v2.0 ]
        │
        ├──────► STAGE 1: Interrogate & Route Live References
        │                 • Identify persona, product moment, & category clichés to subvert.
        │                 • Route by design question ([research/source-routing.md]) across
        │                   [references/source-registry.md] (`typewolf.com`, `unsection.com`,
        │                   `spottedinprod.com`, `hoverstat.es`, `deadsimplesites.com`, `cosmos.so`,
        │                   `eyecannndy.com`, `designeng.tools`, etc.); open deep links & log observations.
        │
        ├──────► STAGE 2: Diverge into 3 Distinct Creative Directions (A vs. B vs. C)
        │                 • Formulate 3 orthogonal concepts varying composition, typography, and
        │                   interaction (quiet hierarchy/spacing vs. justified motion-led moments);
        │                   consult `frontend-design` if extra aesthetic differentiation helps.
        │
        ├──────► STAGE 3: Pass the Originality Gate & Lock `DESIGN.md`
        │                 • Reject generic SaaS templates AND flat `1px` wireframes / default effects.
        │                 • Specify stack-fit implementation, dependency/license check, & effect contract.
        │
        ├──────► STAGE 4: Prototype Primary Composition & Integrate Stack-Fit Components
        │                 • Query `Context7` for current library setup/APIs; discover/install compatible
        │                   components via `shadcn` MCP (web) or `Dissolve` MCP (RN/Expo) into target app.
        │                 • Load expressive web fonts (never default to `Inter`), adapt tokens/real state,
        │                   and prototype hero / core flow + proposed motion inside the primary composition.
        │
        ├──────► STAGE 5: Live Browser Visual & Timing Proof Gate (MANDATORY!)
        │                 • Verify via `Playwright` MCP (or browser subagent): SCREENSHOTS for layout &
        │                   hierarchy, plus RECORDING or TRACE for timing/continuity/touch/keyboard/repeat.
        │                 • Fix any flatness or timing lag BEFORE building remaining sections.
        │
        ├──────► STAGE 6: Scale Full Interface & Stack Implementation
        │                 • Build remaining chapters/screens modulating layout structure, ground tone,
        │                   and stack-fit interactions (`implementation/interaction-implementation.md`).
        │                 • Apply `vercel-react-best-practices` when implementing React / Next.js.
        │
        ├──────► STAGE 7: Multi-Viewport QA, Guidelines & Anti-Slop Audit
        │                 • Verify `390px` Mobile, `768px` Tablet, and `1280px+` Desktop via `Playwright` MCP.
        │                 • Run `web-design-guidelines` accessibility/interaction review + 30-signal audit.
        │
        └──────► STAGE 8: Screenshot Regression Verification & Ship
                          • Compare Before/After screenshots on any refinements, verify zero console/build
                            errors, sync `DESIGN.md`, and present to user.
```

### Required Artifacts
- `DESIGN.md` (10-section Creative Direction & Design System contract).
- Production Source Code (Expressive Fonts, Semantic Tokens, Interactive Components).
