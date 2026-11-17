# Sloppi v2.0 Anti-Slop & Anti-Monoculture Audit (30 Signals)

The Anti-Slop Audit screens interfaces against **both** generations of AI frontend failure:
- **Signals 1–20 (Generation-1 AI Slop)**: Default purple/indigo SaaS templates, centered H1 + 2 pills, 3-card icon grids, meaningless blur orbs, and fake social proof.
- **Signals 21–30 (Generation-2 Overfit / Wireframe Slop)**: Sterile flat `1px`-bordered boxes everywhere, automatic `Inter` + `JetBrains Mono` defaults, repeating the same dark-green CLI terminal on every dev tool, repeating the same white/navy `1px` ledger on every fintech app, and slapping `11px uppercase font-mono tracking-widest` above every single element.

---

## 1. The 30 Review Signals

### Part A: Generation-1 AI Slop Signals (1–20)
1. **Generic Centered Hero**: Eyebrow pill + centered H1 + 2 buttons + tilted screenshot underneath.
2. **Indiscriminate `rounded-3xl` Cards**: Every container rounded to toy-like `24px–32px` without brand justification.
3. **Eyebrow Pill Inflation**: `rounded-full bg-primary/10` pills stacked above every section heading.
4. **Unjustified Neon/Purple Blur Blobs**: `filter: blur(120px)` violet/cyan circles disguising an empty layout.
5. **Rainbow Gradient Text**: Multi-color gradient clip text applied to headings as a cheap gimmick.
6. **Glassmorphism Over Flat Solids**: `backdrop-blur` on static cards with nothing scrolling behind them.
7. **Muddy Drop Shadows**: Single-layer dark `rgba(0,0,0,0.4)` shadows on flat in-flow boxes.
8. **Arbitrary Glowing Dots**: Meaningless blurred dots scattered behind cards.
9. **Random 3D Floating Shapes**: Decorative spheres, torus knots, or stars with zero domain meaning.
10. **Squiggly Wireframe Mockups**: Fake UI fragments with placeholder lines instead of real interactive UI.
11. **Universal 3-Card Icon Grid**: Three identical rectangular cards with a colored circle icon on top.
12. **Cookie-Cutter Section Repetition**: Stacking 4 consecutive sections with the exact same card grid.
13. **Axis-Free Fake Charts**: Decorative wavy SVG lines with no units, scales, or interactive inspection.
14. **Unsubstantiated Hyper-Stats**: *"10x Faster"*, *"99.9% Synergy"* with zero methodology or context.
15. **Fabricated Social Proof**: Fake quotes from *"Sarah J., VP of Growth"* or unauthorized Fortune 500 logo clouds.
16. **Non-Interactive Tag Clutter**: Clusters of pills/badges that cannot be clicked or filtered.
17. **Icon-Beside-Every-Bullet**: Forcing a generic Lucide icon onto every single heading and list item.
18. **Generic CTA Copy**: Repeating *"Get Started"* and *"Learn More"* across the page.
19. **Centered Long Paragraphs**: Center-aligning body copy longer than 3 lines (`> 65ch`).
20. **Buzzword Marketing Copy**: *"Supercharge, elevate, seamless, unleash, next-gen velocity."*

### Part B: Generation-2 Overfit & Wireframe Cliché Signals (21–30)
21. **The Flat `1px` Border Wireframe Trap**: Every single section, card, and metric is just a flat white or dark rectangle with a `1px solid` border and zero materiality, lighting, texture, or tonal depth.
22. **Unthinking `Inter` + `JetBrains Mono` Default**: Failing to load an expressive Display/Serif/Grotesque font pairing that gives the brand a unique typographic voice.
23. **The `11px Uppercase Font-Mono Tracking-Widest` Addiction**: Putting the exact same tiny uppercase monospace eyebrow label above every section and inside every card.
24. **The "Midnight Tungsten + Phosphor Green CLI" Reflex**: Automatically styling every developer or technical tool with `#0b0d13` dark slate, `#00d084` green, and a mock terminal window.
25. **The "Warm Alabaster + Navy Ink Ledger" Reflex**: Automatically styling every fintech or B2B app with `#fbf9f5`/`#ffffff`, `#102A56` navy, and flat `1px` bordered tables.
26. **The Cookie-Cutter `8+4` Bento Reflex**: Replacing a 3-card grid with a standard `col-span-8` + `col-span-4` bento grid without bespoke interactive content.
27. **Timid Typographic Scale Contrast**: Display headlines (`32px–40px`) barely larger than section titles (`24px–28px`), lacking sculptural hero presence.
28. **Generic Static Hero Boilerplate**: A hero with a canned tagline + placeholder screenshot where neither commanding typographic proof (in a quiet direction) nor a purposeful product interaction is present.
29. **Dead Controls or Unjustified Demo Effects**: Either interactive controls have zero hover/focus/active/touch/reduced-motion state feedback, OR a heavy reference-demo effect (`waves`, particles, glitch text, idle loops) was bolted on without serving feedback, orientation, or continuity.
30. **Cross-Project Self-Plagiarism**: Reusing the exact same layout skeleton, font stack, or color palette from another recent project in the workspace.

---

## 2. The Dual Integrity & Materiality Test (Replacing "Strip the Effects")

In Sloppi v1, the *"Strip the Effects"* test caused agents to delete all lighting, texture, and depth—resulting in sterile wireframes. Sloppi v2.0 enforces the **Dual Integrity & Materiality Test**:

```
┌────────────────────────────────────────────────────────────────────────┐
│            THE DUAL INTEGRITY & MATERIALITY TEST (v2.0)                │
│                                                                        │
│ TEST A — STRUCTURAL BONES CHECK:                                       │
│ Does the layout have unmistakable typographic hierarchy, asymmetric    │
│ spatial rhythm, and a real interactive centerpiece even without blur   │
│ blobs?                                                                 │
│ • If NO ──► Fix the spatial composition and scale ratio first.         │
│                                                                        │
│ TEST B — ART DIRECTION & MATERIALITY CHECK:                            │
│ Does the interface possess rich, intentional surface craft—such as     │
│ expressive display typography, tactile surface grain, specular `1px`   │
│ bevels, perceptual color blocking, or choreographed motion—so it NEVER │
│ looks like a bare wireframe?                                           │
│ • If NO ──► Elevate surface materiality, font voice, and choreography. │
└────────────────────────────────────────────────────────────────────────┘
```
