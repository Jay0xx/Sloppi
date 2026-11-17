# Sloppi Interaction & State Implementation

Interaction Implementation governs how interactive components communicate state, feedback, and keyboard navigation to the user.

A coding agent must never build static "dead" components that lack hover feedback, omit focus indicators, or invent chaotic animations that trigger cognitive fatigue.

---

## 1. The 12 Canonical Component States

Every interactive primitive (Button, Input, Card, Link, Tab, Modal) must account for its relevant states:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. RESTING / DEFAULT   ──► Clean base token styling                    │
│ 2. HOVER (:hover)      ──► Subtle brightness or surface tint shift     │
│ 3. FOCUS (:focus-visible) ─► 2px high-contrast focus ring with offset  │
│ 4. ACTIVE / PRESSED    ──► Subtle scale(0.98) tactile compression      │
│ 5. SELECTED / CURRENT  ──► Persistent active indicator (aria-selected) │
│ 6. DISABLED            ──► cursor: not-allowed; opacity: 0.45;         │
│ 7. LOADING / BUSY      ──► aria-busy="true"; inline spinner, disabled  │
│ 8. SUCCESS             ──► Transient green accent / checkmark fade-in  │
│ 9. ERROR / INVALID     ──► aria-invalid="true"; red border + message   │
│ 10. EXPANDED / OPEN    ──► aria-expanded="true"; height transition     │
│ 11. DRAG / ACTIVE HOLD ──► Elevated shadow-lg + cursor: grabbing       │
│ 12. FOCUSED WITHIN     ──► Container-level focus highlight             │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. The Focus Visibility Mandate

Keyboard accessibility is non-negotiable. Sloppi strictly prohibits removing focus outlines with `outline: none`:

```css
/* Universal High-Contrast Focus Ring Protocol */
:focus-visible {
  outline: 2px solid var(--color-focus-ring);
  outline-offset: 2px;
}

/* Button Component State Implementation Example */
.btn-primary {
  background-color: var(--color-brand);
  color: var(--color-brand-contrast);
  font-family: var(--font-body);
  font-size: var(--font-size-body-sm);
  font-weight: 600;
  padding: var(--space-2) var(--space-4);
  border-radius: var(--radius-md);
  border: 1px solid transparent;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--space-2);
  transition: background-color var(--duration-fast) var(--ease-snappy),
              transform var(--duration-fast) var(--ease-snappy),
              box-shadow var(--duration-fast) var(--ease-snappy);
}

.btn-primary:hover:not(:disabled) {
  background-color: var(--color-brand-hover);
  box-shadow: var(--shadow-sm);
}

.btn-primary:active:not(:disabled) {
  transform: scale(0.98);
}

.btn-primary:disabled {
  opacity: 0.45;
  cursor: not-allowed;
  pointer-events: none;
}
```

---

## 3. Behavior-First Motion Strategy, Stack Fit & Dependency Governance

Motion in Sloppi exists to **clarify feedback, orientation, or continuity**—never as decorative amusement or unexamined demo replication.

1. **Start With the Intended Behavior**:
   - First define the exact product moment and what must change for the user (e.g., *"Confirm payment transition anchored from the tap target while holding amount and account steady"*, or *"Keep layout completely still so dense editorial reading stays legible"*).
   - Compare against a minimal-motion baseline (e.g., `deadsimplesites.com` restraint check): if typography, spacing, and crisp state swaps already communicate clearly, do not bolt on motion.
2. **Choose an Implementation That Fits the Existing Stack**:
   - **Native CSS Transitions / `@keyframes` / Scroll-Driven CSS**: Preferred default for hover/focus shifts, press compression, height/opacity reveals, and simple transitions when no physics interruption or cross-subtree layout morph is needed.
   - **CSS View Transitions API / WAAPI**: Strong fit for origin-anchored route/panel state changes in browser apps without heavy runtime shaders.
   - **Spring/Layout Library (`motion`, `motion/react`)**: Use when interruptible drag/gesture physics, shared `layoutId` continuity, or `AnimatePresence` unmount choreography genuinely improves orientation or touch feel in a React codebase.
   - **Canvas / WebGL / Specialized Shader Engines**: Use only when the core product thesis demands custom pixel/particle/3D simulation and the runtime budget supports it.
3. **Inspect Dependency Cost & Licensing Before Recommending an External Primitive**:
   - Before adding any package from `designeng.tools` or elsewhere, check: **bundle & runtime cost**, **peer dependencies** (React version, WebGL2, Metal shaders/Xcode, Skia/Reanimated/Worklets, CORS media constraints), **browser/device fallbacks**, and **license terms** (MIT/Apache vs. proprietary/unspecified). See [dependency-policy.md](dependency-policy.md).
4. **Reference Demos Are Never Automatic Dependencies or Default Effects**:
   - Studying `libraries.dev/waves`, `dissolve.rselmi.com`, `oxyn.space`, or `wobli.space` teaches interaction principles (activation-origin focus, anchored context, dissolve exits, role-based styling). Never auto-install their libraries or inject wave/particle/glitch/idle-loop effects as default house style.

### Motion Duration & Easing Baselines
- **Micro-Interactions (Hovers, Toggles, Buttons)**: `100–150ms` (`--duration-fast`)
- **State Transitions (Tabs, Dropdowns, State Receipts)**: `200–240ms` (`--duration-normal`)
- **Spatial Overlays (Drawers, Modals, Fullscreen Views)**: `300–350ms` (`--duration-slow`)
- **Snappy Settling Curve**: `cubic-bezier(0.16, 1, 0.3, 1)` (instant acceleration followed by smooth, natural deceleration).

---

## 4. Mandatory Proposed-Effect Specification Contract

For every proposed motion or transition beyond basic hover/focus state tokens, specify all seven dimensions before or alongside implementation:

| Contract Field | What Must Be Specified | Failure Avoided |
| :--- | :--- | :--- |
| **1. Intended Behavior & Moment** | Why this specific moment needs motion for **feedback**, **orientation**, or **continuity**. | Gratuitous hero swoops or idle loop clutter. |
| **2. Trigger** | Exact user/system trigger (tap, click, drag threshold, form submit, route change, keyboard command). | Ambiguous or accidental scroll/hover misfires. |
| **3. End State & Anchors** | What moves/updates, what **stays anchored**, how the transition settles, and final DOM/ARIA state. | Disorienting full-screen jumps or layout shift. |
| **4. Touch Behavior** | Touch/tap/swipe behavior, $\ge 44\times 44\text{px}$ hit target, interruptible drag/cancel threshold, zero hover-only controls. | Hover traps or unresponsive mobile taps. |
| **5. Keyboard Behavior** | Full parity via `Tab`, `Enter`/`Space`, `Escape`, preserved `:focus-visible` ring, and focus retention across animated mounts/unmounts. | Focus lost to `<body>` when cards/sheets transition. |
| **6. Repeated Activation** | Behavior on rapid double-clicks, mid-flight re-triggers, or state reversals (cancel/reverse cleanly without animation queueing or duplicate submits). | Stuck spinners, queued jank, or stale async state overriding current UI. |
| **7. Reduced Motion** | Explicit `@media (prefers-reduced-motion: reduce)` and/or `MotionConfig reducedMotion="user"` fallback preserving the state change instantaneously or via brief ($\le 100\text{ms}$) opacity cut. | Vestibular triggers or broken hidden states (`opacity: 0` stuck). |

```css
/* Reduced Motion Compliance: preserve functional state changes without spatial travel */
@media (prefers-reduced-motion: reduce) {
  *, ::before, ::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

---

## 5. Primary-Composition Prototyping & Dual Verification

Never develop and tune a proposed effect in an isolated blank page disconnected from real typography, overflow constraints, and layout chrome.

1. **Prototype in the Primary Composition**: Implement and test the effect directly inside the real primary composition (the above-the-fold hero or primary mobile/app flow) during Stage 4/5 ([implementation/protocol.md](protocol.md)).
2. **Screenshots for Layout & Hierarchy**: Capture viewport screenshots (`390px` mobile, `768px` tablet, `1280px+` desktop) to verify composition, focal hierarchy, contrast, and zero overlap/clipping across resting and settled states.
3. **Browser Recording or Interaction Trace for Timing & Continuity**: Capture a browser video/recording, frame sequence, or interaction timeline/DOM-state trace (via **Playwright MCP** or the `browser` subagent) across **trigger $\rightarrow$ mid-transition $\rightarrow$ settlement** (plus **repeated activation** and **reduced motion**) to verify timing, anchoring, and visual continuity.
4. **Honest Reporting**: If a live recording or trace cannot be captured in the environment, explicitly report the timing/continuity tier as `[INFERRED]` or `UNAVAILABLE` per [failure-recovery.md](../failure-recovery.md)—never claim verified timing from static code alone.

---

## 6. Installing, Adapting & Verifying External Interactive Components

When a component or motion primitive passes the behavior-first, stack-fit, cost, and license checks in [dependency-policy.md](dependency-policy.md):

1. **Verify Current Setup via Docs & Tooling**: Query **`Context7`** (`resolve-library-id`, `query-docs`), **`shadcn` MCP**, or **`Dissolve` MCP** (`get_setup`, `get_variant`) for exact installation commands, peer dependencies, provider wrappers, and platform fallbacks before editing `package.json`.
2. **Install Only in the Target App**: Use the target app's package manager (`pnpm`, `npm`, `yarn`, `bun`, or `npx expo install` / Xcode SPM) and inspect all generated/copied files (`components.json`, `components/dissolve/`, `global.css`, `babel.config.js`, `metro.config.js`, `Package.swift`).
3. **Bind to App Tokens & Real State**: Replace sample copy, hardcoded colors, and demo timers with the app's semantic design tokens and live state flags (async submission, loading state, error/success handling, `reducedMotion` props).
4. **Verify Interaction & Code Quality**:
   - **Web / React**: Review interactions and semantics with **`web-design-guidelines`**, verify bundle/rendering/re-renders with **`vercel-react-best-practices`**, and exercise click, keyboard, viewport resize, and reduced-motion states live via **`Playwright` MCP** (screenshots + trace/snapshot).
   - **React Native / Expo / SwiftUI**: Confirm provider placement, native plugin/Xcode shader compilation requirements, and platform `Reduce Motion` behavior; run project typecheck/tests cleanly.
