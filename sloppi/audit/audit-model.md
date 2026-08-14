# Sloppi Design Audit Model

The Sloppi Design Audit Model is a 6-dimensional evaluation framework used by coding agents to critique and refine rendered interfaces before presenting them to users or shipping code.

During the audit phase, the agent acts as an uncompromising design reviewer, testing the interface against the project's persistent `DESIGN.md`.

---

## The 6 Audit Dimensions

```
                      [ Rendered Interface ]
                                 │
     ┌───────────────────────────┼───────────────────────────┐
     ▼                           ▼                           ▼
[ 1. Visual Hierarchy ]  [ 2. Anti-Slop Check ]    [ 3. Token Consistency ]
     │                           │                           │
     ▼                           ▼                           ▼
[ 4. Responsive UX ]     [ 5. Accessibility ]      [ 6. Distinctiveness ]
```

---

### Dimension 1: Visual Hierarchy & Composition
- **Primary Visual Anchor**: Is there an unmistakable first entry point for the user's eye, or are multiple elements competing with equal visual loudness?
- **Typographic Contrast**: Is the ratio between display headlines, section headings, and body copy sufficiently pronounced (e.g., clear scale steps rather than 16px vs 18px vs 20px ambiguity)?
- **Whitespace & Grouping**: Does negative space cleanly separate distinct narrative chapters, or is the page cluttered with unnecessary borders and card containers?
- **Optical Line Balancing**: Are display headlines optically balanced without single-word line wraps (orphans)?

### Dimension 2: Anti-Slop & Intentionality
- **Decorative Clutter Audit**: Are there arbitrary gradient blobs, meaningless floating badges, glassmorphism on flat backgrounds, or excessive rounded corners that serve no product purpose?
- **Repetitive Structure Audit**: Does the page suffer from card fatigue or monotonous 3-column feature grids?
- **Copywriting Authenticity**: Is the copy grounded in real technical verbs and believable domain data, or is it inflated with generic AI marketing buzzwords?
- **Consequence Verification**: Do all button labels and CTAs explicitly declare the immediate consequence of interaction?

### Dimension 3: Design System & Token Consistency
- **Token Compliance**: Are all colors, fonts, spacing units, and border-radii referencing established tokens from `DESIGN.md`, or are there arbitrary inline hardcoded hex values (e.g., `#3b82f6` or `padding: 23px`)?
- **Semantic Role Adherence**: Are colors used according to their assigned semantic role (e.g., brand color strictly for primary actions, muted text for metadata)?
- **Geometry Coherence**: Is the border-radius scale applied consistently across elements of the same hierarchy?

### Dimension 4: Responsive & Ergonomic Adaptation
- **Mobile Composition**: Is the mobile viewport composed as an ergonomic touch environment, or does it look like a shrunken desktop layout?
- **Touch Targets**: Are all interactive elements (buttons, links, tab items) at least 44x44px in clickable area?
- **Horizontal Overflow**: Is horizontal scrolling strictly prevented across all standard breakpoints (360px, 768px, 1024px, 1440px)?
- **Thumb-Zone Navigation**: Are primary mobile navigation triggers placed within comfortable one-handed reach?

### Dimension 5: Accessibility & Contrast
- **WCAG Contrast**: Does text meet WCAG AA standards (minimum 4.5:1 for body copy, 3:1 for large display text and UI components)?
- **Keyboard Navigation**: Are visible, high-contrast `:focus-visible` rings present on all interactive controls?
- **Semantic Landmarks**: Does the DOM use proper HTML5 semantic landmarks (`<header>`, `<main>`, `<nav>`, `<section>`, `<footer>`) with a single `<h1>` per page?
- **Motion Reduction**: Does the CSS include `@media (prefers-reduced-motion: reduce)` fallbacks that disable heavy animations?

### Dimension 6: Distinctiveness & Brand Thesis Alignment
- **Thesis Adherence**: Does the final rendered interface embody the exact visual point of view formulated in `DESIGN.md`?
- **Visual Identity Signature**: Does the product possess an unmistakable aesthetic identity, or could it be easily mistaken for a generic template?
- **Emotional Calibration**: Does the density, color mood, and typographic weight match the operational stakes of the product (e.g., serious and robust for finance vs. energetic and fluid for creative tools)?

---

## Audit Output Protocol

When an agent completes an audit, it must generate a structured critique log before proceeding to refinement:

```markdown
### Sloppi Visual Audit Log
- **Pass / Fail Status**: [PASS | NEEDS REFINEMENT]
- **Identified Deficiencies**:
  1. [Dimension]: [Specific element and observed issue] → [Recommended fix based on DESIGN.md]
  2. [Dimension]: [Specific element and observed issue] → [Recommended fix based on DESIGN.md]
- **Refinement Actions**:
  - [Action 1]
  - [Action 2]
```
