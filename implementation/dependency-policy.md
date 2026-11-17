# Sloppi v2.0 Dependency Policy: Stack Fit, Dependency Cost, Licensing & Lean Motion

Dependency Policy governs how third-party packages are evaluated and selected so your frontend achieves **world-class craft and interactive clarity** without runtime bloat, license surprises, or unexamined demo lock-in.

> **CRITICAL RULES (v2.0)**:
> 1. **Start With Behavior & Stack Fit**: Choose an implementation that fits the existing stack first (native CSS / View Transitions / WAAPI before JS physics libraries; lightweight DOM transitions before WebGL/Canvas).
> 2. **Inspect Cost & License Before Recommending**: Before recommending any external primitive (from `designeng.tools`, npm, or component registries), inspect its **bundle/runtime cost**, **peer dependencies** (e.g., React version, WebGL2, Metal/Xcode, Skia/Reanimated), **browser/OS fallback**, and **license terms** (MIT/Apache vs. proprietary/unspecified).
> 3. **Reference Demos Never Become Automatic Dependencies or Default Effects**: Studying `libraries.dev/waves`, `dissolve.rselmi.com`, `oxyn.space`, or `wobli.space` informs interaction mechanics—it never justifies importing their runtime or applying their signature effect by default.

---

## 1. Implementation Escalation Ladder & High-Value Primitives

| Capability Domain | Preferred Stack-Fit Options | Dependency Cost & License Gate |
| :--- | :--- | :--- |
| **Standard State Feedback, Reveals & Continuity** | Native CSS Transitions, `@keyframes`, Scroll-Driven CSS, CSS View Transitions API | **Zero external JS cost.** Default choice for hovers, presses, tabs, and origin-anchored transitions when physics interruption isn't needed. |
| **Spring Physics, Shared Layouts & Interruptible Gestures** | `motion` (`motion/react`) | Use in React stacks when interruptible drag/gesture physics, shared `layoutId` continuity, or animated unmounts justify ~30KB+ runtime cost (MIT). Always wire `<MotionConfig reducedMotion="user">`. |
| **Accessible Headless UI Primitives** | `@radix-ui/react-*`, `cmdk`, `vaul` | Verify React peer compatibility and bundle impact; prefer native `<dialog>`/Popover API when simple ergonomics suffice. |
| **Expressive Web Typography** | `next/font/google`, `@fontsource/*`, or self-hosted WOFF2 | Load only needed weights/subsets with `font-display: swap` and zero layout shift. |
| **Canvas, Shaders & 3D (Only When Product Thesis Demands)** | Native HTML5 `<canvas>` 2D/WebGL, `three`, `@react-three/fiber` | Heavy GPU/CPU and bundle cost; verify WebGL fallback, CORS constraints, reduced-motion pause behavior, and OSS license before adopting. |
| **Single Curated Icon Family** | `lucide-react`, `@phosphor-icons/react`, or inline SVGs | Choose **one** family (`1.5px` or `1.75px` stroke), or use inline SVG for small icon sets to avoid extra packages. |

---

## 2. What to Avoid (True Package Slop)

1. **Never Auto-Import Reference Demo Stacks**: Do not pull React Native Skia (`dissolve.rselmi.com`) into web apps, WebGL2/Metal shader wrappers (`libraries.dev/waves`) where CSS View Transitions work, or continuous canvas loops (`wobli.space`) without checking runtime and reduced-motion impact.
2. **Never Mix Multiple Icon Libraries**: Do not mix `lucide-react`, `react-icons/fa`, and `@mui/icons-material` in the same app.
3. **Never Install Heavy Monolithic UI Kits That Override Your Art Direction**: Avoid dropping in default unstyled Material UI (`@mui/material`), Ant Design (`antd`), or Bootstrap themes that overwrite your visual language.
4. **Prefer Custom SVG for Domain Diagrams & Micro-Charts**: Instead of a 500KB charting library for a single schematic, craft bespoke SVGs matched to your typography and tokens.
5. **Always Enforce Reduced Motion & Repeated-Activation Safety**: Every motion dependency or CSS transition must degrade gracefully under `@media (prefers-reduced-motion: reduce)` / `<MotionConfig reducedMotion="user">` and stay safe on rapid re-triggers.
