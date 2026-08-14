# Sloppi Consistency vs. Monotony Audit

The Consistency Audit evaluates whether an interface maintains disciplined systemic token harmony while avoiding the deadening trap of visual monotony.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   THE CONSISTENCY VS. MONOTONY RULE                    │
│                                                                        │
│ "Consistency must never become monotony. A section can intentionally   │
│  differ from another section in height, density, and ground tone.      │
│  The audit question is: 'Is the difference intentional and reasoned?'  │
│  NOT: 'Is every single container identical?'"                          │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 1. Systemic Consistency (What MUST Be Consistent)

The following properties must remain mathematically uniform across all components:
- **Typographic Scale Ratios**: All headings and body text consume the declared modular scale.
- **Button Tokens**: Uniform padding, height ($40\text{px}$), font weight ($600$), and hover micro-interaction timings ($120\text{ms}$).
- **Semantic Color Roles**: `--color-brand` always indicates primary action; `--color-canvas-alt` always indicates elevated section grounds.
- **Concentric Radii**: Inner container radius = Outer container radius minus padding.
- **Iconography**: Single icon family with uniform optical stroke weight (`1.5px` or `2.0px`).

---

## 2. Intentional Modulation (What SHOULD Vary)

The following properties are deliberately modulated down the page to maintain active reading engagement:
- **Section Height**: Alternating compact data sections ($320\text{px}$) with deep interactive sandboxes ($850\text{px}$).
- **Spatial Density**: High-density telemetry HUDs alternating with generous editorial whitespace ($128\text{px}$).
- **Ground Planes**: Alternating `--color-canvas` with `--color-canvas-alt`.
- **Layout Grids**: Asymmetric bento grids alternating with side-by-side code walkthroughs.

---

## 3. Consistency Deficiency Catalog

| Inconsistency Pattern | Type | Severity | Sloppi Remediation |
| :--- | :--- | :--- | :--- |
| **Mixed Icon Families** | Accidental Slop | **MEDIUM** | Standardize on a single curated icon family (`Lucide` or `Phosphor`) across all components. |
| **Arbitrary Border Radii** | Accidental Slop | **MEDIUM** | Map all container corners strictly to `--radius-md` ($8\text{px}$) or `--radius-lg` ($12\text{px}$). |
| **Monotone Card Stacking** | Accidental Monotony | **HIGH** | Replace 3 consecutive identical card sections with an asymmetric bento and a data comparison table. |
