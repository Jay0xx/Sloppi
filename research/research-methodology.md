# Sloppi Design Research Methodology

This document outlines how a Sloppi-enabled coding agent conducts design research before writing code.

Design research in Sloppi is a **focused, constraint-driven intelligence extraction process**. It is not passive browsing, nor does it mean scraping random websites and copying their code.

---

## 1. The Research Decision Gate

An agent does not need to research all 15 sources for every task. Before researching, the agent asks:
- **Is this a greenfield interface or major feature addition?** → YES: Conduct structured domain research.
- **Does a comprehensive, approved `DESIGN.md` already exist?** → YES: Research only if adding a novel, unspecified component pattern.
- **Is this a minor layout tweak or bug fix?** → NO: Skip research; adhere strictly to existing project tokens.

---

## 2. The 4-Step Research Workflow

```
[ Step 1: Identify Target Domain & Information Needs ]
                     │
                     ▼
[ Step 2: Route to Specialized Primary Sources ]
                     │
                     ▼
[ Step 3: Extract Structural & Visual Intelligence ]
                     │
                     ▼
[ Step 4: Synthesize Intelligence into Design Thesis ]
```

### Step 1: Identify Information Needs
Determine the exact design questions that require answers:
- What typography pairing, optical scale, and reading hierarchy fits the voice? (Start with **Typewolf**)
- How should a specific section or page element be structured? (Start with **Unsection**, plus **Supahero** / **Navbar/CTA/Deck/Footer Galleries**)
- What gesture behavior or state-transition feedback clarifies touch/mobile flows? (Start with **Spotted in Prod**, paired with **60fps.design**, **Loadmo.re**, or **Distortion Waves** / **Dissolve**)
- What experimental composition, mood, or pacing widens creative options? (Use **Hover States**, **Cosmos**, **Eyecandy**, **Awwwards**, **Godly**)
- How much does the composition communicate with minimal motion? (Benchmark against **Dead Simple Sites** and **Minimal Gallery**)
- What domain conventions should we adopt or subvert, and what stack-fit tools exist? (Use **SaaSPO**, **Refero Styles**, and **DesignEng Tools** followed to its upstream source)

### Step 2: Question-Driven Source Routing
Use [research/source-routing.md](source-routing.md) and [references/source-registry.md](../references/source-registry.md) to select 2 to 4 targeted sources and open actual examples or clips.
- **Do not** browse feeds randomly or cite thumbnails without opening the example/clip.
- **Do not** treat interactive demos (`libraries.dev/waves`, `dissolve.rselmi.com`, `oxyn.space`, `wobli.space`) as automatic dependencies; verify demo behavior separately from implementation docs.

### Step 3: Intelligence Extraction (What to Look For)
When inspecting research references, log:
1. **Deep Link & Verification Status**: Exact example/clip URL, plus `[INFERRED]` on any unverified timing/internals or status/fallback if a demo is inaccessible.
2. **Observed Composition & Typographic Ratios**: Scale steps, line-height proportions, reading measure, negative space rhythm.
3. **Motion Capture (when applicable)**: Trigger, what moves, what stays anchored, and how the interaction settles.
4. **Adaptable Principle & Product Fit**: The structural/behavioral rule worth adapting and where it serves the current product.

### Step 4: Cross-Domain Synthesis
Feed logged insights into the 3-direction divergence ([research/synthesis.md](synthesis.md)):
- Contrast a **quiet hierarchy/spacing direction** (benchmarked against `deadsimplesites.com` and `typewolf.com`) with section-led and motion-led alternatives that name the exact product moment for feedback, orientation, or continuity.
- Ground the winning direction in `DESIGN.md` with explicit stack-fit, cost, and license checks before coding.

---

## 3. What Remains Intentionally Unimplemented in this Phase

To maintain architectural purity and prevent premature complexity:
- Automated web scrapers and headless browser loops are **not** implemented.
- Vector database embeddings of website screenshots are **not** implemented.
- Autonomous visual scrapers are **not** implemented.

The current system provides the **methodological intelligence** that guides the agent's analytical thinking during pair programming.
