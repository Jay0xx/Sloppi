# Sloppi Reference Analysis & Principle Extraction

Reference Analysis is the structural decomposition of selected design references to extract transferable rules while discarding non-transferable surface artifacts.

A coding agent must never copy a reference website's visual skin. It must analyze the underlying architectural logic that makes the design effective.

---

## 1. Structural Reference Decomposition Schema

For each reference in the constellation, the agent must document the following structural breakdown:

```markdown
### Reference Decomposition: [Reference Name]
- **URL**: `[URL]`
- **Reason Selected**: [Specific design question this reference resolves]

#### 1. Product & Audience Context
- What kind of product or business is this?
- What user mental model does the design address?

#### 2. Composition & Spatial Flow
- How is the page structured across major narrative sections?
- Where is macro-whitespace used to create breathing room?

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
- Wayfinding Pattern: [Floating pill, sticky bar, sidebar dock, or mega-menu]
- Link Hierarchy & Discovery: [Primary routes vs. utility controls]

#### 10. Interaction & Motion Dynamics
- State Feedback: [Hover brightness shifts, active scale down, focus rings]
- State Transitions: [Durations, easing curves, spatial continuity]

#### 11. Imagery, Media & Textures
- Media Type: [Real product UI, interactive code sandbox, technical diagrams, or photography]
- Framing & Containment: [Bordered screenshots, browser chrome wrappers, or raw bleed]

#### 12. Content & Copywriting Impact
- Headline Length & Balancing: [Character count, balance wrapping]
- Action Micro-Copy: [Outcome-explicit verbs vs. generic labels]

#### 13. Distinctive Point of View
- What single visual or architectural decision makes this reference recognizable compared to generic templates?

---

#### 14. MANDATORY: Transferable Principles (The Underlying Rules)
- What fundamental design principles can Sloppi extract and apply to our product?

#### 15. MANDATORY: Non-Transferable Details (What NOT to Copy)
- What specific colors, proprietary illustrations, brand logos, copy, or idiosyncratic decorative artifacts must be explicitly rejected?
```

---

## 2. Principle Extraction: Bad vs. Good Examples

The fundamental skill in reference analysis is converting surface observations into reusable mathematical or ergonomic rules:

| Surface Observation (❌ Bad / Superficial) | Extracted Principle (✅ Good / Sloppi Rule) |
| :--- | :--- |
| *"Use a large black heading."* | **Typographic Scale Hierarchy**: Use an extreme scale step ($48\text{px}+$) with compressed leading ($0.95–1.00$) to establish an unmistakable top-of-fold visual anchor without relying on decorative box containers. |
| *"Use rounded cards with soft borders."* | **Bounded Surface Rule**: Bounded card surfaces are reserved strictly for heterogeneous, independently actionable entities. Continuous narrative text rests directly on the canvas ground. |
| *"Use a dark blue background with purple buttons."* | **Color Contrast Architecture**: High-stakes data products achieve optical calm by using a low-saturation neutral canvas (`#0b0d13`) paired with a single high-luminance brand accent reserved exclusively for primary interactive state changes. |
| *"Use a sticky navigation bar with a blur."* | **Persistent Wayfinding Ergonomics**: When a page contains long-form sequential content exceeding 3 viewports, retain a low-profile sticky header with a primary conversion trigger to eliminate back-to-top scroll friction. |
| *"Put 3 cards in the feature section."* | **Asymmetric Feature Modulation**: Rather than repeating identical 3-column cards, use an asymmetric layout (e.g., 65% interactive live demo + 35% capability breakdown) to spotlight the product's primary differentiator. |
| *"Use animated glowing borders."* | **Purposeful State Indication**: Use subtle perimeter luminance shifts ($150\text{ms}$ transition) strictly to indicate an active running background process or selected keyboard focus state. |

---

## 3. The Golden Rule of Extraction

> **Extract the mathematical ratio, the semantic relationship, and the ergonomic solution.**  
> **Discard the brand colors, the proprietary artwork, and the literal visual skin.**
