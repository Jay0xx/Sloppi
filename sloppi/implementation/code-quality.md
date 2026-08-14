# Sloppi Code Quality Standards & Anti-Slop Audit

Code Quality in Sloppi represents the intersection of technical maintainability, semantic accessibility, and visual token fidelity.

A coding agent must produce clean, readable, robust code that respects framework conventions, adheres to `DESIGN.md` contracts, and eliminates implementation slop.

---

## 1. The 15 Anti-Slop Implementation Failure Flags

During code generation and review, the agent scans for fifteen implementation failure patterns:

```
[ Frontend Implementation Review ]
        │
        ├──────► FLAG 1: Generic Component Library Default (Replacing intentional design with stock library look)
        ├──────► FLAG 2: Arbitrary Unmapped Colors (Scattering raw hex codes #3b82f6 instead of tokens)
        ├──────► FLAG 3: Arbitrary Spacing (Using margin: 37px outside the 4px/8px spatial scale)
        ├──────► FLAG 4: Inconsistent Corner Radii (Mixing 4px, 19px, and 30px radii on adjacent cards)
        ├──────► FLAG 5: Duplicated Micro-Components (Creating single-use wrappers like HeroSubtitle)
        ├──────► FLAG 6: Excessive Premature Abstraction (Creating monolithic configurable mega-components)
        ├──────► FLAG 7: Unnecessary Package Dependencies (Installing 35KB JS libraries for 1-line CSS transitions)
        ├──────► FLAG 8: Decorative Polish Trap (Adding rainbow mesh gradients and glowing orbs to hide weak design)
        ├──────► FLAG 9: Inconsistent Design Tokens (Using different token names for the same concept)
        ├──────► FLAG 10: Desktop-Only Layouts (Causing horizontal overflow on mobile viewports <640px)
        ├──────► FLAG 11: Inaccessible Keyboard Navigation (Removing focus outlines with outline: none)
        ├──────► FLAG 12: Silent Design Drift (Modifying visual layout without updating DESIGN.md)
        ├──────► FLAG 13: Placeholder Copy in Production (Leaving "Lorem ipsum" or generic buzzwords)
        ├──────► FLAG 14: Fabricated Social Proof (Rendering fake customer quotes or unauthorized logos)
        └──────► FLAG 15: Low-Contrast Touch Targets (Buttons smaller than 44px on mobile screens)
```

---

## 2. Framework Agnosticism & Clean Conventions

Sloppi principles apply identically across any frontend framework:

### React / Next.js
- Co-locate styles using clean CSS modules, Tailwind semantic classes, or CSS variables.
- Never write monolithic 800-line single-file components.
- Ensure strict TypeScript typing for all component props.

### Vue / Nuxt
- Use `<script setup lang="ts">` and scoped `<style>` blocks bound to root CSS variables.
- Maintain semantic slot structures for compound components.

### Svelte / SvelteKit
- Leverage Svelte's native scoped styles and reactive stores.
- Use clean semantic HTML without wrapper `<div>` soup.

### Vanilla HTML / Modern CSS
- Use standard semantic landmarks (`<header>`, `<main>`, `<nav>`, `<article>`, `<footer>`).
- Use CSS custom properties in `:root` and native CSS Grid/Flexbox.

---

## 3. The Implementation Decision Log

When implementation requires a deliberate deviation from `DESIGN.md` (e.g. browser compatibility workaround, sub-pixel alignment adjustment), record it in the Implementation Log:

```markdown
### Implementation Decision Log
- **Deviation Category**: [Intentional | Necessary | Temporary]
- **Component / Section**: `src/components/InteractiveTerminal.tsx`
- **Original DESIGN.md Rule**: `min-height: 480px`
- **Implemented Modification**: `min-height: clamp(380px, 50vh, 560px)`
- **Technical Rationale**: Prevents terminal code from overflowing the initial viewport on 13" laptop screens (1280x800).
- **DESIGN.md Update Required**: Yes (Updated Section 7 in DESIGN.md).
```
