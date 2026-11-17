# Sloppi v2.0 Master Design Research & Live Observation Protocol

Design research in Sloppi v2.0 exists to **spark original creative directions and extract concrete visual mechanics**—never to fill out bureaucratic paperwork or name-drop famous startups from memory.

```
1. INTERROGATE PRODUCT & CATEGORY CLICHÉS
                 │
                 ▼
2. INSPECT LIVE REFERENCES (or declare OFFLINE_SYNTHESIS)
                 │
                 ▼
3. LOG CONCRETE VISUAL OBSERVATIONS (Layout, Type, Materiality, Motion)
                 │
                 ▼
4. DIVERGE INTO 3 DISTINCT CREATIVE DIRECTIONS (A vs. B vs. C)
                 │
                 ▼
5. PASS THE PRE-IMPLEMENTATION ORIGINALITY GATE
```

---

## 1. Phase A: Rapid Product & Category Interrogation

Before browsing references or picking tokens, answer 5 sharp questions:
1. **Operational Reality & Persona**: What is the product's core mechanism, who uses it daily, and what environment do they live in?
2. **Primary 5-Second Action**: What interactive proof or live instrument can the user touch in the very first viewport?
3. **Density & Platform Priority**: Does this call for a sparse editorial broadsheet, a balanced interactive workflow, or a viewport-locked (`100dvh`) spatial workbench? Is `390px` mobile or `1440px` desktop the primary ergonomic target?
4. **Category Cliché to Subvert**: What is the lazy AI default for this category (both Gen-1 purple SaaS slop AND Gen-2 flat `1px`-border / dark-green terminal clichés)?
5. **Emotional & Material Metaphor**: If this software were a physical object, publication, or architectural space, what would it feel like?

---

## 2. Phase B: Question-Driven Reference Inspection (Zero Fake Citations)

Route your inquiry by the specific design question using [research/source-routing.md](source-routing.md) and [references/source-registry.md](../references/source-registry.md):
- **Typography, pairings & scale**: Start with `typewolf.com`.
- **Specific section or page element**: Start with `unsection.com`.
- **Gesture behavior & mobile state transitions**: Start with `spottedinprod.com` (alongside `60fps.design` and `loadmo.re`).
- **Experimental web composition & navigation**: Use `hoverstat.es` (alongside `awwwards.com` and `godly.website`).
- **Minimal-motion restraint test**: Use `deadsimplesites.com` (with `minimal.gallery`) to test how much the composition communicates with minimal motion.
- **Mood, imagery, material & color / framing & pacing**: Use `cosmos.so` for mood/material/color and `eyecannndy.com` for visual techniques, framing, pacing, and transitions.
- **Design-engineering discovery & interactive demos**: Use `designeng.tools` and follow entries to their **original source**. For interactive transition/effect demos (`libraries.dev/waves`, `dissolve.rselmi.com`, `oxyn.space`, `wobli.space`), verify in the browser before describing mechanics, inspect the demo separately from implementation docs, and never treat a demo as an automatic dependency or default effect. If a demo is inaccessible, record its exact status and continue with a comparable source.

### The Evidence Logging Rule
Open the **actual example, live site, or video/interaction clip** when available rather than stopping at gallery thumbnails. Never write *"Inspired by Linear and Stripe."* For every reference used, document:
- **Deep Link & Verification Status**: Exact URL of the example/clip inspected (or `OFFLINE_SYNTHESIS` / `INACCESSIBLE: <status>` with fallback source).
- **Specific Behavior or Composition Observed**: Exact spatial ratios, grid rhythm, typographic pairing/scale contrast, or surface materiality observed.
- **Motion Capture (when motion or interaction is analyzed)**:
  - *Trigger*: Event, gesture, or threshold that initiates it.
  - *What Moves*: Layers, properties, or regions that transform.
  - *What Stays Anchored*: Context, values, or layout frames held steady for orientation.
  - *How the Interaction Settles*: End state, settling behavior, reset/reversal, or edge cues.
- **Design Principle Worth Adapting**: The transferable structural/ergonomic rule (vs. discarded brand skin).
- **Where It Serves the Current Product**: Exact page, section, flow, or product moment where the principle applies.
- **Mark Inferred Details**: Any timing, easing curve, gesture threshold, or off-frame detail that could only be inferred rather than directly observed MUST be labeled `[INFERRED]`.

---

## 3. Phase C: Turn Observations into 3 Distinct Creative Directions

Feed your logged observations directly into Sloppi's three-direction workflow ([research/synthesis.md](synthesis.md) and [doctrine/creative-direction.md](../doctrine/creative-direction.md)):
- Each direction (`Direction A`, `Direction B`, `Direction C`) MUST make a **different choice about composition, typography, and interaction** (plus materiality/palette).
- **Quiet Directions Are Valid and First-Class**: A quiet direction can rely on typographic hierarchy, proportion, and spacing (calibrated against `deadsimplesites.com` / `typewolf.com` / `minimal.gallery`) rather than adding decorative motion.
- **Motion-Led Directions Must Justify the Moment**: A motion-led direction MUST name the **specific product moment** where the effect improves **feedback, orientation, or continuity**—never motion for spectacle.
- Evaluate all three against the **Pre-Implementation Originality Gate** and select (or hybridize) the winning direction for `DESIGN.md`.

---

## 4. Calibrating Research Depth to Task Scope

| Task Tier | Research & Divergence Scope | Time Budget |
| :--- | :--- | :--- |
| **Micro / Small Task** (Token fix, single component) | Inspect existing project `DESIGN.md` and tokens; 1 targeted pattern/gesture check if needed (`unsection.com` / `spottedinprod.com`). | Immediate |
| **Medium Task** (Hero redesign, section, state-feedback flow, slop cleanup) | Identify current flaw; route to 1–2 question-matched sources (`typewolf.com`, `unsection.com`, `spottedinprod.com`, `deadsimplesites.com`); formulate 2–3 options and verify Before/After. | Fast & focused |
| **Large Task** (New landing page, web app, full redesign) | Inspect 2–4 live references across question domains; open deep links/clips; generate 3 full divergent directions (A/B/C) varying composition, typography, and interaction; pass Originality Gate; record in `DESIGN.md`. | Comprehensive |
