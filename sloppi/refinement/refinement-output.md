# Sloppi Standardized Refinement Output Schema

The Refinement Output is the formal logging artifact produced at the conclusion of each refinement iteration. It documents the exact modifications made, tracks before-and-after visual changes, monitors regressions, and records the state transition decision.

---

## 1. The 11-Field Refinement Iteration Schema

Every refinement pass must be recorded in this standardized markdown structure:

```markdown
### Refinement Pass: Iteration [Number]

- **Iteration**: [01 | 02 | 03 ...]
- **Objective**: [Single primary goal, e.g. "Eliminate 3-card monotony in feature section"]
- **Findings Addressed**: [List of finding IDs, e.g. AS-004, HI-002]
- **Changes Made**: [Specific description of code diffs and token adjustments]
- **Files Changed**: [Exact file paths, e.g. `src/sections/FeatureSection.tsx`]
- **Expected Effect**: [What was predicted to improve in the visual composition]
- **Actual Effect**: [What was observed after re-rendering in the viewport]
- **Regressions**: [None | Description of collateral defect and severity]
- **Remaining Issues**: [Summary count of remaining Blockers/High/Medium findings]
- **Decision**: [CONTINUE | ACCEPT | ROUTE_RE_ENTRY | REQUEST_HUMAN_REVIEW]
- **Confidence**: [High | Medium | Low]
```

---

## 2. Canonical Refinement Iteration Example

```markdown
### Refinement Pass: Iteration 02

- **Iteration**: 02
- **Objective**: Eliminate repetitive 3-card grid reflex in feature section.
- **Findings Addressed**: `AS-004` (Anti-Slop: Universal Card Reflex) & `HI-002` (Hierarchy: Equal Loudness).
- **Changes Made**: 
  - Refactored `FeatureSection.tsx` from a 3-column symmetrical card grid into an asymmetric 8+4 subgrid.
  - Replaced Card 1 with an interactive monospace CLI terminal (`<InteractiveREPL />`) showcasing the live Redis protocol command.
  - Replaced Cards 2 & 3 with an annotated SVG architecture dataflow illustrating the lock-free io_uring pipeline.
- **Files Changed**: `src/sections/FeatureSection.tsx`, `src/components/InteractiveREPL.tsx`.
- **Expected Effect**: Break visual template feel, establish authentic technical authority, and clarify feature domain differences.
- **Actual Effect**: Asymmetric layout immediately guides eye to live terminal; reading rhythm significantly enhanced; zero card fatigue.
- **Regressions**: None detected across Mobile (390px), Tablet (768px), or Desktop (1280px).
- **Remaining Issues**: 0 Blockers, 0 High, 2 Medium (subtle table padding, headline orphan).
- **Decision**: CONTINUE (Proceed to Iteration 03 for typography balancing).
- **Confidence**: High
```

---

## 3. Cumulative Refinement Progress Log

```markdown
### Refinement Session Summary

| Iteration | Primary Objective | Addressed | Result / Regressions | Next State |
| :--- | :--- | :--- | :--- | :--- |
| **Pass 01** | Fix mobile horizontal overflow & touch targets | `RE-001`, `AC-002` | Overflow resolved; zero regressions | `REFINE (Pass 02)` |
| **Pass 02** | Refactor repetitive feature cards to bento | `AS-004`, `HI-002` | Asymmetry established; zero regressions| `REFINE (Pass 03)` |
| **Pass 03** | Balance hero display typography & line measure | `TY-001`, `SP-002` | `text-wrap: balance` applied | `ACCEPT (Stopping criteria met)` |
```
