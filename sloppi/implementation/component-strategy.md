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
