# Sloppi Reference Selection & Constellation Model

Reference selection is the disciplined process by which an agent curates a diverse set of external benchmarks to answer its formulated research questions.

Sloppi explicitly rejects the single-reference fallacy:

> ❌ **The Single-Reference Fallacy**: "We found this one stunning website; let's base our entire design on it."  
> *Result*: Counterfeit imitation, copied brand artifacts, and visual mismatch with the actual product's constraints.

---

## 1. The Reference Constellation Architecture

Instead of cloning a single site or creating a moodboard of identical visual clones, Sloppi requires the creation of a **Reference Constellation**.

In a Reference Constellation, **every selected reference is chosen for a distinctly different structural or functional reason**:

```
                 [ Target Product Design Thesis ]
                               │
       ┌───────────────┬───────┴───────┬───────────────┐
       ▼               ▼               ▼               ▼
[ Reference A ] [ Reference B ] [ Reference C ] [ Reference D ]
   For: Page       For: Type       For: Header      For: State
  Composition     Scale Ratio      Wayfinding       Transitions
   & Whitespace    & Contrast       Density           & Motion
```

### Constellation Blueprint Example (Developer Cloud Monitor)
- **Reference A (e.g., Linear / Raycast)**: Selected for **density and monospaced tabular data alignment**.
- **Reference B (e.g., Stripe Documentation)**: Selected for **navigation information architecture across deep subpages**.
- **Reference C (e.g., Steep Analytics)**: Selected for **warm neutral background tones and editorial typography contrast**.
- **Reference D (e.g., Vercel CLI)**: Selected for **instantaneous terminal streaming micro-interactions**.

By combining these disparate references, the agent creates a novel, highly tailored visual synthesis rather than an imitation.

---

## 2. The 7 Reference Quality Criteria

Before adding any reference to the project's research log, the agent must validate it against all seven quality filters:

### 1. Relevance
- Does this reference solve the **exact informational, ergonomic, or conversion challenge** facing our product?
- *Anti-Pattern*: Selecting an avant-garde 3D fashion portfolio as a reference for a PostgreSQL query analyzer.

### 2. Distinctiveness
- Does the reference demonstrate a **deliberate, high-conviction visual decision** (e.g., intentional crushed leading, asymmetric layout rhythm, bold monochrome contrast)?
- *Anti-Pattern*: Selecting a generic, indistinguishable SaaS template that looks like 1,000 other landing pages.

### 3. Quality & Craft
- Is the interface genuinely well-crafted (rigorous typographic scale, crisp 1px borders, flawless contrast, fluid responsiveness), or is it merely superficially flashy with heavy 3D renders?
- *Anti-Pattern*: Mistaking slow, laggy 3D animations for design excellence.

### 4. Transferability
- Can the **underlying mathematical or structural principle** be extracted and adapted to a completely different visual theme, or is the appeal tied strictly to proprietary custom 3D art?
- *Anti-Pattern*: Selecting a site whose only strength is a custom $50,000 WebGL animation that cannot be transferred to a standard web app.

### 5. Specificity
- Does the reference provide specific, measurable insights (e.g., exact 48px section padding, 1.05 display line-height, 44px pill buttons), or only a vague "vibe"?

### 6. Diversity
- Does this reference introduce a **new perspective or orthogonal axis**, or does it repeat the aesthetic of an already-selected reference?
- *Rule*: Never select two references from the exact same aesthetic sub-genre (e.g., do not select three dark-mode AI startups with purple neon glow).

### 7. Contemporary Relevance
- Is the reference grounded in modern web design standards (accessible contrast, modern typography, crisp vector geometry, touch-first layouts), or does it carry obsolete 2017-era visual tropes (heavy muddy drop shadows, skeuomorphic gloss, static non-responsive tables)?

---

## 3. Reference Selection Protocol

1. **Determine Required Constellation Size**:
   - *Lightweight Pass*: 1 targeted reference.
   - *Standard Pass*: 2 to 3 diverse references.
   - *Deep Pass*: 4 to 5 multi-domain references.
2. **Assign Explicit Roles**:
   - For every candidate URL, the agent must document: `Selected For: [Specific Design Dimension]`.
3. **Reject Clones**:
   - If two candidates share the same typography, layout structure, and color scheme, discard the weaker one.
4. **Log in Research Output**:
   - Record the URL, domain, reason selected, and the specific question it answers in the project research log.
