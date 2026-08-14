# Sloppi Standardized Research Output Specification

This document defines the standardized markdown output that a Sloppi-enabled agent must generate upon completing the research and synthesis phase.

This document serves as the evidentiary foundation that directly informs the creation of the project's `DESIGN.md` contract.

---

## Standardized Research Document Template

```markdown
# Design Research & Synthesis: [Product Name]

> **Sloppi Design Intelligence Research Log**  
> *Target Project*: [Product Name]  
> *Research Depth*: [Lightweight | Standard | Deep]  
> *Date*: [Timestamp / Date]

---

## 1. Product Context & Constraints
- **Product Category**: [e.g., Developer Infrastructure, Fintech, Consumer Mobile]
- **Target Audience & Mental Model**: [e.g., Senior Systems Engineers living in Linux terminals]
- **Operational Stakes**: [Low / Medium / High & Mission-Critical]
- **Primary User Goal**: [The single most critical job the user arrives to do]
- **Primary Conversion Action**: [e.g., Run `npm i @sloppi/core`, Upgrade to Tier 2]
- **Information Density Requirement**: [Compact (4px base) | Comfortable (8px base) | Spacious (Editorial)]
- **Platform Scope**: [Desktop-first | Mobile-first | Universal Responsive]

---

## 2. Formulated Research Questions
1. **[Question Domain 1]**: [Explicit high-intent research question]
2. **[Question Domain 2]**: [Explicit high-intent research question]
3. **[Question Domain 3]**: [Explicit high-intent research question]

---

## 3. Sources Consulted
- **Primary Sources**:
  - `[Source Name 1]` (`[URL]`): [Reason for consultation]
  - `[Source Name 2]` (`[URL]`): [Reason for consultation]
- **Secondary Sources**:
  - `[Source Name 3]` (`[URL]`): [Reason for consultation]

---

## 4. Selected Reference Constellation

| Reference Name | URL | Selected For (Domain) | Specific Question Answered |
| :--- | :--- | :--- | :--- |
| **Reference A** | `[URL]` | *Composition & Layout* | [Question 1] |
| **Reference B** | `[URL]` | *Typography & Scale* | [Question 2] |
| **Reference C** | `[URL]` | *Navigation & Density* | [Question 3] |

---

## 5. Reference Structural Analysis

### Reference A: [Name] (`[URL]`)
- **Composition & Space**: [Structural layout findings]
- **Typographic Scale**: [Scale steps, line-height proportions]
- **Color Taxonomy**: [Canvas ground, text hierarchy, accent roles]
- **Geometry & Elevation**: [Radii scale, border width, shadow depth]
- **Interaction & Motion**: [Transition timings, micro-feedback]
- **Transferable Principles**:
  - *Principle 1*: [Extracted reusable rule]
  - *Principle 2*: [Extracted reusable rule]
- **Non-Transferable Details**:
  - *Detail 1*: [Brand-specific color, logo, or proprietary illustration to discard]

*(Repeat decomposition for Reference B, Reference C, etc.)*

---

## 6. Cross-Reference Synthesis & Convention Analysis

### A. Common Industry Conventions (Retained)
- *Convention 1*: [Universal pattern that solves a verified usability friction]
- *Convention 2*: [Universal pattern that solves a verified usability friction]

### B. Detected Defaults & Anti-Patterns (Rejected)
- *Rejected Default 1*: [Common industry cliché rejected for this project + Rationale]
- *Rejected Default 2*: [Common industry cliché rejected for this project + Rationale]

### C. Uncovered Design Opportunities
- *Opportunity 1*: [Novel layout, interactive demo, or narrative technique]
- *Opportunity 2*: [Unconventional typographic or spatial approach]

### D. Non-Negotiable Design Constraints
- *Constraint 1*: [e.g., Strict WCAG AAA compliance, zero horizontal overflow at 360px]
- *Constraint 2*: [e.g., 100vh locked dashboard viewport on desktop]

### E. Controlled Visual Tensions
- **[Tension Pair, e.g., Technical + Warm]**: [How this contrast manifests in layout, typography, and color]

---

## 7. The Design Thesis

> **[Insert 2-4 sentence definitive design thesis answering: What should it feel like? Why? What visual principles create it? What defaults are rejected?]**

---

## 8. Open Design Questions & User Decisions
- [ ] [Open question or trade-off requiring user feedback or approval]
- [ ] [Open question or trade-off requiring user feedback or approval]
```

---

## Transition to the Design System Phase

Once this research document is finalized:
1. The **Design Thesis** becomes Section 1 of `DESIGN.md`.
2. The **Extracted Principles & Visual Tensions** dictate token definitions (modular scale, color taxonomy, corner radii).
3. The **Design Constraints & Rejected Defaults** populate the explicit Do's and Don'ts in `DESIGN.md`.
