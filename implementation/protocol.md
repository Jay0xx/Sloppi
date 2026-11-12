# Sloppi v2.0 Visual-First Implementation Protocol

Implementation in Sloppi v2.0 is **visual-first and iterative**.

A coding agent must never write 15 components blindly from top to bottom and only inspect the browser at the very end. If the primary composition (the hero or core workspace) looks flat, generic, or timid in the browser, building 10 more sections on top of it only compounds the mediocrity.

---

## 1. The Visual-First Implementation Sequence

```
┌────────────────────────────────────────────────────────────────────────┐
│               SLOPPI v2.0 VISUAL-FIRST BUILD SEQUENCE                  │
│                                                                        │
│ 1. DIVERGE & GATE      ──► Formulate 3 distinct directions (A/B/C),    │
│                            pass the Originality Gate, write DESIGN.md. │
│                                  │                                     │
│                                  ▼                                     │
│ 2. FONTS & TOKENS      ──► Load distinctive web fonts (never default   │
│                            to Inter) & inject semantic tokens in :root.│
│                                  │                                     │
│                                  ▼                                     │
│ 3. PRIMARY COMPOSITION ──► Build the above-the-fold Hero OR core       │
│    PROTOTYPE FIRST         interactive workspace + navigation +        │
│                            signature 5-second interactive centerpiece. │
│                                  │                                     │
│                                  ▼                                     │
│ 4. LIVE VISUAL PROOF   ──► Render in the browser, capture screenshot,  │
│    GATE (MANDATORY!)       and evaluate against references & thesis:   │
│                            • Does it have bold art direction?          │
│                            • Is the typographic scale dramatic?        │
│                            • Does the interactive hook work?           │
│                            If flat/generic ──► Fix NOW before scaling! │
│                                  │                                     │
│                                  ▼                                     │
│ 5. SCALE FULL          ──► Build remaining sections/screens modulating │
│    INTERFACE               spatial rhythm, ground tones, & mechanics.  │
│                                  │                                     │
│                                  ▼                                     │
│ 6. MULTI-VIEWPORT QA   ──► Inspect 390px, 768px, 1280px+ screenshots,  │
│    & REGRESSION DIFF       fix defects, compare Before/After, & ship.  │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Defeating Both "The Polish Trap" AND "The Wireframe Trap"

Coding agents fail at visual craft in two opposite ways:
- **Trap A — The Polish Trap (Gen-1 Slop)**: Trying to save a weak layout by slapping purple blur blobs, neon drop shadows, and glassmorphism onto generic 3-card grids.
- **Trap B — The Wireframe Trap (Gen-2 Slop)**: Stripping away all lighting, texture, depth, and motion until the page is just flat white or dark rectangles with `1px solid` borders and `11px` monospace labels.

### The Sloppi v2.0 High-Craft Remediation Matrix

| Visual Symptom in Browser | ❌ Gen-1 Slop Reflex | ❌ Gen-2 Wireframe Reflex | ✅ Sloppi v2.0 High-Craft Remediation |
| :--- | :--- | :--- | :--- |
| **Page feels boring / flat** | Add purple/cyan blur blobs in background | Draw flat `1px` boxes around everything | Push typographic scale contrast (`clamp(3rem, 7vw, 6rem)` serif/display vs `16px` body), introduce warm surface materiality/grain or bold chromatic blocking, and create asymmetric negative space. |
| **Hero feels static / generic** | Add tilted 3D dashboard screenshot | Add a generic dark terminal box with `$ npm i` | Build a domain-specific **interactive instrument** (scrubbable timeline, live node patch-bay, interactive calculator, morphing schematic) right in the primary viewport. |
| **Surfaces feel lifeless** | Heavy black drop-shadows (`shadow-2xl`) | Zero depth—everything is flat `#fff` with `#e5e7eb` border | Use tactile materiality: subtle SVG noise texture, `1px` specular top inner highlight (`inset 0 1px 0 rgba(255,255,255,0.6)`), recessed input wells, or multi-layer ambient elevation. |
| **Sections blend together** | Add wavy SVG dividers | Stack 5 sections with identical `1px` top borders | Modulate both **spatial architecture and ground tone**: follow a full-bleed dark/chromatic interactive showcase with an expansive, sunlit single-column editorial manifesto. |
| **Interactions feel dead** | Infinite spinning icons & scroll-jacking | Abrupt `hover:bg-gray-100` only | Orchestrate spring-physics state transitions (`motion`), shared `layoutId` indicators, magnetic/tactile button feedback (`active:scale-[0.98]`), and live tabular number interpolation. |

---

## 3. Design Drift Governance

If browser inspection during Stage 4 (`Live Visual Proof Gate`) reveals that a token, font ratio, or layout proportion needs adjustment to make the design sing, **make the improvement boldly** and synchronize `DESIGN.md` so the contract always reflects the proven visual reality.
