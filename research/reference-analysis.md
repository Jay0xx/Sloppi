# Sloppi Reference Analysis & Principle Extraction

Reference Analysis is the structural decomposition of selected design references to extract transferable rules while discarding non-transferable surface artifacts.

A coding agent must never copy a reference website's visual skin. It must analyze the underlying architectural logic that makes the design effective.

---

## 1. Structural Reference Decomposition Schema

Always open the **actual example, live site, or interaction clip** when available rather than analyzing a gallery card thumbnail. For each reference in the constellation, document the following breakdown—marking any unverified timing, threshold, or off-frame detail as `[INFERRED]`:

```markdown
### Reference Decomposition: [Reference Name]
- **Registry Channel**: `[e.g., Typewolf | Unsection | Spotted in Prod | Hover States | Dead Simple Sites | DesignEng Tools]`
- **Deep Link Inspected**: `[Exact URL of example, clip, live site, or upstream source]`
- **Verification Status**: `[OBSERVED (Live Browser) | PARTIAL ([INFERRED] items tagged) | INACCESSIBLE (<status> — fallback used)]`
- **Reason Selected**: [Specific design question this reference resolves]

#### 1. Product & Audience Context
- What kind of product or business is this?
- What user mental model does the design address?

#### 2. Composition & Spatial Flow (Observed Behavior or Composition)
- How is the page or section structured across narrative beats?
- Where is macro-whitespace or sparse density used to communicate without decorative motion?

#### 3. Visual Hierarchy & Scanning Order
- First Entry Point: [Element that commands immediate attention]
- Secondary Focus: [Supporting explanation or interactive proof]
- Tertiary Focus: [Navigation, auxiliary links, timestamps]

#### 4. Typography Architecture
- Display Typeface: [Family, weight, optical sizing, line-height ratio]
- Body/UI Typeface: [Family, weight, letter-spacing compensation]
- Modular Scale: [Estimated ratio, e.g., Minor Third vs. Perfect Fourth]

#### 5. Color Strategy & Semantic Roles
- Canvas Ground: [Hex / tone]
- Reading Contrast: [Text primary / secondary]
- Brand Anchor: [Signature hue & role]
- Accent Roles: [Functional highlights, badges, status colors]

#### 6. Geometry, Radii & Surface Depth
- Corner Radii Progression: [e.g., tags: 4px, buttons: 6px, cards: 12px]
- Border Logic: [1px solid, subtle opacity, or borderless]
- Elevation Model: [Flush flat, low-opacity ambient occlusion, or hard shadow]

#### 7. Spacing & Density
- Base Unit: [4px or 8px]
- Section Gap: [Vertical spacing between major blocks]
- Card Internal Padding: [Compact vs. Comfortable vs. Spacious]

#### 8. Layout & Grid Symmetry
- Grid Model: [12-column, split 50/50, asymmetric bento, or single-column reading column]
- Spatial Alignment: [Left-aligned editorial vs. centered]

#### 9. Navigation Architecture
- Wayfinding Pattern: [Floating pill, sticky bar, sidebar dock, or experimental nav]
- Link Hierarchy & Discovery: [Primary routes vs. utility controls]

#### 10. Interaction & Motion Dynamics (4-Part Motion Capture)
- **Trigger**: [Exact tap, click, swipe/drag threshold, focus, or state change]
- **What Moves**: [Which layers, coordinates, or fields animate]
- **What Stays Anchored**: [Which containers, values, or layout frames hold steady for orientation]
- **How It Settles**: [End state, easing/spring feel, edge/residual cue, reset/interrupt behavior]
- **Inferred Details**: [Explicitly tag `[INFERRED]` for any duration, curve, haptic, or offscreen mechanic not directly verified]

#### 11. Imagery, Media & Textures
- Media Type: [Real product UI, interactive demo, technical diagrams, or photography]
- Framing & Containment: [Bordered screenshots, browser chrome wrappers, or raw bleed]

#### 12. Content & Copywriting Impact
- Headline Length & Balancing: [Character count, balance wrapping]
- Action Micro-Copy: [Outcome-explicit verbs vs. generic labels]

#### 13. Distinctive Point of View & Implementation Separation
- What single visual or architectural decision makes this reference recognizable?
- *(If from `designeng.tools`, `libraries.dev/waves`, `dissolve.rselmi.com`, `oxyn.space`, or `wobli.space`)*: Separate **observed demo behavior** from **implementation docs** (runtime stack, bundle/peer cost, license). Never treat a demo as an automatic dependency.

---

#### 14. MANDATORY: Design Principle Worth Adapting & Product Fit
- **Principle Worth Adapting**: [Fundamental compositional, typographic, or behavioral rule extracted]
- **Where It Serves the Current Product**: [Exact page, section, or product moment—feedback, orientation, continuity, or quiet typographic clarity]

#### 15. MANDATORY: Non-Transferable Details (What NOT to Copy)
- What specific colors, proprietary illustrations, brand logos, copy, or heavy runtime dependencies must be explicitly rejected?
```

---

## 2. Principle Extraction: Bad vs. Good Examples

The fundamental skill in reference analysis is converting surface observations into reusable mathematical, compositional, or behavioral rules—marking inferred details honestly:

| Surface Observation (❌ Bad / Superficial) | Extracted Principle & Product Fit (✅ Good / Sloppi Rule) |
| :--- | :--- |
| *"Use a large black heading."* | **Typographic Scale Hierarchy**: Use an extreme scale step ($48\text{px}+$) with compressed leading ($0.95–1.00$) to establish an unmistakable top-of-fold visual anchor without relying on decorative box containers. *Serves*: Editorial hero entry point. |
| *"Use rounded cards with soft borders."* | **Bounded Surface Rule**: Bounded card surfaces are reserved strictly for heterogeneous, independently actionable entities. Continuous narrative text rests directly on the canvas ground. *Serves*: Essay/methodology sections. |
| *"Use a dark blue background with purple buttons."* | **Color Contrast Architecture**: High-stakes data products achieve optical calm by using a low-saturation neutral canvas (`#0b0d13`) paired with a single high-luminance brand accent reserved exclusively for primary interactive state changes. |
| *"Put 3 cards in the feature section."* | **Asymmetric Feature Modulation**: Rather than repeating identical 3-column cards, use an asymmetric layout (e.g., 65% interactive live demo + 35% capability breakdown) to spotlight the product's primary differentiator. |
| *"Copy the Distortion Waves shader library."* | **Activation-Point State Continuity** *(from `libraries.dev/waves` `Preview`)*: **Trigger**: Primary confirm tap/click. **Moves**: State fields transition upward from the trigger anchor while **Anchored**: numeric total, unchanged rows, frame, and button stay fixed; **Settles**: confirmed receipt (`[INFERRED]` exact shader duration). *Principle*: Anchor state transitions at the trigger element while keeping stable context fixed; implement with lightweight CSS/View Transitions rather than adding WebGL2/Metal dependencies. |
| *"Add animations everywhere so it feels alive."* | **Minimal-Motion Restraint Check** *(from `deadsimplesites.com`)*: Test whether scale contrast (`4:1+`), disciplined `60ch` line measure, and asymmetric margin whitespace already establish reading order—reserving motion strictly for moments needing clearer state feedback, orientation, or continuity. |

---

## 3. The Golden Rule of Extraction

> **Extract the mathematical ratio, the semantic relationship, and the causal behavior (trigger, moves, anchored, settles).**  
> **Discard the brand skin, proprietary artwork, and unexamined demo dependencies.**
