# Sloppi Core Design Principles

Sloppi is a design intelligence system for coding agents. Its purpose is to guide agents away from generic, reflexive, low-intent visual defaults toward deliberate, high-conviction product interfaces.

---

## 1. Anti-Default, Not Anti-Style
The enemy of good design is not aesthetic exuberance, nor is it severe minimalism. The enemy is **unconscious default behavior**.
- An AI coding agent must not default to purple gradients, dark glassmorphism, floating cards, and centered heroes simply because those patterns saturated its training weights.
- Conversely, Sloppi does not mandate a single dogmatic aesthetic. A playful consumer app should feel vibrant and expressive; a precision financial terminal should feel dense, calm, and rigorous; an editorial blog should prioritize typographic rhythm.
- **Anti-default means every visual decision has an explicit product-specific justification.**

## 2. A Pattern is Not Bad Simply Because AI Uses It
A card layout, a pill badge, or a subtle border gradient is not inherently defective.
- Patterns become "slop" only when applied mechanically, without understanding their communicative function.
- A card is appropriate when grouping distinct, interactable entities with heterogeneous content. A card is slop when wrapped around a single line of plain text just to create a container.
- Evaluate patterns by their **functional and communicative utility**, never by superficial prejudice.

## 3. Research Before Invention
Design without context is guessing. Before writing CSS or architecting component trees, an agent must ground its decisions in domain research.
- Inspect how real products in the target category solve similar information hierarchy challenges.
- Study authentic typography pairings, density expectations, and interaction patterns.
- Research does not mean endless browsing; it means targeted extraction of constraints, vocabulary, and visual tone before coding begins.

## 4. Synthesis Over Imitation
Never copy a single reference website or design system wholesale.
- Direct copying produces counterfeit artifacts that ignore the unique constraints of the current product.
- **Synthesis** means extracting principles from multiple complementary domains: taking structural layout from an industry benchmark, typographic discipline from an editorial publication, and micro-interaction timing from a mobile app.
- Combine these inputs into a novel, coherent design thesis documented in `DESIGN.md`.

## 5. Product Specificity
Visual form must directly reflect the product's functional reality, audience expectations, and operational stakes.
- A developer CLI tool requires high information density, monospaced data alignment, subtle contrast, and minimal decorative overhead.
- A high-wealth wealth management dashboard requires visual gravity, restrained color palettes, high typographic authority, and absolute clarity of numerical data.
- A creative social platform requires kinetic energy, expressive geometries, and dynamic color accents.
- If two radically different products end up looking interchangeable, the agent has failed the principle of product specificity.

## 6. Composition Before Decoration
Strong visual design begins with layout, negative space, proportion, and hierarchy—not with decorative filters and background blobs.
- Establish visual hierarchy through typography scale, asymmetric spacing, and alignment before adding colors or borders.
- If a layout fails in monochrome wireframe, adding a multi-stop mesh gradient will only make it a decorative mess.
- Restraint and whitespace are active design tools, not empty voids waiting to be filled with cards.

## 7. Purposeful Motion
Motion must communicate state change, spatial hierarchy, causality, or user confirmation.
- Never add animation simply because "it looks dynamic."
- Motion should orient the user: showing where an expanded item came from, confirming that a destructive action was recorded, or smoothing a heavy data transition.
- Respect user preferences (`prefers-reduced-motion`) and keep durations crisp (100–250ms for micro-actions, 300–450ms for major view transitions).

## 8. Responsive Design as Composition
Mobile viewports are independent ergonomics environments, not merely shrunk-down desktop screens.
- Desktop multi-column comparisons must be re-architected into mobile-native narrative blocks, swipe carousels, or bottom-anchored sheets.
- Touch ergonomics dictate navigation placement (thumb zone at bottom vs. top header).
- Typography scales must be optically adjusted for hand-held reading distances.

## 9. Content is Part of Design
Copywriting and visual layout are inseparable. Generic AI placeholder text ("Empower your seamless workflow with next-gen synergy") destroys visual authenticity.
- Real layout constraints depend on real content length, real technical vocabulary, and realistic numerical data.
- Use realistic, product-specific micro-copy, believable metrics, authentic user personas, and precise value propositions.
- An agent must write high-intent copy as an integral phase of interface design.

## 10. Consistency Without Monotony
A design system must create visual coherence across an entire product without forcing every section into an identical structural template.
- Coherence comes from a shared token system: consistent typography scale, shared color roles, standardized spacing units, and unified border-radius logic.
- Avoid repetitive monotony (e.g., stacking four consecutive sections of 3-card grids). Vary section density, visual weight, asymmetry, and background ground tones.

## 11. Distinctiveness
The final interface must possess an identifiable visual point of view.
- When someone views the interface, they should perceive intentional art direction, whether subtle or bold.
- Distinctiveness is achieved through sharp typographic hierarchy, bespoke color harmonies, intentional geometry, and purposeful section rhythm.
