# Sloppi Visual Language & Design Personality

The Visual Language is the overarching aesthetic, spatial, and material grammar of a product. It translates the abstract **Design Thesis** into an observable visual vocabulary that guides every token, layout, and component.

A coding agent must never rely on subjective, unfalsifiable aesthetic buzzwords. Sloppi mandates that all visual language descriptions be expressed through concrete, measurable design characteristics.

---

## 1. The Ban on Vague Aesthetic Buzzwords

Coding agents frequently generate hollow descriptions that cannot be evaluated or implemented. Sloppi translates vague buzzwords into concrete architectural specifications:

| ❌ Vague Buzzword | ❌ Why It Fails | ✅ Sloppi Observable Specification |
| :--- | :--- | :--- |
| *"Make it modern"* | Meaningless; subjective; defaults to current overused tropes. | *"Use asymmetric 2-column layouts, strict typographic scale contrast (48px H1 / 16px body), 1px subtle borders (`#e2e8f0`), and solid neutral canvas grounds."* |
| *"Make it sleek"* | Encourages unthinking dark mode and blue neon glows. | *"Use ultra-low radius geometry (4px–6px), tight 4px baseline density, monospace status metadata, and muted monochrome palettes with a single high-luminance accent."* |
| *"Make it clean"* | Often leads to empty layouts with missing hierarchy. | *"Rely on generous macro-whitespace (96px section padding) to separate chapters; eliminate all non-essential card containers and background gradient blobs."* |
| *"Make it premium"* | Defaults to generic black-and-gold or heavy glassmorphism. | *"Use high-contrast humanistic serif typography for display headlines, warm paper ground tones (`#fbf9f5`), restrained hairline dividers, and deliberate editorial line lengths (60ch)."* |
| *"Make it futuristic"* | Produces chaotic WebGL spheres and illegible neon glows. | *"Use high-density data visualizations, precise tabular alignment, dark carbon canvas (`#0d0e12`), and subtle phosphor-tinted status indicators."* |

---

## 2. Design Personality Diagnostic Dimensions

Sloppi establishes 8 bipolar diagnostic axes to map a product's unique visual personality. The agent selects only the 3 to 5 axes that meaningfully define the product:

```
Restrained     ◄─────────────────────────►     Expressive
Dense          ◄─────────────────────────►     Spacious
Formal         ◄─────────────────────────►     Playful
Technical      ◄─────────────────────────►     Human
Geometric      ◄─────────────────────────►     Organic
Quiet          ◄─────────────────────────►     Energetic
Editorial      ◄─────────────────────────►     Utilitarian
Conservative   ◄─────────────────────────►     Experimental
```

### Personality Axis Mapping in Practice

#### Profile 1: Institutional B2B Fiduciary Platform
- **Restrained** (90%): Monochrome canvas, zero decorative illustrations.
- **Spacious** (70%): Generous breathing room to convey calm stability and clear reading.
- **Formal** (85%): High typographic authority, strict alignment, structured tables.
- **Editorial** (80%): Narrative pull-quotes, multi-column reporting layout.

#### Profile 2: High-Performance Database CLI & Dashboard
- **Technical** (95%): Monospaced data tables, live telemetry streaming, command palette.
- **Dense** (90%): 4px grid baseline, 12px card padding, high information density.
- **Geometric** (85%): Crisp 4px corner radii, straight 1px borders, square grid alignment.
- **Utilitarian** (90%): Zero decorative imagery; every pixel communicates state or data.

#### Profile 3: Tactile Consumer Audio Studio
- **Expressive** (85%): Multi-accent color palette (lavender, mint, ember, electric blue).
- **Playful** (80%): Soft pill-shaped buttons, tactile spring physics, bouncy feedback.
- **Organic** (75%): Large corner curvature (24px–32px), hand-cut carbon outlines.
- **Energetic** (85%): Kinetic micro-animations, interactive waveform visualizers.

---

## 3. The 10 Core Visual Language Facets

When defining the visual language in `DESIGN.md`, the agent must document these 10 concrete facets:

1. **Personality & Archetype**: The selected diagnostic position and tonal identity.
2. **Mood & Atmospheric Temperature**: The psychological environment (e.g., *cool and clinical* vs. *warm and archival* vs. *electric and kinetic*).
3. **Visual Vocabulary**: The recurring physical metaphors (e.g., *sheet of physical paper*, *flight recorder telemetry HUD*, *sticker-book collage*).
4. **Compositional Rhythm**: How sections pace the user's attention (alternating dense comparative tables with spacious editorial breaks).
5. **Spatial Density**: Exact baseline ($4\text{px}$ vs. $8\text{px}$) and container padding conventions.
6. **Contrast Hierarchy**: Where the eye is directed first, second, and third.
7. **Controlled Visual Tension**: The deliberate combination of contrasting qualities (e.g., *technical precision paired with warm paper materiality*).
8. **Brand Expression**: How brand motifs (angles, emblems, typography) naturally permeate UI elements.
9. **Materiality & Surfaces**: How cards and containers reflect light (flat hairline borders vs. multi-layer ambient occlusion).
10. **Distinctive Visual Point of View**: The unmistakable visual signature that differentiates this interface from any generic competitor.
