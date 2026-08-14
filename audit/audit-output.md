# Sloppi Standardized Audit Report Schema

The Audit Report is the structured deliverable produced by the Visual QA & Anti-Slop Audit Engine. It records category-level pass/fail statuses and itemized findings before feeding the refinement loop.

Sloppi **strictly rejects single reductionist scores** (*"Design Score: 82/100"*). A single number conceals critical blockers and provides zero actionable architectural direction. Instead, Sloppi delivers multi-category status assessments and granular, evidence-based findings.

---

## 1. Category-Level Status Dashboard

```markdown
### Sloppi Visual & Anti-Slop Audit Dashboard

| Audit Dimension | Status | Primary Observation |
| :--- | :--- | :--- |
| **1. Functionality & Integrity** | **PASS** | All interactive tabs and forms mount cleanly without console errors. |
| **2. Accessibility (WCAG AA/AAA)**| **PASS** | 2px focus rings verified; contrast ratios exceed 4.5:1 on all text. |
| **3. Visual & Info Hierarchy** | **NEEDS WORK** | Competing action buttons in hero; secondary card headings too loud. |
| **4. Composition & Cadence** | **NEEDS WORK** | 3 consecutive sections use identical 3-column card symmetry. |
| **5. Typography & Measure** | **PASS** | Mathematical type scale verified; body copy constrained to 65ch. |
| **6. Spatial Baseline & Tokens** | **PASS** | All padding and margins map to 4px/8px baseline scale tokens. |
| **7. Color Taxonomy & Roles** | **PASS** | Semantic color roles adhered to; zero unmapped hex codes in CSS. |
| **8. Responsive & Ergonomics** | **PASS** | Zero horizontal overflow on 390px mobile; touch targets >= 44px. |
| **9. Interaction & Motion** | **PASS** | Micro-interactions at 120ms; prefers-reduced-motion respected. |
| **10. Content & Truthfulness** | **PASS** | Real benchmark parameters; zero fake testimonials or stock avatars. |
| **11. Systemic Consistency** | **PASS** | Single Lucide icon family with uniform 1.5px optical stroke. |
| **12. Distinctiveness & Anti-Slop**| **NEEDS WORK** | Features section uses generic card reflex instead of an architecture diff. |
```

---

## 2. Granular Audit Finding Format

Every identified issue must follow this exact 9-field schema:

```markdown
#### Finding: [ID] — [Short Descriptive Title]
- **Category**: [Hierarchy | Composition | Typography | Spacing | Color | Responsive | Interaction | Accessibility | Content | Consistency | Distinctiveness | Anti-Slop]
- **Severity**: [BLOCKER | HIGH | MEDIUM | LOW]
- **Location**: [Component file, section name, or DOM selector]
- **Observation**: [Exact description of what is physically rendered in the viewport]
- **Why It Matters**: [Concrete impact on user cognition, conversion, accessibility, or design authority]
- **Design Principle Affected**: [Specific principle from principles.md, anti-slop.md, or DESIGN.md]
- **Recommended Direction**: [Actionable structural, typographic, or layout guidance]
- **Confidence**: [High | Medium | Low]
```

### Example Canonical Finding

```markdown
#### Finding: AS-004 — Universal Card Reflex in Feature Section
- **Category**: Anti-Slop
- **Severity**: High
- **Location**: `src/sections/FeatureSection.tsx` (Middle viewport)
- **Observation**: Three visually identical rectangular cards with generic rounded corners and lightbulb icons present three completely heterogeneous technical capabilities (Concurrency Engine, NVMe Persistence, and Redis Protocol Compatibility).
- **Why It Matters**: Stacking identical cards creates a generic, interchangeable AI SaaS pattern and obscures the fundamental architectural differences between storage persistence and network protocols.
- **Design Principle Affected**: Content-to-Component Mapping (Principle 24) & Anti-Slop Catalog (Pattern 12).
- **Recommended Direction**: Refactor the section into an asymmetric layout: 1 dominant interactive terminal showing the Redis wire compatibility command, paired with a side-by-side architectural diff illustrating the NVMe memory-mapping pipeline.
- **Confidence**: High
```
