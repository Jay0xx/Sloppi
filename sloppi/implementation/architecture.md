# Sloppi Implementation Architecture & Dependency Ordering

Implementation Architecture defines the structural build order and abstraction layers through which design decisions become production frontend code.

Building an interface without understanding layer dependencies leads to chaotic spaghetti code, broken styles, and circular component imports. Sloppi establishes a strict, bottom-up dependency ordering.

---

## 1. The 5-Layer Dependency Hierarchy

Implementation must progress sequentially through five systemic layers:

```
┌────────────────────────────────────────────────────────────────────────┐
│                        5. PAGES & ROUTE LAYOUTS                        │
│   Full page composition, dynamic routing, metadata & layout frames     │
├────────────────────────────────────────────────────────────────────────┤
│                        4. NARRATIVE SECTIONS                           │
│   Composed chapters (Hero, ArchitectureDiff, SpecGrid, ActionClosure)   │
├────────────────────────────────────────────────────────────────────────┤
│                        3. DOMAIN COMPONENTS                            │
│   Self-contained functional widgets (CodeTerminal, NavMenu, Pricing)   │
├────────────────────────────────────────────────────────────────────────┤
│                        2. COMPONENT PRIMITIVES                         │
│   Accessible UI building blocks (Button, Input, Badge, Dialog, Surface)│
├────────────────────────────────────────────────────────────────────────┤
│                        1. DESIGN TOKENS                                │
│   Mathematical variables (Colors, Typography, Spacing, Radii, Shadows) │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Layer Definitions & Architectural Boundaries

### Layer 1: Design Tokens (`globals.css` / `:root`)
- **Role**: Mathematical foundation of the design system.
- **Contents**: Raw hex mappings, semantic color aliases, type scales, spatial steps, corner radii, and easing bezier curves.
- **Rule**: Tokens contain **zero component markup or layout logic**.

### Layer 2: Component Primitives (`components/ui/` / `primitives/`)
- **Role**: Low-level, domain-agnostic UI elements.
- **Examples**: `Button`, `Input`, `Badge`, `Card`, `Switch`, `Tooltip`, `Dialog`.
- **Rule**: Primitives accept design tokens and implement complete accessibility (`:focus-visible`, ARIA, keyboard navigation). They contain **no hardcoded business copy**.

### Layer 3: Domain Components (`components/` / `widgets/`)
- **Role**: Purpose-built, functional combinations of primitives.
- **Examples**: `InteractiveTerminal`, `TelemetryHUD`, `ComparisonMatrix`, `PricingTierCard`.
- **Rule**: Domain components encapsulate interactive state, copy data bindings, and specific layouts.

### Layer 4: Narrative Sections (`sections/` / `features/`)
- **Role**: Full-width narrative chapters that pass the Section Justification test.
- **Examples**: `HeroSplitSection`, `ArchitectureDeepDiveSection`, `BenchmarkSection`, `FinalActionSection`.
- **Rule**: Sections govern vertical rhythm, section ground alternation (`--color-canvas` vs `--color-canvas-alt`), and responsive column transformations.

### Layer 5: Pages & Layouts (`app/` / `pages/` / `layouts/`)
- **Role**: Top-level page assemblies that orchestrate sections into a coherent cognitive journey.
- **Contents**: Semantic document landmarks (`<header>`, `<main>`, `<footer>`), SEO metadata, and global state providers.

---

## 3. Dependency Build Order in Practice

```
1. Write/Update Token Stylesheet  ──► (globals.css / theme.ts)
2. Build UI Primitives            ──► (Button, Card, Badge)
3. Build Domain Widgets           ──► (TerminalREPL, SpecTable)
4. Compose Narrative Sections     ──► (HeroSection, BenchmarkSection)
5. Assemble Page Container        ──► (page.tsx / index.html)
6. Add Responsive Refinements     ──► (Mobile transformations)
7. Audit & Validate               ──► (WCAG contrast & anti-drift checks)
```
