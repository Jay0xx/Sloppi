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

## 2. Installing & Integrating Verified Packages and Copyable Components

When an interface genuinely benefits from an external primitive or copyable component—never as an automatic default—Sloppi installs and integrates it cleanly into the **target app**:

### App-Scoped Installation Workflow
1. **Detect the App's Package Manager & Stack**: Inspect lockfiles (`pnpm-lock.yaml`, `yarn.lock`, `bun.lockb`, `package-lock.json`) or Expo/Swift manifests and use that exact package manager. Install runtime dependencies **into the app that uses them**, never into skill directories.
2. **Fetch Current Docs & Discovery Tools First**:
   - Query **`Context7`** (`resolve-library-id`, `query-docs`) for current version setup and API signatures.
   - Use **`shadcn` MCP** (`search_items_in_registries`, `view_items_in_registries`, `get_add_command_for_items`) for `@shadcn` or third-party shadcn registries (`https://oxyn.space/r/registry.json`).
   - Use **`Dissolve` MCP** (`list_variants`, `get_variant`, `get_setup`) when integrating `react-native-dissolve` in Expo / React Native.
3. **Review Prerequisites & Generated Files**: Inspect copied component source, `package.json`/lockfile diffs, peer dependencies, Babel/Metro/Vite plugins, CSS token imports, and provider wrappers before accepting the integration.
4. **Adapt to Design Tokens & Real State**: Replace generic demo colors/labels with the project's semantic tokens (`--color-*`, `--radius-*`, NativeWind `@theme inline`) and bind animations to real app state (`aria-busy`, async submission, stream status, reduced motion).

### Verified Source Integration Reference

| Source & Official Publisher | Platform | Official Installation Routes | Prerequisites & Fallback Check |
| :--- | :--- | :--- | :--- |
| **Dissolve** ([rs-4/dissolve](https://github.com/rs-4/dissolve), MIT) | React Native & Expo | **Engine**: `npx expo install react-native-dissolve @shopify/react-native-skia react-native-reanimated react-native-worklets react-native-gesture-handler expo-haptics`<br>**Components CLI**: `npx react-native-dissolve init`, `npx react-native-dissolve list`, `npx react-native-dissolve add <component>` | Wrap root layout once in `<GestureHandlerRootView>` + `<DissolveProvider>` (plus `<ToastProvider>` for toasts). Bare RN needs `'react-native-worklets/plugin'` in `babel.config.js`. CLI-copied components require **NativeWind v5** (`nativewind@5.0.0-preview.4`, `react-native-css@3.0.7`, `tailwindcss@^4`, `@tailwindcss/postcss`, `tailwind-merge`, `lightningcss` `1.30.1` override, Metro `withNativewind`). |
| **Distortion Waves** ([libraries.dev/waves](https://libraries.dev/waves) / [Jakubantalik/Libraries.dev](https://github.com/Jakubantalik/Libraries.dev), MIT) | React Web & SwiftUI | **React**: `npm install distortion-waves` *(check npm availability first: `npm view distortion-waves` returned `404` on npmjs at verification time while `packages/distortion-waves` source `v0.1.0` lives in the GitHub repo)*<br>**SwiftUI**: Swift package product `DistortionWavesKit` from `https://github.com/Jakubantalik/Libraries.dev` (`branch: "main"`) | **React**: React 18+, **WebGL2**, CORS for cross-origin media, no iframes; crossfade fallback when WebGL2 is unavailable or `reducedMotion` applies.<br>**SwiftUI**: **iOS 17+ / macOS 14+**, build via **Xcode** to compile `DistortionWaveShaders.metal` (not SwiftPM CLI alone), opaque backgrounds, no UIKit views; Reduce Motion crossfade fallback. |
| **Oxyn** ([oxyn.space](https://oxyn.space/) / [lokidotdev/oxyn-frontend](https://github.com/lokidotdev/oxyn-frontend), MIT) | React Web (`"use client"`) | `npx shadcn@latest add https://oxyn.space/r/<slug>.json` (or `shadcn` MCP / `oxyn` MCP `search_loaders` + `get_loader`) | Imports only from `react`; uses HTML5 `<canvas>`; renders `role="status"` with `label` and holds still under `prefers-reduced-motion`. Not for determinate progress or Vue/Svelte/plain HTML. |
| **Wobli** ([wobli.space](https://wobli.space/) / [lokidotdev/wobli](https://github.com/lokidotdev/wobli), MIT) | Web JS/TS & React | `npm i wobli` (`wobli` engine, `wobli/react` `<Sticker>`, `wobli/icons/<slug>`), or export transparent PNGs | HTML5 `<canvas>`, `react >= 18` optional. Check canvas runtime cost and pause/still behavior under `prefers-reduced-motion`. |
| **shadcn/ui & DesignEng Tools** ([ui.shadcn.com](https://ui.shadcn.com/docs/mcp), [designeng.tools](https://www.designeng.tools/)) | Web / React | Follow `designeng.tools` entries to upstream publisher; use `shadcn` MCP or project package manager (`pnpm dlx` / `npx` / `bunx`) | Verify `components.json`, Tailwind/CSS variable compatibility, bundle weight, accessibility, and OSS license before keeping copied code. |

---

## 3. What to Avoid (True Package Slop)

1. **Never Auto-Import Reference Demo Stacks**: Do not pull React Native Skia (`dissolve.rselmi.com`) into web apps, WebGL2/Metal shader wrappers (`libraries.dev/waves`) where CSS View Transitions work, or continuous canvas loops (`wobli.space`) without checking runtime and reduced-motion impact.
2. **Never Mix Multiple Icon Libraries**: Do not mix `lucide-react`, `react-icons/fa`, and `@mui/icons-material` in the same app.
3. **Never Install Heavy Monolithic UI Kits That Override Your Art Direction**: Avoid dropping in default unstyled Material UI (`@mui/material`), Ant Design (`antd`), or Bootstrap themes that overwrite your visual language.
4. **Prefer Custom SVG for Domain Diagrams & Micro-Charts**: Instead of a 500KB charting library for a single schematic, craft bespoke SVGs matched to your typography and tokens.
5. **Always Enforce Reduced Motion & Repeated-Activation Safety**: Every motion dependency or CSS transition must degrade gracefully under `@media (prefers-reduced-motion: reduce)` / `<MotionConfig reducedMotion="user">` and stay safe on rapid re-triggers.
