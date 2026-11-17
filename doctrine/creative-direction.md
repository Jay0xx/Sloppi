# Sloppi v2.0 Creative Direction, 3-Direction Divergence & Originality Gate

A design system is not an art direction. You can have mathematically valid tokens, `WCAG AAA` contrast, and `1px` borders, and still ship a sterile, forgettable wireframe that looks like every other agent-built page.

This module governs **how a coding agent explores, selects, and executes genuinely original visual ideas** before writing application code.

---

## 1. Mandatory Live Reference Inspection (Zero Fake Citations)

Before proposing any design direction, ground your visual thinking in real reference evidence routed by design question ([research/source-routing.md](../research/source-routing.md) and [references/source-registry.md](../references/source-registry.md)):

1. **Inspect Actual Examples or Clips When Online**:
   - Route by need: `typewolf.com` (typography), `unsection.com` (specific sections), `spottedinprod.com` (iOS gestures/state transitions), `hoverstat.es` (experimental composition/nav), `deadsimplesites.com` (minimal-motion restraint check), `cosmos.so` (mood/material/color), `eyecannndy.com` (framing/pacing/transitions), `designeng.tools` (follow entries to original sources), plus `awwwards.com`, `godly.website`, `minimal.gallery`, `60fps.design`, `dribbble.com`, `saaspo.com`, `loadmo.re`, and verified interactive demos (`libraries.dev/waves`, `dissolve.rselmi.com`, `oxyn.space`, `wobli.space`).
   - **Record Concrete Observations (Never Name-Drop)**: Open the actual example or clip and log:
     - *Deep link & verification status* (mark any unverified timing/internals `[INFERRED]`; if a demo is inaccessible, log its status and switch to a comparable source).
     - *Composition, typography & materiality observed* (spatial ratios, font voice/scale contrast, surface lighting/grain).
     - *Motion mechanics (when relevant)*: **trigger**, **what moves**, **what stays anchored**, and **how the interaction settles**.
     - *Design principle worth adapting & where it serves the current product* (keeping demo mechanics separate from package dependencies).
2. **Epistemic Honesty When Offline**:
   - If network/browser access is unavailable or blocked, explicitly mark `Reference Mode: OFFLINE_SYNTHESIS` in `DESIGN.md`. Never fabricate observations of websites you did not inspect.

---

## 2. The 3-Direction Divergence Mandate

Before writing `DESIGN.md` or generating components for a new frontend or redesign, you **MUST formulate 3 meaningfully different creative directions** (`Direction A`, `Direction B`, `Direction C`).

> **Strict Rule**: Three color palettes applied to the same layout DO NOT count as three directions. Each direction must make a **different choice about composition, typography, and interaction** (alongside surface/materiality). A **quiet direction** can rely on typographic hierarchy and spacing (calibrated against `deadsimplesites.com`); a **motion-led direction** must name the **specific product moment** where the effect improves **feedback, orientation, or continuity**:

| Divergence Axis | Direction A (e.g., Quiet / Hierarchy-Led) | Direction B (e.g., Editorial / Section-Led Subversion) | Direction C (e.g., Motion-Led / Spatial Instrument) |
| :--- | :--- | :--- | :--- |
| **1. Composition Choice** | Sparse asymmetric column or broadsheet relying on spacing & scale | Distinct section cadence tailored per content job | Viewport-locked workbench, experimental nav, or full-bleed canvas |
| **2. Typography Choice** | Distinct font pairing & dramatic scale ratio #1 | Distinct font pairing & scale ratio #2 | Distinct font pairing & scale ratio #3 |
| **3. Interaction Choice** | Minimal motion; instant, crisp state feedback + high-legibility hierarchy | Lightweight anchored micro-feedback at specific user actions | Motion-led centerpiece naming the exact product moment for **feedback, orientation, or continuity** |
| **4. Surface, Materiality & Palette** | Light/dark temperature, texture, depth & border philosophy #1 | Opposite temperature, surface physics & depth model #2 | High-craft tactile/chromatic or archival material model #3 |

### Example: Diverging on a Developer API / Cloud Database Tool

- **Direction A — "Phosphor Flight Recorder" (Industrial Telemetry HUD)**
  - *Why it's risky*: Close to the overused dark-mode dev-tool trope; often fails the Originality Gate unless executed with extraordinary bespoke canvas craft.
- **Direction B — "Bell Labs Technical Monograph" (Swiss Archival Blueprint)**
  - *Canvas*: Warm drafting vellum (`#F4F1EA`) + blueprint cobalt (`#0038A8`) + oxidation vermilion (`#D9381E`).
  - *Typography*: `Instrument Serif` (italicized theorems & section titles) + `Space Grotesk` (structural headers) + `Commit Mono` (inline memory layouts).
  - *Layout*: Two-column academic paper margin-note grid with live interactive SVG B-Tree page-split visualizer embedded directly into the margin.
- **Direction C — "Hardware Synthesizer Rack" (Tactile Physical Instrument)**
  - *Canvas*: Brushed anodized aluminum (`#DCDFE4`) with recessed matte carbon wells (`#181A1F`), specular `1px` top bevels, and physical rotary throughput dials.
  - *Typography*: `Syne` / `Cabinet Grotesk` bold industrial labels + `JetBrains Mono` LED seven-segment-inspired readouts.
  - *Layout*: Full-viewport interactive patch-bay where users drag virtual cables between edge nodes and watch real-time replication latency curves morph.

Notice how Directions B and C immediately look and feel **nothing like** a generic AI template—and nothing like the standard "Sloppi v1 dark tungsten terminal"!

---

## 3. The Pre-Implementation Design Originality Gate

Before selecting your winning direction and coding, run every candidate through this **5-Point Originality Gate**. If a direction fails any check, **reject or mutate it immediately**:

```
┌────────────────────────────────────────────────────────────────────────┐
│               THE PRE-IMPLEMENTATION ORIGINALITY GATE                  │
│                                                                        │
│ 1. THE FIRST-REFLEX REJECTION TEST                                     │
│    Is this the very first aesthetic an LLM thinks of for this prompt?  │
│    (e.g., dark slate + neon green for dev tools; white + navy + 1px    │
│    borders for fintech; purple glow for AI). If YES ──► REJECT IT.     │
│                                                                        │
│ 2. THE SILHOUETTE SQUINT TEST                                          │
│    If you blur the page to 20px, is the silhouette just a centered     │
│    header over rectangular card rows or a standard 8+4 bento grid?     │
│    If YES ──► Redesign the spatial composition before coding.          │
│                                                                        │
│ 3. THE TYPOGRAPHIC VOICE TEST                                          │
│    Did you default to `Inter`, `Roboto`, `Plus Jakarta Sans`, or       │
│    `Geist` paired with `11px uppercase tracking-widest` mono labels?   │
│    If YES ──► Choose a bolder, domain-distinctive font pairing.        │
│                                                                        │
│ 4. THE "WIREFRAME IN DISGUISE" TEST                                    │
│    Did you strip away all gradients, shadows, lighting, and textures   │
│    until the page is just flat white/dark boxes with `1px` borders?    │
│    If YES ──► Add authentic materiality (grain, specular lighting,     │
│    custom SVG artwork, tonal depth, or sculptural typography).         │
│                                                                        │
│ 5. THE PRIMARY MOMENT & INTERACTION FIT TEST                           │
│    If the direction is interactive or motion-led, does it name the     │
│    exact product moment improving feedback, orientation, or continuity?│
│    If it is a quiet direction, do hierarchy, spacing, and immediate    │
│    domain proof communicate clearly without generic hero boilerplate?  │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 4. Eight High-Craft Art Direction Vocabularies (Beyond Flat Wireframes)

Never fall into a single house style. Draw from diverse visual traditions and combine them in unexpected ways:

1. **Swiss Neo-Brutalist Poster & Kinetic Type**: Monumental display typography (`clamp(3.5rem, 9vw, 8.5rem)`), exposed structural rules, stark chromatic blocks (International Klein Blue, cadmium yellow, vermilion, raw newsprint), zero rounded cards, and scroll-linked typographic displacement.
2. **Editorial Broadsheet & Literary Luxury**: High-contrast serif display type (`Playfair Display`, `Newsreader`, `Instrument Serif`, `Cormorant Garamond`), asymmetric magazine columns, drop caps, warm archival paper tones, fine hairline engravings, and unhurried cinematic transitions.
3. **Tactile Hardware & Dieter Rams Industrial**: Anodized metallic or matte polycarbonate surfaces, subtle inner shadows (`inset 0 1px 2px`), specular top highlights (`rgba(255,255,255,0.6)`), physical toggle switches, detented rotary sliders, and laser-etched legends.
4. **Atmospheric Optical Depth & Shader Canvas**: Deep perceptual OKLCH color fields, interactive HTML5 Canvas / WebGL shader backdrops that respond to pointer velocity or product state, refractive glass overlays used *only* over live moving layers, and razor-sharp foreground typography.
5. **Cartographic & Scientific Monograph**: Coordinate grid ticks, isometric or orthographic SVG schematics, contour lines (`stroke-dasharray`), margin annotations, footnotes, and interactive mathematical plots.
6. **Warm Humanist Craft & Organic Studio**: Sunlit terracotta, sage, raw linen, and espresso palettes; expressive rounded serif or humanist sans (`Fraunces`, `Bricolage Grotesque`); overlapping collage compositions; and tactile spring-physics micro-interactions.
7. **High-Velocity Kinetic Consumer / Stickers**: Bold multi-accent color blocking, crushed heavy display fonts (`Syne`, `Clash Display`, `Unbounded`), crisp `2px` solid ink outlines, hard offset shadows (`4px 4px 0px`), and bouncy spring choreography.
8. **Spatial Workbench & Infinite Canvas**: Viewport-locked (`100dvh`) multi-dock studio environment, pannable/zoomable node graph or timeline canvas, floating radial tool palettes, and sub-millisecond keyboard shortcut ergonomics.

---

## 5. Visual-First Prototyping & Dual Verification Mandate

Never write 10 components blindly and only check the browser at the end.
1. **Build and Prototype in the Primary Composition First**: Implement the global tokens (`globals.css`), typography, and **above-the-fold hero / core flow** first—prototyping any proposed motion directly inside that primary composition ([implementation/interaction-implementation.md](../implementation/interaction-implementation.md)).
2. **Verify Static Hierarchy + Live Timing**: Capture **screenshots** to verify layout, spacing, and typographic hierarchy, and capture a **browser recording or interaction trace** to inspect timing, continuity, touch/keyboard response, and repeated activation.
3. **Evaluate Against Your Chosen Direction**:
   - Does it actually look like a distinctive, art-directed piece of design, or did it regress into a generic Tailwind template?
   - Is the display typography commanding? Do quiet moments breathe cleanly, and do motion-led moments improve feedback, orientation, or continuity?
4. **Course-Correct Before Scaling**: Fix any visual flatness or motion lag in the primary composition **before** building the remaining sections, using the proven visual language as the benchmark for the rest of the application.
