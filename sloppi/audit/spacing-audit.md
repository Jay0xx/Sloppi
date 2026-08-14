# Sloppi Spacing & Spatial Cadence Audit

The Spacing Audit inspects the mathematical consistency, vertical cadence, and density alignment of all margins, padding, and layout gaps across the rendered interface.

---

## 1. The 6-Point Spacing Audit Checklist

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. BASELINE SCALE FIDELITY     ──► All margins, padding, and gaps map  │
│                                    strictly to the 4px/8px token scale.│
│ 2. ZERO MAGIC PIXEL NUMBERS    ──► Zero arbitrary values (e.g., 37px,  │
│                                    53px, 19px) hardcoded in CSS.       │
│ 3. DENSITY MODE ALIGNMENT      ──► Matches the project density model   │
│                                    (Sparse vs. Moderate vs. Dense HUD).│
│ 4. SECTION CADENCE MODULATION  ──► Dynamic vertical padding variation  │
│                                    (48px ↔ 96px ↔ 128px).              │
│ 5. INTERNAL CONTAINER RATIOS   ──► Card padding is proportional to     │
│                                    internal typography and child gaps. │
│ 6. RESPONSIVE COMPRESSION      ──► Desktop 96px gaps gracefully scale  │
│                                    to 48px/64px on mobile viewports.   │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Spacing Deficiency Catalog & Fixes

| Spacing Flaw | Diagnostic Symptom | Severity | Sloppi Remediation |
| :--- | :--- | :--- | :--- |
| **Magic Number Pollution** | CSS contains arbitrary hardcoded values (`margin-top: 29px; gap: 17px;`). | **MEDIUM** | Map all values to canonical space tokens (`var(--space-6)` $24\text{px}$, `var(--space-8)` $32\text{px}$). |
| **Monotone Vertical Cadence** | Every section on the page has identical 64px padding, creating a flat visual scroll. | **MEDIUM** | Modulate vertical padding: high-gravity hero ($96\text{px}$–$128\text{px}$), compact telemetry ($48\text{px}$). |
| **Internal Card Suffocation** | A 3-column feature card has dense text packed against borders with only 8px padding. | **MEDIUM** | Increase card internal padding to `var(--space-6)` ($24\text{px}$) or `var(--space-8)` ($32\text{px}$). |
| **Unbounded Horizontal Stretch**| On wide screens ($1920\text{px}$), content stretches edge-to-edge with no container max-width. | **HIGH** | Wrap content in a centered container (`max-width: 1200px / 1440px; margin: 0 auto;`). |
| **Mobile Padding Blowout** | Desktop 128px section margins remain uncompressed on mobile, wasting entire screens. | **MEDIUM** | Apply responsive spacing media queries (`py-12 md:py-24 lg:py-32`). |
