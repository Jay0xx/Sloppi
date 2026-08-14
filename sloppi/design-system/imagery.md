# Sloppi Imagery & Media Architecture

Imagery in Sloppi encompasses product user interfaces, technical diagrams, photography, 3D assets, textures, and illustrations. 

In a high-intent design system, imagery is an evidentiary tool that demonstrates product capabilities, proves performance claims, or establishes immediate human context.

A coding agent must never insert arbitrary stock photography, generic 3D abstract blobs, or fake dashboard illustrations merely to fill empty space.

---

## 1. The 4 Categories of Product Imagery

```
1. PRODUCT UI & WORKFLOW ARTIFACTS ──► High-fidelity screenshots, live interactive demos, code terminals
2. TECHNICAL ARCHITECTURE DIAGRAMS ──► Data pipelines, network flows, sequence diagrams, integration schemas
3. EDITORIAL & HUMAN PHOTOGRAPHY   ──► Authentic customer environments, material textures, physical hardware
4. BRAND MOTIFS & GRAPHIC EMBLEMS  ──► Geometric symbols, iconographic stamps, subtle vector watermarks
```

---

## 2. Product UI & Screenshot Treatment Rules

When presenting the product's actual software interface:

### 1. The Realism & Fidelity Imperative
- **No Wavy Placeholder Lines**: Never use cartoonish squiggly lines or grey rectangular skeletons to represent text in a product screenshot. Show authentic domain data, real metric names, and syntactically valid code.
- **Readable Typography**: Interface screenshots must remain legible at standard viewing resolutions. Avoid extreme 3D tilts or miniature scaling that makes the software unreadable.

### 2. Browser & Window Framing
- **Minimalist Window Chrome**: Wrap web and desktop software previews in a subtle 1px bordered container with three simple window control dots (`6px` circles with `8px` gap) or a clean URL path bar.
- **Aspect Ratio Consistency**: Standardize screenshot containers to `16:10` or `16:9` to prevent irregular vertical jumping across carousel tabs.

---

## 3. Technical Architecture & Data Diagrams

For developer tools, enterprise security, and infrastructure products, technical diagrams provide higher conversion credibility than marketing illustrations:
- **Clean SVG Linework**: Use consistent 1.5px or 2px vector strokes that match the design system's border tokens.
- **Node-and-Edge Geometry**: Match diagram node corner radii to the system's `--radius-md` token ($8\text{px}$).
- **Semantic Data Flow**: Use animated dashed strokes or directional arrows strictly to illustrate data movement and API request lifecycles.

---

## 4. Photography & Texture Treatment

When photography is required (e.g., editorial, physical products, case studies):
- **Aspect Ratio Standards**:
  - Hero Landscape: `16:9` or `21:9`
  - Feature Cards: `4:3` or `16:10`
  - Portrait Avatars / Author Bios: `1:1` square or `4:5` vertical
- **Corner Containment**: Apply `overflow: hidden` and mirror the parent container's corner radius using the concentric radius rule.
- **Color Grading & Tonal Harmonization**: Apply a subtle CSS filter or overlay tint (e.g., `mix-blend-mode: multiply` with `--color-canvas-alt`) to integrate external photography into the brand palette.

---

## 5. Anti-Slop Imagery Guardrails

1. **No Fake 3D Spheres**: Banned: floating purple glass orbs, metallic donuts, and glowing isometric cubes that have no operational connection to the software.
2. **No Uncalibrated Stock Avatars**: Testimonials must feature real verified portraits or company emblems, not generic AI-generated stock model faces.
3. **No Unsubstantiated Benchmark Graphs**: Charts must label both the $X$ and $Y$ axes with real units (e.g., `Time (ms)`, `Throughput (req/s)`), rather than showing unlabelled exponential curves.
