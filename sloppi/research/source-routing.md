# Sloppi Source Routing & Prioritization Matrix

Source routing is the mechanism by which a coding agent maps specific design questions to the most authoritative primary and secondary design galleries.

Agents must not browse sources randomly. They must route questions based on functional domains and prioritize sources according to their relevance to the immediate task.

---

## 1. Domain Routing Matrix

| Design Question Domain | Primary Sources | Secondary Sources | Tertiary Sources | What to Extract |
| :--- | :--- | :--- | :--- | :--- |
| **Product / Industry Taxonomy** | **SaaSPO**<br>`saaspo.com` | **Recent.design**<br>`recent.design` | **Minimal Gallery**<br>`minimal.gallery` | Industry information architecture, category credibility expectations, realistic feature framing. |
| **General Visual Composition & Space** | **Minimal Gallery**<br>`minimal.gallery` | **Recent.design**<br>`recent.design` | **Inspora**<br>`inspora.design` | Negative space ratios, asymmetric grid tension, layout restraint, breaking card-in-card clutter. |
| **Design System & AI Context** | **Refero Styles**<br>`styles.refero.design` | **SaaSPO**<br>`saaspo.com` | *Internal project tokens* | Machine-readable token models, exact modular scales, semantic color roles, explicit Do/Don't rules. |
| **Typography & Scale Hierarchy** | **Minimal Gallery**<br>`minimal.gallery`<br>**Deck.Gallery**<br>`deck.gallery` | **Refero Styles**<br>`styles.refero.design` | **Recent.design**<br>`recent.design` | Font pairing contrast, line-height proportions (crushed display vs. open body), optical letter-spacing. |
| **Hero Sections & First Entry Points** | **Supahero**<br>`supahero.io` | **SaaSPO**<br>`saaspo.com`<br>**Minimal Gallery**<br>`minimal.gallery` | **Recent.design**<br>`recent.design` | Top-of-fold visual weight balance, interactive demo vs. editorial headline vs. code terminal. |
| **Navigation & Header Architecture** | **Navbar Gallery**<br>`navbar.gallery` | **SaaSPO**<br>`saaspo.com` | **Minimal Gallery**<br>`minimal.gallery` | Link density scaling (floating island vs. mega-menu), wayfinding hierarchy, mobile hamburger vs. tab bar. |
| **CTA, Conversion & Action Hierarchy** | **CTA Gallery**<br>`cta.gallery` | **SaaSPO**<br>`saaspo.com` | **Deck.Gallery**<br>`deck.gallery` | Visual weight contrast (primary vs. secondary), outcome-explicit micro-copy, inline assurance proof. |
| **Interaction, Motion & State Physics** | **60fps.design**<br>`60fps.design` | *Relevant production web apps* | **Inspora**<br>`inspora.design` | State transition triggers, duration scales (100–300ms), spatial continuity cues, feedback timing. |
| **Mobile-First & Touch Ergonomics** | **Loadmo.re**<br>`loadmo.re` | *Relevant production mobile web* | **Minimal Gallery**<br>`minimal.gallery` | Thumb-zone reachability, responsive refactoring (multi-column tables → vertical narrative/sheets), touch hit areas. |
| **Brand Identity, Motifs & Geometry** | **LogoInspo**<br>`logoinspo.com`<br>**Deck.Gallery**<br>`deck.gallery` | **Posts.design**<br>`posts.design` | **Refero Styles**<br>`styles.refero.design` | Geometric motifs, corner radius derivation, logo typography relationships, graphic symbols. |
| **Social, Campaign & Marketing Expression** | **Posts.design**<br>`posts.design` | **Inspora**<br>`inspora.design` | **OGfolio**<br>`ogfolio.com` | Multi-surface brand consistency, social graphic framing, changelog and announcement cards. |
| **Page Closures & Footers** | **Footer.design**<br>`footer.design` | **SaaSPO**<br>`saaspo.com` | **Minimal Gallery**<br>`minimal.gallery` | Secondary sitemap density, brand signature closure, legal/utility disclosures without clutter. |
| **OG Images & Link Previews** | **OGfolio**<br>`ogfolio.com` | **Posts.design**<br>`posts.design` | **Deck.Gallery**<br>`deck.gallery` | 1200x630 social card layout, feed-stopping typography, visual continuity with the landing hero. |

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

### Scenario 3: An Expressive Consumer Mobile Application
- **Primary Sources**:
  - `Loadmo.re`: Extract mobile-native swipe navigation, bottom sheets, and thumb-zone ergonomics.
  - `60fps.design`: Extract spring-based physics, micro-interactions, and fluid list-reordering gestures.
- **Secondary Sources**:
  - `Refero Styles`: Extract soft, tactile geometry (pill buttons, organic card curvature, vibrant multi-accent palettes).
  - `Recent.design`: Inspect contemporary tactile textures and expressive typography.
  - `OGfolio`: Design high-impact, bold social share preview cards.
- **Excluded Sources**:
  - Enterprise directories with 5-column desktop comparison tables.
