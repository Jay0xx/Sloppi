# Sloppi Typography & Text Measure Audit

The Typography Audit evaluates whether rendered typography exhibits disciplined mathematical scaling, ergonomic reading measures, and optical harmony aligned with the project's Design Thesis.

---

## 1. The 8-Point Typography Audit Checklist

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. MATHEMATICAL TYPE SCALE     ──► Clear size progression across tokens│
│                                    (61px → 49px → 39px → 31px → 16px). │
│ 2. LEADING INVERSION RULE      ──► Tight leading on display type (0.95)│
│                                    vs. open leading on body copy (1.60)│
│ 3. TRACKING / LETTER-SPACING   ──► Negative tracking on display type   │
│                                    (-0.025em) vs. positive on tags.   │
│ 4. STRICT LINE MEASURE         ──► Body copy strictly 45–75 characters │
│                                    (max-width: 65ch;).                 │
│ 5. OPTICAL LINE BALANCING      ──► text-wrap: balance applied to H1/H2 │
│                                    (zero single-word orphan lines).    │
│ 6. TABULAR NUMERIC FIGURES     ──► font-variant-numeric: tabular-nums  │
│                                    on all financial and metric tables. │
│ 7. FONT PAIRING INTEGRITY      ──► Max 2–3 curated font families with  │
│                                    explicit system fallback chains.    │
│ 8. FLUID CLAMP SCALING         ──► Smooth clamp() scaling between      │
│                                    mobile (32px) and desktop (61px).   │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Typography Deficiency Catalog & Fixes

| Typographic Flaw | Diagnostic Symptom | Severity | Sloppi Remediation |
| :--- | :--- | :--- | :--- |
| **Runaway Body Line Length** | Paragraph lines stretch 120+ characters across wide displays, causing eye fatigue. | **HIGH** | Apply `max-width: 65ch;` to all body copy containers. |
| **Awkward Headline Orphans** | A 12-word display headline drops a single short word (*"now."*) onto its own line. | **MEDIUM** | Apply `text-wrap: balance;` to display headlines or manually insert non-breaking spaces (`&nbsp;`). |
| **Loose Display Leading** | A 56px hero headline has default 1.50 line-height ($84\text{px}$), creating disconnected floating lines. | **MEDIUM** | Compress display leading to `line-height: 0.95`–`1.05` and apply `letter-spacing: -0.025em`. |
| **Jittery Data Tables** | Numbers in a live telemetry table shift horizontal alignment on re-renders. | **MEDIUM** | Set `font-family: var(--font-mono);` and `font-variant-numeric: tabular-nums;`. |
| **Oversized Low-Impact Headings**| A minor section subhead uses massive 48px type, competing with the primary hero title. | **MEDIUM** | Realign heading to semantic token scale (`heading-md` $31\text{px}$ or `heading-sm` $25\text{px}$). |
