# Sloppi Audit Severity Model & Triage Framework

The Severity Model establishes a rigorous, unambiguous classification system for prioritizing audit findings, preventing agents from fixing minor cosmetic details while functional or accessibility blockers remain unaddressed.

---

## 1. The 4-Tier Severity Hierarchy

```
┌────────────────────────────────────────────────────────────────────────┐
│ TIER 1: BLOCKER                                                        │
│ Definition: Prevents core task execution, violates accessibility       │
│             standards, or catastrophically breaks responsive layout.   │
│ Examples:   Broken navigation links, failing WCAG contrast (<3:1),     │
│             horizontal body scroll overflow, missing form labels,      │
│             sub-44px touch targets on primary mobile actions.          │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 2: HIGH                                                           │
│ Definition: Major structural, hierarchy, or brand thesis failure.      │
│ Examples:   Equal Loudness Syndrome, runaway body line length (>80ch), │
│             generic AI default reflex (e.g. 3-card grid for diff),     │
│             desktop layout crushed on mobile, fabricated social proof. │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 3: MEDIUM                                                         │
│ Definition: Noticeable quality, spatial rhythm, or token inconsistency.│
│ Examples:   Monotone section heights, arbitrary unmapped hex values,   │
│             headline orphans with single-word drop lines, inconsistent │
│             icon stroke weights, loose display leading.                │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 4: LOW                                                            │
│ Definition: Minor aesthetic refinement or micro-interaction polish.    │
│ Examples:   Subtle 2px alignment tweak, micro-timing curve adjustment  │
│             (150ms → 120ms), minor hover shadow opacity shift.         │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Action Triage Matrix

Every finding from the audit engine is categorized into an action bucket:

| Action Bucket | Qualification Criteria | Execution Timing |
| :--- | :--- | :--- |
| **FIX NOW** | All `BLOCKER` and `HIGH` severity findings. | Must be resolved immediately before writing additional features. |
| **FIX NEXT** | All `MEDIUM` severity findings with High/Medium confidence. | Resolved in the second refinement pass. |
| **CONSIDER** | `LOW` severity polish items or architectural trade-offs. | Evaluated during final review pass. |
| **ACCEPT** | Intentional design decisions documented in the Implementation Log. | Preserved as intentional product choices. |

---

## 3. The Human Judgment Boundary

Sloppi recognizes that certain qualitative evaluations require human designer or stakeholder review:
- **Brand Resonance**: Whether a bold editorial serif matches the executive team's vision.
- **Strategic Tone**: Whether a humorous or provocative headline aligns with company policy.
- **Subjective Aesthetics**: Nuanced personal preferences regarding color temperature or whitespace volume.

> **Rule**: When evaluating subjective brand decisions, the agent flags the issue as `CONSIDER` with `Low` confidence, framing it as an informed recommendation rather than an objective defect.
