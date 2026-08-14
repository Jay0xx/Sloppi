# Sloppi Typography Architecture

Typography is the primary structural backbone of user interface design. In Sloppi, typography is not merely styling applied to text; it defines spatial hierarchy, reading pace, cognitive effort, and brand authority.

A coding agent must never default to Inter, Roboto, or system-ui without reasoning. Conversely, an agent must not avoid standard fonts out of superficial novelty. The operative question is always: **Why this font for this specific product?**

---

## 1. Font Selection Methodology

Every font family selected for a project must have an explicit rationale connecting it to the product's operational reality:

```
[ Product Operational Context ] ──► [ Personality Axes ] ──► [ Font Pairing Rationale ] ──► [ Fallback Stack ]
```

### Font Selection Criteria
- **Personality Alignment**: Does the typeface's stroke modulation, geometric structure, or serifs support the Design Thesis?
- **Optical Legibility at Scale**: Does the body font perform cleanly at $12\text{px}–16\text{px}$ in low-contrast environments?
- **Tabular / Numeric Support**: For data-rich tools, does the font include tabular figures (`tnum`) where all numbers share identical widths?
- **Character Set & Weights**: Does the family provide necessary weights without artificial browser faux-bolding?
- **Fallback Stacks**: Explicit, robust fallback chains (e.g., `'Aeonik Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`).

---

## 2. The 3 Functional Type Categories

A project system defines at most three functional font roles:

### 1. Display & Heading Typeface
- **Role**: Visual entry points, hero punchlines, major section anchors (H1, H2).
- **Attributes**: High character, expressive letterforms, distinct optical weight.
- **Rule**: Never use a high-character display font for dense body copy.

### 2. UI & Body Typeface
- **Role**: Sustained reading, interactive button controls, input fields, form labels, card copy.
- **Attributes**: Neutral grotesque or clean humanist sans with open counters and large x-height.

### 3. Monospace & Data Typeface
- **Role**: Code blocks, terminal logs, tabular telemetry, numerical values, timestamps, technical tags.
- **Attributes**: Strict monospaced character widths, distinct zero/O and 1/l glyphs.

---

## 3. Mathematical Modular Scale Architecture

Sloppi structures type scales mathematically rather than picking arbitrary pixel numbers. The agent selects a scale multiplier based on the product's required information density:

- **Minor Third ($1.200$)**: Recommended for high-density tools, code editors, and data analytics dashboards where vertical space is constrained.
- **Major Third ($1.250$)**: Recommended for balanced SaaS workflows and standard web applications.
- **Perfect Fourth ($1.333$)**: Recommended for spacious editorial layouts, luxury marketing, and high-impact visual storytelling.

### Complete Modular Type Scale (Major Third 1.250 Example, Base 16px)

| Scale Token | Font Size | Weight | Line-Height | Letter-Spacing | Intended Semantic Role |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `--font-display-2xl` | `61px / 3.81rem` | 800 | `0.95` | `-0.030em` | Hero visual anchor wordmark |
| `--font-display-xl` | `49px / 3.05rem` | 700 | `1.02` | `-0.025em` | Page main titles (H1) |
| `--font-heading-lg` | `39px / 2.44rem` | 600 | `1.12` | `-0.020em` | Section primary headers (H2) |
| `--font-heading-md` | `31px / 1.95rem` | 600 | `1.20` | `-0.015em` | Subsection & feature headers (H3) |
| `--font-heading-sm` | `25px / 1.56rem` | 600 | `1.30` | `-0.010em` | Card titles, modal headers (H4) |
| `--font-body-lg` | `20px / 1.25rem` | 400 | `1.50` | `-0.005em` | Lead paragraphs, hero subtext |
| `--font-body` | `16px / 1.00rem` | 400 | `1.60` | `normal` | Standard body copy, form inputs |
| `--font-body-sm` | `13px / 0.81rem` | 500 | `1.45` | `+0.010em` | Buttons, navigation links, table cells |
| `--font-caption` | `11px / 0.69rem` | 500 | `1.40` | `+0.030em` | Uppercase labels, status tags, timestamps |

---

## 4. Proportional Line-Height & Letter-Spacing Rules

Sloppi enforces strict mathematical relationships between font size, leading, and tracking:

### The Leading Inversion Rule
- **Large Display Type ($48\text{px}+$) requires Compressed Leading ($0.85–1.05$)**: As type size increases, standard $1.5$ leading creates cavernous gaps between stacked words, breaking visual unity. Compressed leading allows large words to function as sculpted visual objects.
- **Body Type ($14\text{px}–18\text{px}$) requires Generous Leading ($1.55–1.65$)**: Small text requires breathing space between ascenders and descenders to prevent eye fatigue during multi-line reading.
- **Code & Tabular Data ($12\text{px}–14\text{px}$) requires Uniform Leading ($1.40–1.50$)**: Keeps row heights consistent across multi-line terminal outputs and side-by-side diffs.

### The Tracking Compensation Rule
- **Negative Tracking on Large Headings (`-0.02em` to `-0.035em`)**: Compensates for optical letter spreading at large scales.
- **Positive Tracking on Small Uppercase Labels (`+0.02em` to `+0.05em`)**: Gives uppercase caps and metadata badges breathing room for rapid optical recognition.

---

## 5. Text Measure & Optical Line Balancing

- **Optimal Reading Measure**: Constrain paragraph text between 45 and 75 characters per line (`max-width: 65ch`). Lines exceeding 80 characters cause reader disorientation when returning to the next line.
- **Headline Balancing**: Apply `text-wrap: balance` to all H1, H2, and H3 headers to eliminate typographic orphans (single words wrapping onto their own line).

---

## 6. Responsive Typography Scaling

Do not arbitrarily reduce body font size on mobile devices ($16\text{px}$ must remain the baseline for readable mobile text to prevent unwanted browser auto-zooming).

Instead, scale display headings down using CSS `clamp()` or discrete breakpoint tokens:
- Desktop H1: `49px` / `3.05rem`
- Tablet H1: `39px` / `2.44rem`
- Mobile H1: `31px` / `1.95rem`
- Formula: `clamp(1.95rem, 4vw + 1rem, 3.05rem)`
