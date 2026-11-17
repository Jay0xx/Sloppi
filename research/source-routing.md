# Sloppi Source Routing & Prioritization Matrix

Source routing is the mechanism by which a coding agent maps specific design questions to the most authoritative primary and secondary design galleries.

Agents must not browse sources randomly. They must route questions based on functional domains and prioritize sources according to their relevance to the immediate task.

---

## 1. Domain Routing Matrix

Route every design question to its specialized primary source first, open the **actual example, clip, or live site** rather than stopping at thumbnails, and pair motion-heavy explorations with a minimal-motion restraint check:

| Design Question Domain | Start Here (Primary) | Companion / Secondary Sources | Minimal-Restraint or Tooling Check | What to Extract |
| :--- | :--- | :--- | :--- | :--- |
| **Typography, Pairings & Scale** | **Typewolf**<br>`typewolf.com` | **Minimal Gallery** (`minimal.gallery`), **Refero Styles** (`styles.refero.design`) | **Dead Simple Sites** (`deadsimplesites.com`) | Display/body/mono pairing contrast, optical scale ratio, crushed vs. open leading, reading measure. |
| **Specific Section or Page Element** | **Unsection**<br>`unsection.com` | **Supahero** (`supahero.io`), **Navbar/CTA/Deck/Footer Galleries** | **Minimal Gallery** (`minimal.gallery`) | Deep link to section example, column split, focal entry order, padding rhythm, element count. |
| **iOS Gestures & Mobile State Transitions** | **Spotted in Prod**<br>`spottedinprod.com` | **60fps.design** (`60fps.design`), **Loadmo.re** (`loadmo.re`) | **Dissolve** (`dissolve.rselmi.com`), **Waves** (`libraries.dev/waves`) | Clip deep link, trigger, what moves, what stays anchored, how it settles, `[INFERRED]` internals. |
| **Experimental Composition & Navigation** | **Hover States**<br>`hoverstat.es` | **Awwwards** (`awwwards.com`), **Godly** (`godly.website`) | **Dead Simple Sites** (`deadsimplesites.com`) | Live site deep link, unconventional grid/nav structure, trigger/settlement behavior, DOM feasibility. |
| **Sparse Composition & Minimal-Motion Test** | **Dead Simple Sites**<br>`deadsimplesites.com` | **Minimal Gallery** (`minimal.gallery`) | **Typewolf** (`typewolf.com`) | How much hierarchy, spacing, and typography communicate with minimal or zero motion. |
| **Moodboards, Imagery, Material & Color** | **Cosmos**<br>`cosmos.so` | **Dribbble** (`dribbble.com`), **Godly** (`godly.website`) | *Discard literal artwork* | Cluster mood, tactile surface textures, lighting temperature, value/contrast relationships. |
| **Visual Techniques, Framing & Pacing** | **Eyecandy**<br>`eyecannndy.com` | **Awwwards** (`awwwards.com`), **60fps.design** (`60fps.design`) | *Open in real browser* | Framing geometry, transition cuts, pacing cadence, spatial continuity across state shifts. |
| **Activation-Point Transitions & Interactive Demos** | **Distortion Waves** (`libraries.dev/waves`) | **Dissolve** (`dissolve.rselmi.com`), **Oxyn** (`oxyn.space`), **Wobli** (`wobli.space`) | **DesignEng Tools** (`designeng.tools`) | Verify live in browser; separate demo mechanics from implementation docs, dependency cost, and license. |
| **Design-Engineering Tools & Components** | **DesignEng Tools**<br>`designeng.tools` | *Follow entries to original upstream source* | `implementation/dependency-policy.md` | Upstream repo/doc deep link, stack fit, bundle/peer requirements, and OSS license. |
| **Product / Industry Taxonomy** | **SaaSPO**<br>`saaspo.com` | **Unsection** (`unsection.com`), **Recent.design** (`recent.design`) | **Deck.Gallery** (`deck.gallery`) | Domain proof architecture, credible workflow patterns, and category clichés to subvert. |

---

## 2. The 3-Tier Source Prioritization Model

To avoid cognitive overload and research waste, Sloppi classifies sources into three operational tiers for every task:

```
┌────────────────────────────────────────────────────────┐
│ 1. PRIMARY RESEARCH (60–70% of research time)          │
│ Direct answers to the core design problem.             │
├────────────────────────────────────────────────────────┤
│ 2. SECONDARY RESEARCH (20–30% of research time)        │
│ Adjacent architectural context (navigation, mobile).   │
├────────────────────────────────────────────────────────┤
│ 3. TERTIARY INSPIRATION (0–10% of research time)       │
│ Creative mood exploration (consulted only if needed).  │
└────────────────────────────────────────────────────────┘
```

### Classification Definitions

1. **Primary Research Sources**:
   - Sources that solve the exact functional, structural, or category-specific problem at hand.
   - Example: For a Developer Tool pricing page, Primary Sources are **SaaSPO** (pricing category) and **Refero Styles** (developer tool tokens).

2. **Secondary Research Sources**:
   - Sources that provide critical structural constraints for adjacent components.
   - Example: For the same Developer Tool pricing page, Secondary Sources are **CTA Gallery** (pricing button tiers) and **Navbar Gallery** (header context).

3. **Tertiary Inspiration Sources**:
   - Broad visual discovery feeds used only when seeking unexpected aesthetic tension or creative art direction.
   - Example: **Inspora** or **Posts.design** for color harmony exploration.

---

## 3. Cross-Category Routing Examples

Real design problems rarely fit neatly into a single source. Sloppi agents synthesize across complementary sources:

### Scenario 1: A B2B Fintech Lending Dashboard & Landing Page
- **Primary Sources**:
  - `SaaSPO` (Finance category): Extract credible compliance structures and loan calculator architectures.
  - `Refero Styles`: Extract high-contrast mathematical typography tokens and calm neutral color palettes.
  - `Minimal Gallery`: Extract whitespace discipline to keep dense loan terms readable.
- **Secondary Sources**:
  - `Supahero`: Analyze high-trust, dual-column hero layouts.
  - `CTA Gallery`: Extract high-assurance action copy ("Check Your Rate · Zero Impact on Credit Score").
  - `Footer.design`: Extract multi-column regulatory and FDIC disclosures.
- **Excluded Sources**:
  - `Inspora` (avoid overly theatrical or chaotic art experiments).
  - `Recent.design` (avoid fleeting crypto micro-trends).

### Scenario 2: A High-Performance Developer CLI & Cloud Orchestration Platform
- **Primary Sources**:
  - `SaaSPO` (Developer Tools category): Extract terminal showcase patterns, telemetry graphs, and quickstart blocks.
  - `Refero Styles`: Extract monospaced typography ratios, dark canvas tokens, and tight spacing scales.
- **Secondary Sources**:
  - `Navbar Gallery`: Select a dense, technical command-palette / sidebar hybrid navigation.
  - `60fps.design`: Extract instantaneous (100ms) copy-to-clipboard and terminal output streaming transitions.
  - `Loadmo.re`: Refactor complex terminal output for narrow mobile viewports.
- **Tertiary Sources**:
  - `LogoInspo`: Derive subtle geometric status symbols from the tool's CLI monogram.

### Scenario 3: A Typography-Led Editorial Landing Page
- **Primary Sources**:
  - `Typewolf`: Open live featured sites to extract display-to-body pairing contrast, optical sizing, and reading hierarchy.
  - `Dead Simple Sites`: Benchmark how much composition, whitespace, and scale communicate with minimal or zero motion.
  - `Unsection`: Inspect specific editorial hero, index, and essay/feature section layouts without generic 3-card clutter.
- **Secondary Sources**:
  - `Cosmos`: Extract archival paper textures, ink contrast temperatures, and editorial photography crops (discard literal imagery).
  - `Hover States`: Inspect one experimental navigation or asymmetric column option for `Direction C`.
- **Excluded / Guarded Sources**:
  - Heavy kinetic illustration or WebGL transition libraries (`wobli.space`, `libraries.dev/waves`) unless a specific product moment justifies motion over pure typographic clarity.

### Scenario 4: A Mobile Flow Where a State Change Needs Clearer Feedback
- **Primary Sources**:
  - `Spotted in Prod`: Open shipped iOS interaction clips to capture trigger, moving elements, anchored context, and settlement behavior.
  - `Distortion Waves` (`libraries.dev/waves`): Inspect `Preview` separately from `Install` docs to study transitions originating at the tap button while keeping totals/labels anchored.
  - `Loadmo.re` & `60fps.design`: Extract thumb-zone ergonomics, bottom-sheet continuity, and touch response timing.
- **Secondary / Tooling Sources**:
  - `Dissolve` (`dissolve.rselmi.com`): Study mobile exit/deletion causality and swipe-threshold feedback (without importing React Native Skia into a web stack).
  - `DesignEng Tools`: Follow relevant gesture/toast/sheet entries to their original source to evaluate stack fit, dependency cost, and licensing.
- **Restraint Check**:
  - `Dead Simple Sites`: Verify whether an instant anchored label/badge change already solves clarity under `prefers-reduced-motion` and repeated taps.
