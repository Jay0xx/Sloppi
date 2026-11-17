# Sloppi Component Strategy & Abstraction Boundaries

Component Strategy defines how UI elements are classified, extracted, and composed across an application.

A frequent failure mode of AI coding agents is **Premature Micro-Abstraction**—creating twenty trivial single-line wrapper components (`HeroTitle`, `HeroSubtitle`, `HeroBadge`, `HeroParagraph`, `HeroIconWrapper`) that provide zero reusable value and obscure DOM hierarchy.

---

## 1. The 5-Tier Component Taxonomy

Sloppi enforces a disciplined distinction across five component classifications:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. PRIMITIVE           ──► Domain-agnostic UI base element             │
│                            (e.g., Button, Input, Badge, Surface)       │
│ 2. COMPONENT           ──► Self-contained functional unit              │
│                            (e.g., CodeTerminal, TelemetryBadge)        │
│ 3. COMPOUND COMPONENT  ──► Coordinated multi-element subsystem         │
│                            (e.g., Tabs.Root + Tabs.Trigger + Tabs.Panel│
│                             or Accordion.Item + Accordion.Trigger)     │
│ 4. NARRATIVE SECTION   ──► Contextual chapter container                │
│                            (e.g., HeroSplitSection, ComparisonSection) │
│ 5. PAGE / ROUTE        ──► Top-level orchestrator                      │
│                            (e.g., LandingPage, DocumentationPage)      │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. The Core Rule: Repetition Precedes Abstraction

Sloppi enforces the principle that **abstraction must follow verified repetition, not speculative possibility**:

$$\text{Verified Repetition} \longrightarrow \text{Abstraction}$$

$$\text{Speculative Possibility} \centernot\longrightarrow \text{Abstraction}$$

### ❌ What NOT to Abstract (Micro-Component Bloat)
Do not create single-use wrapper components for standard HTML elements:
- ❌ `<HeroHeading>` (just use `<h1 className="text-display-xl font-bold tracking-tight">`)
- ❌ `<HeroParagraph>` (just use `<p className="text-body-lg text-secondary max-w-[65ch]">`)
- ❌ `<HeroContainer>` (just use `<section className="py-24 px-6 max-w-7xl mx-auto">`)
- ❌ `<BadgeWrapper>` (just use `<span className="inline-flex items-center gap-1.5 ...">`)

### ✅ What TO Abstract
Create reusable abstractions only when:
1. **Behavioral Complexity**: The element manages complex interactive states, keyboard listeners, focus traps, or ARIA attributes (`Dialog`, `Dropdown`, `Tabs`, `CommandPalette`).
2. **Verified Multi-Instance Reuse**: The element is rendered across 3+ distinct sections with identical styling rules (`Button`, `Badge`, `CopyButton`, `SpecRow`).
3. **Encapsulated Domain Logic**: The component manages internal timers, streaming websockets, or clipboard events (`InteractiveTerminal`, `LiveTelemetryHUD`).

---

## 3. Visual Similarity vs. Semantic Identity

> **Critical Rule**: Visual similarity does not automatically mean semantic identity.

If two UI boxes share identical background colors and border radii:
- Box A is a **Product Feature Card** with a title, body, and hover lift.
- Box B is a **System Telemetry Panel** with tabular figures and a live status dot.

**Do not merge them into a generic `<UniversalBox>` component.** Merging semantically distinct entities creates fragile prop-drilling monsters (`<UniversalBox isTelemetry={true} showStatusDot={true} ...>`). Keep them distinct.

---

## 4. Compound Component Architecture

For complex, coordinated UI primitives (e.g. Tabs, Accordions, Dropdowns), prefer compound component architectures that expose composable slots rather than rigid configuration objects:

```tsx
// ✅ Composable, readable, accessible
<Tabs.Root defaultValue="typescript">
  <Tabs.List aria-label="Code examples">
    <Tabs.Trigger value="typescript">TypeScript</Tabs.Trigger>
    <Tabs.Trigger value="go">Go</Tabs.Trigger>
    <Tabs.Trigger value="python">Python</Tabs.Trigger>
  </Tabs.List>
  <Tabs.Content value="typescript">
    <CodeBlock language="ts" code={tsCode} />
  </Tabs.Content>
</Tabs.Root>

// ❌ Fragile monolithic configuration prop anti-pattern
<Tabs tabs={[{ label: 'TypeScript', content: '...' }]} />
```

---

## 5. Discovering, Installing & Adapting Registry Components

When an app needs accessible UI primitives or compatible domain components (never replacing core bespoke creative direction with generic boilerplate):

1. **Discover & Inspect**: Use **`shadcn` MCP** (`search_items_in_registries`, `view_items_in_registries`) for `@shadcn` or compatible registries (such as `https://oxyn.space/r/registry.json`), **`Dissolve` MCP** (`list_variants`, `get_variant`) for Expo/RN particle components, or **`Context7`** for up-to-date package APIs.
2. **Install Into the Target App**: Install via the app's existing package manager (`pnpm`, `npm`, `yarn`, `bun`, `npx expo install`, or `npx react-native-dissolve add <component>`) and review generated files and peer/CSS/provider prerequisites ([dependency-policy.md](dependency-policy.md)).
3. **Strip Demo Chrome & Bind Tokens**: Map copied component styles to the app's semantic tokens (`--color-*`, `--radius-*`, typography, NativeWind `@theme inline`) and wire real state/accessibility (`aria-busy`, `role="status"`, `:focus-visible`, reduced motion).
4. **Review Before Shipping**: Run **`web-design-guidelines`** for accessibility/interaction compliance and **`vercel-react-best-practices`** for React/Next.js performance patterns when working in React.
