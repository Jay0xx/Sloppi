# Sloppi Motion & Micro-Interaction Architecture

Motion in Sloppi is governed by physical purpose, spatial continuity, and user feedback. Grounded in research from **60fps.design**, motion is treated as an ergonomic communication channel rather than theatrical decoration.

A coding agent must never animate elements gratuitously or introduce sluggish fade-in delays that block user reading and interaction.

---

## 1. The 6 Purposeful Motion Categories

Every animation in a Sloppi interface must belong to one of six functional categories:

```
1. USER FEEDBACK    ──► Instantaneous confirmation that an action was registered (Button click, toggle flip)
2. STATE TRANSITION ──► Smoothing the transition between two data states (Loading → Loaded, Row deletion)
3. SPATIAL ORIENTATION ──► Showing where an expanded view came from (Card → Fullscreen modal, Drawer slide)
4. HIERARCHICAL ENTRY ──► Staggered entrance revealing reading order (Hero headline → Canvas → CTAs)
5. SYSTEM ALERTS    ──► Drawing immediate attention to critical operational warnings (Error shake, toast pulse)
6. CRAFT & DELIGHT  ──► Micro-physics on key brand interactions (Subtle spring settle on completed tasks)
```

---

## 2. Duration & Velocity Standards

Animation durations must be calibrated to human cognitive perception and physical motor response:

| Motion Tier | Duration Token | Time (ms) | Typical Application |
| :--- | :--- | :--- | :--- |
| **Instantaneous Feedback** | `--duration-instant` | `100ms` | Checkbox tick, button press scale, toggle state switch. |
| **Micro-Interactions** | `--duration-fast` | `150ms` | Hover color shifts, tooltip reveals, dropdown chevron rotation. |
| **Component Transitions** | `--duration-normal` | `240ms` | Accordion expansion, tab switching, toast banner slide-in. |
| **Modal & View Changes** | `--duration-slow` | `350ms` | Centered modal backdrop fade, side drawer slide-in, route transition. |
| **Complex Choreography** | `--duration-narrative`| `500ms` | Multi-step onboarding sequence, complex bento layout morphing. |

### The 300ms Rule
- **No everyday interactive feedback should ever exceed 300ms.** Animations exceeding 300ms create perceptible interface lag and degrade user productivity.

---

## 3. Easing & Timing Curves

Linear animations (`transition: all 0.3s linear`) look robotic and unnatural. Sloppi standardizes on physics-based cubic-bezier curves:

```css
:root {
  /* Snappy Entry & Natural Settle: Rapid acceleration with a long decelerating landing */
  --ease-standard: cubic-bezier(0.16, 1, 0.3, 1);
  
  /* Smooth Deceleration (Entering Elements) */
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
  
  /* Smooth Acceleration (Exiting / Dismissed Elements) */
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  
  /* Spring Simulation: Subtle bounce on completion */
  --ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);
}
```

---

## 4. Spatial Continuity & Layout Morphing

When an element transitions between two visual states (e.g., clicking a summary card to open a full detail modal):
- **Shared Spatial Origin**: The modal must visually expand outward from the trigger card's coordinates rather than popping into existence from screen center.
- **Preserve Context**: Surrounding elements should gently shift rather than abruptly disappearing.

---

## 5. Accessibility & Reduced Motion Protocol

Every Sloppi stylesheet must provide comprehensive `@media (prefers-reduced-motion: reduce)` fallbacks:

```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```
- Under reduced motion, state changes occur instantaneously via immediate opacity cuts, preserving functional state transitions without vestibular discomfort.
