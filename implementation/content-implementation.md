# Sloppi Content Implementation & Data Separation

Content Implementation governs how domain messaging, technical specifications, and narrative copy are structured inside the codebase.

A coding agent must avoid two extremes:
1. **The Hardcoded Spaghetti Anti-Pattern**: Burying lengthy, important marketing copy and benchmark numbers directly inside nested 20-level JSX tags.
2. **The Over-Engineering Anti-Pattern**: Building a complex headless CMS, database, or external GraphQL pipeline for a simple static marketing landing page.

---

## 1. The Separation of Concerns Triad

Where appropriate, Sloppi structures code into three distinct concerns:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. CONTENT LAYER       ──► Structured data models, domain copy, specs, │
│                            benchmarks, and feature matrices.           │
│                            (e.g., `src/data/benchmarks.ts`)            │
├────────────────────────────────────────────────────────────────────────┤
│ 2. PRESENTATION LAYER  ──► Layout containers, typography tokens, CSS   │
│                            classes, and spatial arrangement.           │
│                            (e.g., `src/sections/BenchmarkSection.tsx`) │
├────────────────────────────────────────────────────────────────────────┤
│ 3. BEHAVIOR LAYER      ──► State handlers, tab switching, copy-to-     │
│                            clipboard listeners, and keyboard traps.    │
│                            (e.g., `src/components/CopyButton.tsx`)     │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Structured Content Data Contracts (Example)

For structured, data-heavy sections (e.g. comparison tables, benchmarks, interactive tabs), define typed data contracts:

```typescript
// src/data/comparison.ts

export interface ComparisonRow {
  parameter: string;
  category: 'performance' | 'architecture' | 'operations';
  aurakv: string | boolean;
  redis: string | boolean;
  notes?: string;
}

export const COMPARISON_DATA: ComparisonRow[] = [
  {
    parameter: 'Concurrency Model',
    category: 'architecture',
    aurakv: 'Multi-threaded Lock-Free (io_uring)',
    redis: 'Single-Threaded Event Loop',
    notes: 'Eliminates CPU core under-utilization under high thread counts.'
  },
  {
    parameter: 'Memory Overhead / Key',
    category: 'performance',
    aurakv: '12 bytes (Compressed SIMD Index)',
    redis: '56 bytes (dictEntry struct)',
    notes: 'Reduces total AWS RAM instance footprint by ~78%.'
  },
  {
    parameter: 'Cold-Start Warmup Time',
    category: 'operations',
    aurakv: '< 150ms (NVMe Memory-Mapped)',
    redis: '4–8 mins (RDB / AOF Replay)',
    notes: 'Instant node recovery during autoscaling deployments.'
  }
];
```

---

## 3. When to Data-Drive vs. When to Inline

| Content Category | Implementation Strategy | Rationale |
| :--- | :--- | :--- |
| **Display Hero Headline & Subhead** | Inline within Section Component | Single-instance high-gravity anchor; benefit from co-located semantic typography classes. |
| **Comparative Specification Tables** | Separate Typed Data Constant (`data/`) | Multi-row parameter grids are easier to audit and update without risking CSS syntax breakage. |
| **Interactive Code Snippets** | Separate Monospace Data Store (`data/`) | Preserves clean indentation and language metadata for syntax highlighters. |
| **Section Narrative Chapters** | Inline within Section Container | Direct visual relationship between layout containers and paragraph line-length constraints. |
