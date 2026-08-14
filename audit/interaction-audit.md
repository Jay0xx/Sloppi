# Sloppi Interaction & State Audit

The Interaction Audit inspects how components respond to user interaction, provide real-time state feedback, and implement keyboard navigation.

---

## 1. The 6-Point Interaction Audit Checklist

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. FOCUS VISIBILITY VERIFICATION──► Visible 2px high-contrast focus ring│
│                                    on Tab focus (:focus-visible).      │
│ 2. HOVER & ACTIVE FEEDBACK     ──► Instantaneous brightness/scale shift │
│                                    on mouse hover and active press.    │
│ 3. DISABLED STATE CLARITY      ──► cursor: not-allowed; opacity: 0.45; │
│                                    pointer events disabled.            │
│ 4. MOTION DURATION DISCIPLINE  ──► Micro-timings strictly 120ms–240ms; │
│                                    zero lagging 800ms fade animations. │
│ 5. ZERO GRATUITOUS ANIMATIONS  ──► Zero constantly pulsing glow blobs   │
│                                    or spinning icon badges.            │
│ 6. REDUCED MOTION COMPLIANCE   ──► Animations cleanly disabled under   │
│                                    @media (prefers-reduced-motion).    │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Interaction Deficiency Catalog & Fixes

| Interaction Flaw | Diagnostic Symptom | Severity | Sloppi Remediation |
| :--- | :--- | :--- | :--- |
| **Missing Focus Outlines** | Developer applied `outline: none;` without custom `:focus-visible` styling, breaking keyboard access. | **BLOCKER** | Apply universal `:focus-visible { outline: 2px solid var(--color-focus-ring); outline-offset: 2px; }`. |
| **Dead Interactive Elements** | Button has zero hover, focus, or active state feedback, feeling like static text. | **HIGH** | Add `:hover` background brightness shift and `:active { transform: scale(0.98); }`. |
| **Slow Lagging Transitions** | Modal or dropdown takes 600ms to open, making software feel sluggish and unresponsive. | **MEDIUM** | Speed transition to `--duration-normal` ($240\text{ms}$) with `cubic-bezier(0.16, 1, 0.3, 1)`. |
| **Distracting Infinite Loops** | A badge constantly pulses and vibrates on the screen, stealing attention from reading. | **MEDIUM** | Remove infinite `@keyframes` loop; reserve animation for one-time state transitions. |
| **Broken Loading Indicators** | Submitting a form gives zero feedback while in-flight, prompting repeated double clicks. | **HIGH** | Set `aria-busy="true"`, disable button clicks, and show inline loading spinner. |
