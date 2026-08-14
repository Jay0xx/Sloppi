# Sloppi Dependency Policy & Lean Architecture

Dependency Policy governs the introduction of third-party NPM packages, external scripts, and UI libraries into a codebase.

A coding agent must never indiscriminately install packages simply because they are popular, or add heavy JavaScript libraries to solve problems easily handled by modern CSS.

---

## 1. The 6 Dependency Evaluation Gates

Before proposing or executing `npm install`, `pnpm add`, or `yarn add`, the agent must verify all six evaluation gates:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. ABSOLUTE NECESSITY       ──► Is this dependency strictly necessary? │
│ 2. NATIVE CAPABILITY TEST   ──► Can modern CSS/JS solve this cleanly? │
│ 3. COMPATIBILITY & OVERHEAD ──► Does it conflict with existing stack?  │
│ 4. ACCESSIBILITY BENEFIT    ──► Does it provide robust ARIA/keyboard?  │
│ 5. BUNDLE SIZE FOOTPRINT    ──► Is bundle impact justified (<25KB)?    │
│ 6. PRODUCTION STABILITY     ──► Is it actively maintained & typed?     │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Native Alternatives to Common Dependency Reflexes

| ❌ Lazy AI Dependency Reflex | ❌ Why It Fails | ✅ Sloppi Lean Native Solution |
| :--- | :--- | :--- |
| `framer-motion` for basic hover/tab fades | Adds 35KB JS bundle for simple opacity shifts. | Native CSS transitions (`transition: opacity 240ms var(--ease-snappy)`). |
| `react-slick` / `swiper` for card rows | Heavy bundle, complex touch listeners. | Native CSS Scroll Snap (`scroll-snap-type: x mandatory;`). |
| `lodash` / `ramda` for simple array operations | Redundant JS overhead. | Native ES6+ methods (`Array.prototype.map`, `filter`, `reduce`). |
| `react-icons` (full bundle) | Imports thousands of unused icons into build. | Targeted single-icon imports or clean inline SVGs. |
| `classnames` / `clsx` (for simple static classes) | Unnecessary for static string concatenation. | Template literals (use `clsx`/`tailwind-merge` only when handling dynamic conditional class collisions). |

---

## 3. Justified Dependencies: High-Value Primitives

Dependencies **are** justified when they provide complex accessibility, focus-trapping, and keyboard management that is error-prone to hand-roll:

- **Accessible Headless Primitives**: `@radix-ui/react-dialog`, `@radix-ui/react-dropdown-menu`, `@radix-ui/react-popover`.
- **Complex Floating Positioning**: `@floating-ui/dom` (for sub-pixel collision-aware tooltips).
- **Utility Conflict Resolution**: `tailwind-merge` + `clsx` (when composing dynamic Tailwind variant wrappers).
