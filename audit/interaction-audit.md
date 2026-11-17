# Sloppi Interaction & State Audit

The Interaction Audit inspects how components respond to user interaction, provide real-time state feedback, and implement keyboard navigation.

---

## 1. The 8-Point Interaction & Motion Verification Checklist

Verify interactive state behavior using a **browser recording or interaction trace** for timing and continuity (paired with **screenshots** for resting/settled layout and contrast):

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. FOCUS VISIBILITY & KEYBOARD ──► Visible 2px high-contrast ring on   │
│                                    :focus-visible; Tab/Enter/Esc parity│
│ 2. TOUCH & TARGET ERGONOMICS   ──► ≥44×44px touch targets; zero hover- │
│                                    only controls; clean swipe/tap feel │
│ 3. TRIGGER & END STATE CLARITY ──► Clear trigger causality, anchored   │
│                                    context, and clean visual settlement│
│ 4. REPEATED ACTIVATION SAFETY  ──► Rapid re-triggers cancel/reverse    │
│                                    cleanly with zero queued backlog    │
│ 5. DISABLED & IN-FLIGHT STATES ──► cursor: not-allowed; opacity: 0.45; │
│                                    aria-busy="true" prevents double-tap│
│ 6. MOTION DURATION DISCIPLINE  ──► Micro-timings strictly 100ms–240ms; │
│                                    zero lagging 800ms fade animations  │
│ 7. ZERO GRATUITOUS ANIMATIONS  ──► Zero pulsing glow blobs, spinning   │
│                                    badges, or forced demo defaults     │
│ 8. REDUCED MOTION COMPLIANCE   ──► @media (prefers-reduced-motion)     │
│                                    preserves state changes cleanly     │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Interaction Deficiency Catalog & Fixes

| Interaction Flaw | Diagnostic Symptom | Severity | Sloppi Remediation |
| :--- | :--- | :--- | :--- |
| **Missing Focus Outlines** | Developer applied `outline: none;` without custom `:focus-visible` styling, breaking keyboard access. | **BLOCKER** | Apply universal `:focus-visible { outline: 2px solid var(--color-focus-ring); outline-offset: 2px; }`. |
| **Dead Interactive Elements** | Button/control has zero hover, focus, or active state feedback, feeling like static text. | **HIGH** | Add `:hover` surface shift, `:focus-visible` ring, and `:active { transform: scale(0.98); }`. |
| **Hover-Only or Small Mobile Controls** | Critical interaction only reveals on `:hover` or uses `<44px` tap targets on touch viewports. | **HIGH** | Expose touch-accessible triggers at `>=44×44px` and test swipe/tap thresholds. |
| **Repeated-Activation Queueing / Drift** | Rapid double-clicking or mid-flight re-trigger stacks delayed transitions or loses focus. | **HIGH** | Make transitions interruptible/cancellable, guard async submits with `aria-busy`, and preserve focus. |
| **Slow Lagging Transitions** | Modal or dropdown takes 600ms to open, making software feel sluggish and unresponsive. | **MEDIUM** | Speed transition to `--duration-normal` ($240\text{ms}$) with `cubic-bezier(0.16, 1, 0.3, 1)`. |
| **Distracting Infinite Loops** | A badge or decorative illustration constantly loops, stealing attention from reading or failing reduced motion. | **MEDIUM** | Remove decorative loops; reserve motion for feedback, orientation, or continuity with `prefers-reduced-motion` pause/cut. |
| **Broken Loading Indicators** | Submitting a form gives zero feedback while in-flight, prompting repeated double clicks. | **HIGH** | Set `aria-busy="true"`, disable duplicate clicks, and show inline anchored progress/state feedback. |
