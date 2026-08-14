# Sloppi Design Research Source Registry

This registry serves as the canonical map of the design-reference ecosystem for Sloppi-enabled coding agents. It defines why each source exists, which design domain it serves, its operational priority tier, when an agent must consult it, when an agent must avoid it, and what specific design intelligence must be extracted.

---

## Source Classification & Priority Framework

Sloppi categorizes sources into three operational tiers:
- **Primary Sources**: Essential, high-conviction archives providing direct structural, mathematical, or category-specific solutions.
- **Secondary Sources**: Specialized or component-focused archives providing adjacent architectural and ergonomic context.
- **Tertiary Sources**: Broad visual discovery feeds used strictly for exploratory mood synthesis and creative tension.

---

## 1. Design Systems, Machine-Readable Tokens & Rules

### Refero Styles
- **URL**: `https://styles.refero.design/`
- **Design Domain**: AI-Readable Design Systems, Design Tokens, Semantic Roles, Component Rules
- **Classification**: **Primary Research Source**
- **Primary Purpose**: Provides curated, production design systems decomposed into structured `DESIGN.md` specifications with exact numerical tokens, semantic color taxonomies, mathematical typography scales, line-height proportions, and explicit Do/Don't guardrails.
- **When Sloppi Should Use It**:
  - When establishing a new project's design foundation and drafting the initial `DESIGN.md`.
  - When looking for real-world mathematical ratios in typography (e.g., compressed display leading vs. open body leading).
  - When defining semantic token roles (distinguishing Brand, Accent, and Neutral functions with explicit rationale).
  - When establishing concrete component geometry rules (border-radius scales mapped to component hierarchy).
- **When Sloppi Should NOT Use It**:
  - When the project already has an established design system and token dictionary.
  - To blindly copy-paste tokens without adapting them to the specific client/product brand thesis.
  - For complex interactive motion physics or dynamic application state machines.
- **Information to Extract**:
  - `DESIGN.md` structure and semantic hierarchy.
  - Semantic color taxonomy (Brand, Accent, Neutrals, Canvas, Surface, Border) with functional descriptions.
  - Exact typography stacks, line-height proportions, and letter-spacing compensations.
  - Layout density tokens (section gaps, card paddings, element gaps, container bounds).
  - Component geometry rules and explicit Do/Don't guardrails.

---

## 2. Product & Industry Categorization

### SaaSPO
- **URL**: `https://saaspo.com/`
- **Design Domain**: Industry-Specific UX, Page Types, Product-Category Visual Conventions
- **Classification**: **Primary Research Source**
- **Primary Purpose**: Indexes live software products categorized by industry (Developer Tools, AI, Crypto/Web3, Finance, Healthcare, Design, CRM, Enterprise) and by page type (Landing, Pricing, Product Features, Integrations, About, Customers).
- **When Sloppi Should Use It**:
  - During the `Understand` and `Research` phases to inspect how real products in the target industry solve specific information architecture and communication challenges.
  - When designing high-intent page types (e.g., multi-tier pricing tables, API documentation hubs, compliance-heavy enterprise pages).
  - When determining category conventions to either adopt deliberately or intentionally subvert.
- **When Sloppi Should NOT Use It**:
  - As a generic visual theme picker.
  - To replicate the median "generic AI startup" or "generic SaaS" look.
  - For consumer-native apps, editorial publications, or artistic experimental interfaces.
- **Information to Extract**:
  - Information architecture patterns specific to the industry (e.g., code snippets + latency metrics in Developer Tools vs. security proofs + tier breakdown in Fintech).
  - Industry-specific feature presentation techniques.
  - Realistic pricing grid architectures and feature comparison taxonomies.
  - Proof and credibility structures expected by the target audience.

---

## 3. Visual Composition, Whitespace & Editorial Restraint

### Minimal Gallery
- **URL**: `https://minimal.gallery/`
- **Design Domain**: Composition, Whitespace Architecture, Editorial Typography, Visual Hierarchy
- **Classification**: **Primary Research Source**
- **Primary Purpose**: Curates interfaces governed by restraint, high-contrast typography, disciplined grid layouts, asymmetric spatial tension, and purposeful reduction of visual noise.
- **When Sloppi Should Use It**:
  - When designing products that require high clarity, calm utility, luxury positioning, or editorial authority.
  - When an interface feels overcrowded, muddy, or burdened by decorative containers (cards inside cards).
  - When studying how typography and negative space alone can establish strong visual hierarchy without decorative crutches (gradients, drop shadows, borders).
- **When Sloppi Should NOT Use It**:
  - When the target product is high-density data analytics, playful consumer entertainment, or requires rich multi-layered graphic expression.
  - As a mandate to make everything stark monochrome or brutally empty.
- **Information to Extract**:
  - Negative space ratios (macro whitespace between narrative blocks vs. micro whitespace within components).
  - Asymmetric grid layouts that break repetitive columnar monotony.
  - Typographic scale contrast (pairing oversized display headings with disciplined body text).
  - Subtraction principles: removing borders, cards, and backgrounds when whitespace can define grouping.

---

## 4. Interaction, State Transitions & Motion Dynamics

### 60fps.design
- **URL**: `https://60fps.design/`
- **Design Domain**: UI/UX Animation, Micro-interactions, Motion Hierarchy, State Transitions
- **Classification**: **Primary Research Source**
- **Primary Purpose**: Catalogs real production micro-interactions, state transitions, spatial continuity cues, and feedback physics across top-tier iOS and web applications.
- **When Sloppi Should Use It**:
  - When planning transitions between complex UI states (e.g., modal expansions, list-to-detail views, filtering transitions, drag-and-drop mechanics).
  - When defining timing curves, durations, and easing functions in `DESIGN.md`.
  - When engineering micro-interactions (button active states, loading indicators, toggle shifts, navigation drawer unfolds).
- **When Sloppi Should NOT Use It**:
  - When adding motion merely for theatrical display or decorative novelty.
  - When motion degrades performance, triggers layout reflows, or violates `prefers-reduced-motion`.
  - When designing static documents or low-interaction informational pages.
- **Information to Extract**:
  - Purposeful motion triggers: causality (what caused the movement), hierarchy (what enters first), and confirmation (did the action succeed).
  - Duration standards (micro-interactions: 100–200ms; structural transitions: 250–350ms; complex scene choreography: 400–600ms).
  - Physics parameters (spring stiffness, damping ratios, cubic-bezier timing values).
  - Spatial continuity (shared layout IDs, morphing geometry, preserving user context across view changes).

---

## 5. Mobile-First & Touch Ergonomics

### Loadmo.re
- **URL**: `https://loadmo.re/`
- **Design Domain**: Mobile Interface Design, Mobile Visual Hierarchy, Touch Interactions
- **Classification**: **Primary Research Source**
- **Primary Purpose**: Dedicated gallery focused exclusively on mobile web interfaces and alternative mobile-native UX patterns.
- **When Sloppi Should Use It**:
  - When designing responsive layouts to ensure mobile is treated as a dedicated ergonomic environment rather than a shrunken desktop viewport.
  - When designing touch-friendly navigation patterns (bottom sheets, thumb-zone controls, horizontal swipe rails, swipe gestures).
  - When refactoring complex multi-column desktop tables/grids into mobile-native narrative blocks.
- **When Sloppi Should NOT Use It**:
  - When optimizing strictly desktop-only software interfaces.
  - When desktop spatial density is the primary design requirement.
- **Information to Extract**:
  - Thumb-zone ergonomic reachability maps.
  - Progressive disclosure for narrow screens.
  - Mobile typography scale compression and touch target geometries (minimum 44x44px hit areas).
  - Mobile-native section pacing and scroll rhythm.

---

## 6. Component-Specific Deep Dives

### Supahero
- **URL**: `https://supahero.io/`
- **Design Domain**: Hero Section Architecture, Visual Entry Points, Headline Hierarchy, Primary CTAs
- **Classification**: **Primary Research Source** (Hero sections)
- **Primary Purpose**: Curated repository of top-of-fold landing page hero sections analyzing headline structure, product framing, and first-impression conversion dynamics.
- **When Sloppi Should Use It**:
  - When structuring the primary visual entry point of a landing or product page.
  - When deciding whether a hero requires an interactive demo, live terminal simulator, video preview, product canvas, or high-impact editorial typography.
- **When Sloppi Should NOT Use It**:
  - To pick a generic "centered H1 + two pill buttons + tilted dashboard screenshot" template.
  - When the hero requirements call for an unconventional narrative start.
- **Information to Extract**:
  - Above-the-fold visual weight balance (headline vs. product demonstration vs. social proof).
  - Headline character counts and optical line-length balancing (`text-wrap: balance`).
  - Contextual CTA placement and supporting assurance copy.

### Navbar Gallery
- **URL**: `https://navbar.gallery/`
- **Design Domain**: Navigation Architecture, Header Systems, Wayfinding UX
- **Classification**: **Primary Research Source** (Navigation)
- **Primary Purpose**: Comprehensive categorization of navigation patterns (floating pills, sticky bars, full-screen overlays, flyouts, mega menus, sidebar docks, command palette hybrids).
- **When Sloppi Should Use It**:
  - When deciding the information architecture model for a site or web app.
  - When selecting navigation style based on link density (e.g., minimalist floating island for 3–4 links vs. persistent full-bleed header with mega menu for 30+ links).
  - When handling responsive navigation transitions (desktop bar → mobile bottom sheet/fullscreen drawer).
- **When Sloppi Should NOT Use It**:
  - When designing single-screen utility views or distraction-free workflows (checkout, onboarding modal).
  - To apply a trendy floating pill navbar to an enterprise tool with 20 deep subpages.
- **Information to Extract**:
  - Navigation patterns mapped to link count and hierarchy.
  - Scroll-linked behaviors (auto-hide on scroll down, reveal on scroll up, blur on scroll).
  - Mobile hamburger vs. bottom tab bar tradeoffs.

### CTA Gallery
- **URL**: `https://cta.gallery/`
- **Design Domain**: Conversion Patterns, Action Hierarchy, Button UX & Copywriting
- **Classification**: **Primary Research Source** (Conversion blocks)
- **Primary Purpose**: Specialized library of call-to-action sections, button hierarchies, form embeds, and conversion triggers.
- **When Sloppi Should Use It**:
  - When designing high-stakes conversion points (sign-up blocks, trial triggers, purchase flows).
  - When defining the visual weight difference between Primary, Secondary, and Tertiary actions.
  - When writing high-intent action copy that clearly articulates what happens next.
- **When Sloppi Should NOT Use It**:
  - For decorative button styling without clear user intent.
  - To insert excessive, aggressive CTAs that spam the user across every single viewport.
- **Information to Extract**:
  - Visual hierarchy contrast ratios between primary and auxiliary actions.
  - High-converting micro-copy formulas (value-driven vs. generic "Submit").
  - Inline assurance elements (zero credit card required, instant setup, SOC2 compliance).

### Footer.design
- **URL**: `https://footer.design/`
- **Design Domain**: Page Closures, Secondary Information Architecture, Legal & Global Links
- **Classification**: **Primary Research Source** (Page closures)
- **Primary Purpose**: Dedicated gallery analyzing footer structures, comprehensive sitemaps, brand closure statements, newsletter capture blocks, and secondary navigation.
- **When Sloppi Should Use It**:
  - When closing a page experience with appropriate weight and brand identity.
  - When organizing secondary links, legal disclosures, status widgets, and social links.
  - When choosing between a dense multi-column directory footer and a minimalist single-line signature footer.
- **When Sloppi Should NOT Use It**:
  - When building locked web app viewports (dashboards, canvases, code editors) where footers do not belong.
- **Information to Extract**:
  - Link grouping and multi-column visual hierarchy.
  - Brand closure signatures (large stylized wordmark, mission statement, copyright stamp).
  - Utility integrations (theme toggle, language switcher, newsletter input).

---

## 7. Narrative, Brand Identity & Geometry

### Deck.Gallery
- **URL**: `https://deck.gallery/`
- **Design Domain**: Presentation Design, Visual Storytelling, Narrative Pacing, Slide Systems
- **Classification**: **Primary Research Source** (Storytelling & Pacing)
- **Primary Purpose**: Curates pitch decks, product launches, keynote presentations, and editorial slide decks showcasing sequential narrative architecture.
- **When Sloppi Should Use It**:
  - When designing a long-form landing page or product walkthrough that requires dramatic sequential storytelling.
  - When establishing visual pacing across sections (alternating high-density proof with breathing pauses).
  - When designing slide-based presentations, investor materials, or interactive story widgets.
- **When Sloppi Should NOT Use It**:
  - For dense transactional interfaces or everyday administrative CRUD tables.
- **Information to Extract**:
  - Visual narrative arcs (Problem → Insight → Solution → Proof → Vision → Action).
  - Slide typography rules: one dominant idea per frame with strong typographic scale.
  - Clean data visualization and diagrammatic storytelling.

### LogoInspo
- **URL**: `https://logoinspo.com/`
- **Design Domain**: Logo Systems, Geometric Motifs, Brand Identity, Visual Geometry
- **Classification**: **Primary Research Source** (Geometry derivation)
- **Primary Purpose**: Analyzes logo construction, geometric marks, monogram systems, and wordmark typography relationships.
- **When Sloppi Should Use It**:
  - When deriving a product's interface geometry from its brand identity (e.g., echoing sharp triangular logo geometry in container angles or pill brand marks in rounded corners).
  - When selecting typography pairings that complement the logo's typographic personality.
  - When creating favicon, wordmark, and brand emblem specifications for `DESIGN.md`.
- **When Sloppi Should NOT Use It**:
  - To generate arbitrary complex vector illustrations that do not scale down to UI elements.
- **Information to Extract**:
  - Geometric rules and angle relationships.
  - Typographic character details (geometric sans vs. humanistic serif vs. technical monospace).
  - Visual motifs that can be translated into subtle UI accents, icons, and dividers.

---

## 8. Contemporary Discovery & External Surfaces

### Recent.design
- **URL**: `https://recent.design/`
- **Design Domain**: Contemporary Visual Language, Fresh Layout Patterns, Emerging Aesthetics
- **Classification**: **Secondary Research Source**
- **Primary Purpose**: Real-time discovery feed of contemporary visual design, graphic composition, branding systems, and new interface aesthetics across current digital releases.
- **When Sloppi Should Use It**:
  - To ensure Sloppi's design knowledge is aware of current aesthetic movements (e.g., modern brutalism, tactile physical skeuomorphism 2.0, editorial retro-futurism, fluid kinetic typography).
  - To benchmark a design against contemporary production standards rather than older defaults.
- **When Sloppi Should NOT Use It**:
  - As a reason to chase fleeting micro-trends that do not serve the product thesis.
  - When evergreen clarity and utility must override stylistic experimentation.
- **Information to Extract**:
  - Contemporary treatment of borders, glass surfaces, ambient lighting, and grain textures.
  - Modern layout compositions (overlapping layers, broken grids, non-standard section dividers).
  - Distinction between ephemeral visual fads and durable contemporary design paradigms.

### Posts.design
- **URL**: `https://posts.design/`
- **Design Domain**: Social Media Visual Identity, Campaign Graphics, Brand Consistency
- **Classification**: **Secondary Research Source**
- **Primary Purpose**: Curates brand expression across social media posts, feature announcement cards, and marketing campaign graphics.
- **When Sloppi Should Use It**:
  - When ensuring the visual design language built for the website translates coherently into marketing assets and social graphics.
  - When designing social share previews, in-app announcement banners, or changelog cards.
- **When Sloppi Should NOT Use It**:
  - For core application layouts or dense UI component patterns.
- **Information to Extract**:
  - Framing techniques for product highlights within fixed square/portrait aspect ratios.
  - Consistent brand color and typography application on promotional canvases.

### OGfolio
- **URL**: `https://ogfolio.com/`
- **Design Domain**: Open Graph (OG) Images, Link Preview Identity, Metadata Cards
- **Classification**: **Secondary Research Source**
- **Primary Purpose**: Specialized collection of Open Graph social preview cards (1200x630px) designed for link sharing on X, LinkedIn, Slack, and Discord.
- **When Sloppi Should Use It**:
  - When generating `og:image` and `twitter:image` assets for a web application.
  - To ensure that when a user shares the URL, the link preview immediately conveys the distinct visual identity, value proposition, and typography of the product.
- **When Sloppi Should NOT Use It**:
  - For inside-the-app UI layouts.
- **Information to Extract**:
  - 1200x630 layout grids and safe-zone margins.
  - Value proposition headline framing within social feeds.
  - Visual continuity between the OG preview card and the actual landing page hero.

### Inspora
- **URL**: `https://inspora.design/`
- **Design Domain**: Broad Creative Discovery, Visual Mood, Multidisciplinary Graphic Design
- **Classification**: **Tertiary Inspiration Source**
- **Primary Purpose**: Cross-disciplinary visual archive spanning graphic design, branding, kinetic art, and experimental digital interfaces.
- **When Sloppi Should Use It**:
  - During early moodboard synthesis when exploring unconventional art direction or distinct brand personality.
  - When a product needs a strong artistic hook or brand metaphor that traditional SaaS directories cannot provide.
- **When Sloppi Should NOT Use It**:
  - For standard UI component architecture or semantic token definitions.
  - For accessible enterprise UX workflows.
- **Information to Extract**:
  - Visual motifs, unexpected color harmony combinations, tactile textures, and expressive layout concepts.

---

## Summary Matrix: Research Routing by Task Type

| Design Task | Primary Sources | Secondary Sources | Tertiary Sources |
| :--- | :--- | :--- | :--- |
| **New Project Foundation & `DESIGN.md`** | Refero Styles, SaaSPO | Minimal Gallery, LogoInspo | Inspora |
| **Industry Information Architecture** | SaaSPO | Supahero, Footer.design | Recent.design |
| **Editorial & Restrained Layouts** | Minimal Gallery, Deck.Gallery | Recent.design | Inspora |
| **Motion, Transitions & States** | 60fps.design | *Production Web Apps* | Inspora |
| **Mobile-Native UX & Ergonomics** | Loadmo.re | Minimal Gallery | Recent.design |
| **Hero Sections & First Entry Points** | Supahero, SaaSPO | Minimal Gallery, Refero Styles | Recent.design |
| **Navigation & Wayfinding Systems** | Navbar Gallery | SaaSPO, Refero Styles | Minimal Gallery |
| **Conversion Blocks & Call-to-Actions** | CTA Gallery | SaaSPO, Deck.Gallery | Recent.design |
| **Footers & Page Closures** | Footer.design | SaaSPO, Minimal Gallery | Posts.design |
| **Narrative Flow & Pitch Storytelling** | Deck.Gallery | Minimal Gallery | Recent.design |
| **Brand Motifs, Geometry & Radii** | LogoInspo, Refero Styles | Deck.Gallery, Posts.design | Inspora |
| **Social Previews & Meta Cards** | OGfolio, Posts.design | Deck.Gallery | Inspora |
