# Sloppi Change Strategy & Minimal Intervention

The Change Strategy defines the tactical order of code modification and enforces the principle of minimal intervention, ensuring that changes solve root causes with the smallest possible blast radius.

---

## 1. The 11-Tier Change Strategy Order

When a design flaw is diagnosed, the agent works through the architectural hierarchy from structural to surface:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. CONTENT         ──► Fix copy clarity, length, or factual precision. │
│ 2. STRUCTURE       ──► Fix semantic HTML landmarks and DOM hierarchy.  │
│ 3. HIERARCHY       ──► Adjust visual contrast, optical scale, and focus│
│ 4. LAYOUT          ──► Modify grid templates, column spans, or flex.   │
│ 5. TYPOGRAPHY      ──► Adjust scale ratios, line measure, and leading. │
│ 6. SPACING         ──► Adjust 4px/8px margin, padding, and gap tokens. │
│ 7. COLOR           ──► Re-assign semantic color roles and contrast.    │
│ 8. GEOMETRY        ──► Adjust concentric border radius and 1px borders.│
│ 9. INTERACTION     ──► Add focus rings, hover shifts, and active press.│
│ 10. MOTION         ──► Calibrate duration scales and ease curves.      │
│ 11. DECORATION     ──► Refine subtle hairline dividers and indicators. │
└────────────────────────────────────────────────────────────────────────┘
```

> **Directness Rule**: If an issue is clearly a local color contrast failure, fix the color token directly. Do not touch typography simply because it appears earlier in the sequence. The order represents a **root-cause diagnostic hierarchy**, not a rigid mechanical sequence.

---

## 2. The Principle of Minimal Intervention

Always prefer the smallest, most localized change that completely resolves the underlying defect:

| Problem Identified | ❌ Destructive Over-Correction | ✅ Sloppi Minimal Intervention |
| :--- | :--- | :--- |
| **Secondary button competes with primary** | Redesign the entire CTA component system across the application. | Change secondary variant class from solid fill to `1px solid var(--color-border)` with transparent background. |
| **Hero headline wraps awkwardly** | Rewrite the entire hero section layout and change global container widths. | Add `text-wrap: balance;` or wrap key words with a non-breaking space (`&nbsp;`). |
| **Feature cards feel repetitive** | Add purple mesh gradients, 3D floating blobs, and glowing neon borders. | Refactor 1 card into an interactive monospace CLI terminal and 1 into an SVG architecture diff. |
| **Mobile navigation overflows** | Swap the entire project navigation framework for an external drawer library. | Apply `flex-wrap: wrap;` or collapse desktop links behind an accessible native toggle menu. |

---

## 3. Design Drift Protection & Token Discipline

Every modification made during refinement must be verified against `DESIGN.md`:
- **Zero Silent Expansion**: Never introduce ad-hoc hex values (`#4f46e5`), arbitrary margins (`27px`), or new typography sizes without checking the token registry.
- **Intentional System Updates**: If a refinement legitimately requires a new design primitive (e.g. an expanded table surface token `--color-surface-table`), the agent must **update `DESIGN.md` first** before committing the code change.
