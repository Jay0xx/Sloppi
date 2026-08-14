# Sloppi Project Inspection & Stack Adaptation

Before modifying or generating a single line of frontend code, a Sloppi agent must thoroughly inspect the existing codebase.

Sloppi must **work with the project's established technical architecture**, rather than blindly imposing external dependencies or overwriting existing styling systems.

---

## 1. The 16-Point Project Inspection Protocol

The agent interrogates the codebase across sixteen distinct dimensions and generates a structured inspection summary:

```
┌────────────────────────────────────────────────────────────────────────┐
│                 THE 16-POINT CODEBASE INSPECTION MATRIX                │
│                                                                        │
│ 1. FRAMEWORK          ──► Next.js / React / Vue / Svelte / Astro / HTML│
│ 2. LANGUAGE           ──► TypeScript (strict/loose) vs JavaScript      │
│ 3. BUILD SYSTEM       ──► Vite / Turbopack / Webpack / Rollup / esbuild│
│ 4. PACKAGE MANAGER    ──► pnpm / npm / yarn / bun                      │
│ 5. STYLING ARCHITECTURE ─► Vanilla CSS / CSS Modules / Tailwind / SCSS │
│ 6. COMPONENT LIBRARY  ──► Radix / shadcn / Headless UI / MUI / None    │
│ 7. ROUTING MODEL      ──► App Router / Pages Router / React Router     │
│ 8. DESIGN SYSTEM STATE ─► None / Weak / Established / Mature           │
│ 9. TOKEN INFRASTRUCTURE ─► CSS Variables / Tailwind Config / JS Theme  │
│ 10. ASSET PIPELINE    ──► Public directory / SVG bundler / CDN / static│
│ 11. COMPONENT DIRECTORY ─► `src/components/`, `components/ui/`, atomic │
│ 12. PAGE WRAPPERS     ──► Global layouts, providers, metadata roots    │
│ 13. RESPONSIVE MODEL  ──► Media query tokens / mobile-first conventions│
│ 14. ACCESSIBILITY     ──► jsx-a11y / Radix primitives / ARIA utilities │
│ 15. MOTION SYSTEM     ──► Framer Motion / Motion One / Pure CSS Keyframes│
│ 16. TEST RUNNERS      ──► Playwright / Vitest / Jest / Storybook       │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Existing Design System Maturity Evaluation

Sloppi classifies the project's existing design infrastructure into one of four maturity tiers:

| Maturity Tier | Observed Codebase Characteristics | Sloppi Implementation Strategy |
| :--- | :--- | :--- |
| **Tier 1: No Design System** | Raw HTML/CSS, inline styles, arbitrary utility classes scattered with no central variables. | **Establish Greenfield Tokens**: Inject canonical CSS custom properties (`--color-canvas`, `--font-display`, etc.) in global stylesheet. |
| **Tier 2: Weak Design System** | Partial CSS variables (`:root { --blue: #00f }`), inconsistent naming, mixed pixel sizes. | **Consolidate & Map**: Refactor existing variables into semantic roles without breaking existing components. |
| **Tier 3: Established Design System** | Organized tokens (e.g. Tailwind config, CSS variables), standard button/input primitives. | **Respect & Extend**: Map Sloppi design decisions directly to existing token names. Do not create parallel systems. |
| **Tier 4: Mature Design System** | Published NPM token package, strict lint rules, multi-tier semantic tokens, component library. | **Strict Native Integration**: Author components strictly using the existing library primitives and token wrappers. |

### The Non-Duplication Mandate
> **Rule**: If a project already has a functional CSS variable `--background` or a Tailwind class `bg-background`, Sloppi must use it rather than creating a competing `--color-canvas` variable. Never create duplicate, parallel token systems.

---

## 3. Inspection Output Schema

The agent records its findings in the implementation plan or scratch log before writing code:

```markdown
### Project Inspection Log
- **Framework & Runtime**: Next.js 15 (App Router, TypeScript strict)
- **Styling Architecture**: Tailwind CSS v4 + Vanilla CSS Custom Properties
- **Component Primitives**: Radix UI Primitives (`@radix-ui/react-dialog`, `@radix-ui/react-dropdown-menu`)
- **Icon Infrastructure**: `lucide-react` (v0.450.0)
- **Motion System**: Pure CSS transitions + `@media (prefers-reduced-motion)`
- **Design System Maturity**: Tier 3 (Established - Tailwind semantic theme config exists)
- **Adaptation Strategy**: Map Sloppi `DESIGN.md` tokens directly into `app/globals.css` `:root` variables and extend `tailwind.config.ts`.
```
