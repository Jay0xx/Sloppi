# Sloppi v2.0 Dependency Policy: High-Craft Motion, Creative Tech & Lean Architecture

Dependency Policy governs how third-party packages are selected so your frontend achieves **world-class interactive polish and art direction** without unnecessary bloat.

> **CRITICAL v2.0 UPDATE**:
> Sloppi v2.0 **explicitly encourages** purposeful animation, physics, creative coding, and accessible headless UI primitives when they elevate art direction and interactivity. Never strip an interface down to lifeless static HTML out of misguided package austerity.

---

## 1. High-Value Dependencies Explicitly Encouraged

When building rich, memorable interfaces, use best-in-class libraries for motion, interactivity, and accessibility:

| Capability Domain | Recommended Packages | When to Use |
| :--- | :--- | :--- |
| **Spring Physics, Shared Layouts & Scrollytelling** | `motion` (`motion/react` or `framer-motion`) | Shared `layoutId` transitions, interruptible bottom sheets, tactile spring gestures (`whileTap`, `whileHover`), scroll-linked choreography (`useScroll`, `useTransform`), and `AnimatePresence` view transitions. |
| **Accessible Headless UI Primitives** | `@radix-ui/react-*`, `cmdk`, `vaul` | Focus-trapped modal dialogs, command palettes (`⌘K`), accessible popovers/selects, and physics-driven mobile drawers. |
| **Expressive Web Typography** | `next/font/google` or `@fontsource/*` | Loading distinctive Display, Serif, Grotesque, and Monospace pairings with zero layout shift. |
| **Interactive Canvas, Shaders & 3D (When Thesis Demands)** | `three` / `@react-three/fiber` / lightweight HTML5 `<canvas>` 2D/WebGL | When the chosen creative direction features an interactive shader field, spatial node graph, or 3D physical artifact. |
| **Single Curated Icon Family** | `lucide-react` or `@phosphor-icons/react` | Choose **one** icon library per project and enforce uniform stroke weight (`1.5px` or `1.75px`), paired with custom bespoke SVGs for hero schematics. |
| **Dynamic Class Composition** | `clsx` + `tailwind-merge` | Clean variant composition in component primitives. |

---

## 2. What to Avoid (True Package Slop)

1. **Never Mix Multiple Icon Libraries**: Do not mix `lucide-react`, `react-icons/fa`, and `@mui/icons-material` in the same app.
2. **Never Install Heavy monolithic UI Kits That Override Your Art Direction**: Avoid dropping in default unstyled Material UI (`@mui/material`), Ant Design (`antd`), or Bootstrap themes that make your app look like a 2019 corporate intranet.
3. **Prefer Custom SVG for Domain Diagrams & Micro-Charts**: Instead of fighting a 500KB charting library for a signature hero visualization, craft bespoke, interactive, animated SVGs (`<svg>`, `<motion.path>`) that match your exact typography and grid tokens.
4. **Always Respect Reduced Motion**: Whenever using `motion` or canvas animations, wire `<MotionConfig reducedMotion="user">` and `@media (prefers-reduced-motion: reduce)` so accessibility is never compromised.
