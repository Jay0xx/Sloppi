# Sloppi Signature Anti-Slop Audit & Default Detection

The Anti-Slop Audit is Sloppi's flagship critique protocol. It evaluates whether an interface exhibits the telltale signs of unthinking, mechanical AI generation.

```
┌────────────────────────────────────────────────────────────────────────┐
│                      THE DEFAULT DETECTION RULE                        │
│                                                                        │
│ "These patterns are NOT absolutely forbidden. They are REVIEW SIGNALS. │
│  For every flagged pattern, the agent must ask:                        │
│  'Does this element have a concrete, product-specific reason to exist?'│
│  If YES: Retain or refine.  If NO: Reconsider and replace."            │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 1. Catalog of 26 AI Default Review Signals

```
[ Rendered Interface Inspection ]
        │
        ├──────► SIGNAL 1:  Generic Centered Hero (Giant Title + 2 Pill Buttons + Floating Dashboard)
        ├──────► SIGNAL 2:  Excessive Rounded Cards (rounded-3xl applied indiscriminately)
        ├──────► SIGNAL 3:  Excessive Pill Badges (Pills stacked above every single section heading)
        ├──────► SIGNAL 4:  Unjustified Gradient Backgrounds (Radial mesh blobs filling empty space)
        ├──────► SIGNAL 5:  Unjustified Gradient Text (Multi-colored rainbow text on every H2)
        ├──────► SIGNAL 6:  Unjustified Glassmorphism (backdrop-filter: blur() on plain backgrounds)
        ├──────► SIGNAL 7:  Excessive Ambient Shadows (Heavy fuzzy drop-shadows on flat cards)
        ├──────► SIGNAL 8:  Excessive Blur Filters (Blurred glowing dots behind UI components)
        ├──────► SIGNAL 9:  Decorative 3D Blobs / Spheres (Floating rendered shapes with zero meaning)
        ├──────► SIGNAL 10: Floating UI Fragments (Tilted mockups with squiggly placeholder lines)
        ├──────► SIGNAL 11: Universal 3-Card Grid Reflex (Stacking 3 identical cards for everything)
        ├──────► SIGNAL 12: Repetitive Feature Sections (Identical card geometry repeated 4 times)
        ├──────► SIGNAL 13: Generic Dashboard Mockups (Fake graphs with missing axes and units)
        ├──────► SIGNAL 14: Decorative Statistics ("10x Faster", "99.9% Growth" with no data source)
        ├──────► SIGNAL 15: Fabricated Social Proof (Unverified quotes, fake avatars, unauthorized logos)
        ├──────► SIGNAL 16: Excessive Badges & Tags (Visual clutter with no filtering function)
        ├──────► SIGNAL 17: Unnecessary Icons (Forcing a generic icon onto every bullet point)
        ├──────► SIGNAL 18: Generic CTA Copy (Repeating "Get Started" or "Learn More" 8 times)
        ├──────► SIGNAL 19: Repeated CTA Banner Blocks (Identical full-width signup boxes every 2 scrolls)
        ├──────► SIGNAL 20: Excessive Section Symmetry (Every section having identical column counts)
        ├──────► SIGNAL 21: Monotone Section Heights (Every section having identical 600px height)
        ├──────► SIGNAL 22: Excessive Centered Body Copy (Centered paragraphs longer than 3 lines)
        ├──────► SIGNAL 23: Arbitrary Whitespace Gaps (160px gaps separating related micro-copy)
        ├──────► SIGNAL 24: Decorative Wavy Dividers (Arbitrary SVG wave transitions between sections)
        ├──────► SIGNAL 25: Excessive Animation / Spinning (Pulsing glowing buttons and spinning badges)
        └──────► SIGNAL 26: Trendy Effects Without Justification (Parallax or scroll-jacking on tools)
```

---

## 2. The "Strip the Effects" Mental Test

To verify that an interface's design strength is structural rather than decorative, the agent executes the **"Strip the Effects" Test**:

```
┌────────────────────────────────────────────────────────────────────────┐
│                 THE "STRIP THE EFFECTS" INTEGRITY TEST                 │
│                                                                        │
│ Mentally (or via CSS override) strip away:                             │
│ • All background gradients & glowing mesh blurs                        │
│ • All drop-shadows & elevation glows                                  │
│ • All glassmorphism blur filters                                       │
│ • All decorative animations & floating transformations                 │
│                                                                        │
│ Then inspect: DOES THE INTERFACE STILL POSSESS A STRONG DESIGN?        │
│                                                                        │
│ • If YES: The design has authentic structural, typographic, and        │
│   compositional integrity. Visual effects are serving as enhancement.  │
│                                                                        │
│ • If NO: The design is hollow slop relying on surface decoration to     │
│   mask weak hierarchy, generic copy, and lazy card grids.              │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Remediation Matrix: Converting Slop into Intentional Design

| Flagged Review Signal | Why It Fails | Sloppi Intentional Replacement |
| :--- | :--- | :--- |
| **Generic Centered Hero** | Conveys zero product-specific reality. | Choose from 10 Hero Paradigms (Split Terminal, Dense Telemetry HUD, Editorial). |
| **Universal 3-Card Grid** | Lazy default representation for heterogeneous concepts. | Map to specific presentation models (Spec Table, Architectural Diff, Sequential Timeline). |
| **Gradient Text Blobs** | Cheap visual gimmick that degrades readability. | Crisp high-contrast display typography with tight letter-spacing (`-0.025em`). |
| **Centered Body Paragraphs** | Severely degrades reading speed and tracking comprehension. | Left-align body copy constrained strictly to `max-width: 65ch`. |
| **Floating 3D Spheres** | Irrelevant decorative filler. | Replace with annotated SVG system architecture diagram or live interactive REPL. |
