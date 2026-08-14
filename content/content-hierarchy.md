# Sloppi Content & Attention Hierarchy

Content Hierarchy defines the disciplined visual, sequential, and cognitive order in which information is delivered to the user.

A fundamental flaw in AI-generated web interfaces is **"Equal Loudness Syndrome"**—where every heading, card, badge, button, and banner screams with identical visual intensity. When every element claims maximum importance, the user experiences cognitive overload, scanning friction, and zero memorable takeaways.

```
┌────────────────────────────────────────────────────────────────────────┐
│                        THE ATTENTION BUDGET                            │
│                                                                        │
│ In any single viewport, the human eye can process exactly ONE          │
│ primary focal point without friction. Sloppi allocates visual energy   │
│ with mathematical discipline across 7 communicative tiers.             │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 1. The 7 Tiers of Content Hierarchy

Sloppi structures all page content across seven distinct communicative tiers, each paired with an exact typographic weight, spatial role, and visual contrast level:

```
┌────────────────────────────────────────────────────────────────────────┐
│ TIER 1: PRIMARY HOOK / CORE VALUE (Attention Priority 1)              │
│ Role: The single most critical assertion or takeaway on the page.      │
│ Typographic Scale: Display XL / 2XL (40px–64px), tight leading (0.95)  │
│ Optical Contrast: 100% Foreground Contrast (AAA)                       │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 2: SUPPORTING EXPLANATION (Attention Priority 2)                 │
│ Role: 1–2 precise sentences clarifying the hook in technical terms.   │
│ Typographic Scale: Body Large (18px–20px), relaxed leading (1.50)     │
│ Optical Contrast: Secondary Contrast (AA), text-secondary             │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 3: EVIDENTIARY PROOF / DEMONSTRATION (Attention Priority 3)       │
│ Role: Live interactive REPL, terminal CLI, architecture SVG, or data. │
│ Visual Container: High-contrast bounded surface, code styling, shadow  │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 4: PRIMARY ACTION (Conversion Trigger)                            │
│ Role: The immediate next step for the high-intent user.               │
│ Visual Weight: var(--color-brand) solid fill, outcome-explicit label   │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 5: DEEP EXPLANATORY MECHANICS                                     │
│ Role: Feature deep-dives, sequential process steps, comparison tables. │
│ Typographic Scale: Heading MD (24px–32px) + Body Regular (15px–16px)   │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 6: ASSURANCE & SECONDARY INFORMATION                              │
│ Role: Friction reducers (pricing limits, SLA, zero credit card, terms) │
│ Typographic Scale: Body Small (13px–14px), text-muted                  │
├────────────────────────────────────────────────────────────────────────┤
│ TIER 7: METADATA, CAPTIONS & DISCLOSURES                               │
│ Role: Hardware specs, timestamps, commit hashes, legal licensing.      │
│ Typographic Scale: Caption / Monospace (11px–12px), text-muted         │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Managing Attention Budgets: 4 Core Rules

An interface possesses a finite "attention budget." Sloppi manages this budget through strict optical governance:

### 1. The Single Focal Point Mandate
In any single viewport, **there must be exactly one primary visual focal point**:
- If the hero features an interactive live terminal or 3D canvas, the adjacent headline must act as a clean, calm typographic anchor rather than competing with pulsing animated glow effects and flashing badges.
- If the headline is the focal point (e.g. an editorial brand thesis), supporting media must sit quietly in a secondary structural container.

### 2. Typographic Contrast Ratios
Maintain unambiguous mathematical separation between consecutive hierarchy tiers:
- Display Title ($48\text{px}$) $\longrightarrow$ Supporting Subhead ($18\text{px}$) $\longrightarrow$ Body Copy ($15\text{px}$) $\longrightarrow$ Caption ($11\text{px}$).
- *Anti-Pattern*: Using $18\text{px}$ semibold for section headers and $16\text{px}$ regular for body text, creating muddy visual ambiguity.

### 3. Spatial Isolation for High-Priority Content
- If an assertion is of paramount importance (e.g., an architectural breakthrough or SOC2 security assurance), give it **generous vertical breathing room** ($96\text{px}$–$128\text{px}$ margin) rather than squeezing it into a generic card grid.

### 4. Background Elevation Modulation
- High-priority interactive elements (Tier 3) rest on elevated surface containers (`--color-surface` with subtle 1px border); secondary metadata (Tier 7) sits directly on the canvas (`--color-canvas`) with muted opacity.

---

## 3. Dynamic Scanning Pathways

Human readers scan interfaces in distinct cognitive pathways based on content structure and user intent. Sloppi aligns visual cues with these natural trajectories:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. Z-SHAPED SCANNING (High-Conversion Landing Pages)                   │
│ Top-Left (Brand Logo) ──────► Top-Right (Primary Nav Action)           │
│           │                                                            │
│           └────────────────► Center-Left (Hero Display Hook)           │
│                                      │                                 │
│                                      └────────► Bottom-Right (Hero CTA)│
│ Sloppi Rule: Place the primary conversion trigger along this diagonal. │
├────────────────────────────────────────────────────────────────────────┤
│ 2. F-SHAPED SCANNING (Documentation & Technical Editorial)             │
│ Top Line: Read full primary headline                                   │
│ Second Line: Read subhead across left-to-center                        │
│ Left Margin: Scan downwards reading bold keywords at start of lines    │
│ Sloppi Rule: Front-load high-intent technical terms at start of items. │
├────────────────────────────────────────────────────────────────────────┤
│ 3. LAYER-CAKE SCANNING (Telemetry & Operational HUDs)                  │
│ Scan horizontal section headings and metric status indicators.         │
│ Stop only at anomalous values or alert states.                         │
│ Sloppi Rule: Use high-contrast status colors strictly on metrics.      │
├────────────────────────────────────────────────────────────────────────┤
│ 4. SPOT-CHECKING SCANNING (Data Matrices & Pricing Tables)             │
│ Scan column headers ──► identify target tier ──► scan vertical column. │
│ Sloppi Rule: Highlight recommended tier with subtle border accent.     │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 4. Attention Hierarchy Emerges From Product Context

The hierarchy must never be applied as a rigid formula:
- For an **Open-Source Developer Engine**, Tier 3 (Live Terminal Code) is the primary focal point; Tier 1 (Headline) is secondary framing.
- For an **Ultra-Luxury Horology Brand**, Tier 1 (Philosophical Statement) and Tier 3 (Macro Photography) dominate; Tier 4 (Action) is restrained to a quiet boutique inquiry link.
- For a **Financial Trading Platform**, Tier 5 (Dense Order Book Data) and Tier 7 (Real-Time Latency Metadata) dominate the viewport.
