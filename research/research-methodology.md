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
- What information density and terminology does this product's audience expect? (Consult **SaaSPO**)
- What typography hierarchy and color balance best conveys the brand tone? (Consult **Refero Styles**, **Minimal Gallery**)
- How should the primary value entry point be structured? (Consult **Supahero**, **CTA Gallery**)
- What navigation and wayfinding model fits the link count? (Consult **Navbar Gallery**)
- What feedback physics and transitions will clarify state changes? (Consult **60fps.design**)
- How should mobile screens reorganize the desktop information architecture? (Consult **Loadmo.re**)

### Step 2: Source Routing
Use the `references/source-registry.md` to select 2 to 3 targeted sources.
- **Do not** consult generic Dribbble/Pinterest art boards for technical SaaS tools.
- **Do not** consult enterprise directories when designing an expressive consumer product.

### Step 3: Intelligence Extraction (What to Look For)
When inspecting research references, extract:
1. **Mathematical Ratios**: Exact type scale steps, line-height proportions, container widths, padding units.
2. **Semantic Mappings**: How colors are assigned to functional roles (what color is the canvas? What color indicates an active state?).
3. **Negative Space Architecture**: Where does the page breathe? How do margins separate major narrative chapters?
4. **Content Scaffolding**: How are technical terms, metrics, code snippets, and customer proofs framed?

### Step 4: Cross-Domain Synthesis
Combine insights from disparate sources into a cohesive whole:
- Take **layout architecture** from a top developer tool in SaaSPO.
- Take **typographic restraint and whitespace** from Minimal Gallery.
- Take **micro-interaction feedback timing** from 60fps.design.
- Ground them in a unified token system inside `DESIGN.md`.

---

## 3. What Remains Intentionally Unimplemented in this Phase

To maintain architectural purity and prevent premature complexity:
- Automated web scrapers and headless browser loops are **not** implemented.
- Vector database embeddings of website screenshots are **not** implemented.
- Autonomous visual scrapers are **not** implemented.

The current system provides the **methodological intelligence** that guides the agent's analytical thinking during pair programming.
