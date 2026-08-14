# Sloppi Content & Copywriting Strategy

In Sloppi, **content is an inseparable layer of visual design**.

Coding agents frequently treat copywriting as an afterthought, populating high-effort layouts with hollow buzzwords ("Empower your seamless next-gen synergy") or lazy placeholder text ("Lorem ipsum dolor sit amet"). This produces semantic and visual slop:
- Placeholder text distorts typography line wrapping, optical balance, and vertical rhythm.
- Vague buzzwords destroy user trust and fail to communicate the actual product utility.
- Generic button text ("Click Here", "Get Started") offers zero contextual value.

---

## 1. The Sloppi Anti-Slop Copywriting Rules

### Rule 1: Replace Abstract Buzzwords with Plain Technical Verbs
| Slop Buzzword | Sloppi Intentional Replacement |
| :--- | :--- |
| "Supercharge your database workflow" | "Run automated zero-downtime schema migrations on Postgres" |
| "Seamless integration across platforms" | "Native SDKs for TypeScript, Python, Go, and Rust" |
| "Intelligent next-gen analytics" | "Sub-second SQL queries across 100M+ events with ClickHouse" |
| "Elevate your team collaboration" | "Real-time multiplayer canvas with CRDT conflict resolution" |
| "Unleash the power of AI" | "Fine-tuned Llama-3 model running locally on your hardware" |

### Rule 2: Ground Copy in Believable, Domain-Specific Realities
- When creating UI mockups, populate them with authentic domain data:
  - For an observability dashboard: show real metric names (`http_req_duration_ms{status="500"}`, `p99 = 42ms`), authentic timestamp formats (`2026-08-14T22:45:12Z`), and realistic log lines.
  - For a financial app: show believable currency formatting (`$14,285.50 USD`), realistic settlement statuses (`Cleared · ACH Direct`), and authentic transaction metadata.
  - For a developer tool: write syntactically valid code snippets, actual shell commands (`curl -X POST https://api.sloppi.dev/v1/critique`), and realistic JSON responses.

### Rule 3: Write Outcome-Explicit Action Copy
Every button and link label must communicate **what will happen immediately upon interaction**:
- ❌ "Submit" → ✅ "Create Free Team Account"
- ❌ "Learn More" → ✅ "Read Migration Architecture Guide"
- ❌ "Download" → ✅ "Download macOS Universal Binary (v2.4.0)"
- ❌ "Explore" → ✅ "View Live Interactive Demo"

---

## 2. Typographic Line Length & Balancing

Copywriting directly impacts visual composition:
- **Display Headlines**: Keep under 10–12 words. Use CSS `text-wrap: balance` to prevent awkward typographic orphans.
- **Body Paragraphs**: Keep line lengths between 45 and 75 characters (`max-w-[65ch]`). Lines exceeding 85 characters cause eye fatigue; lines under 35 characters fragment reading flow.
- **List Items & Feature Descriptions**: Keep concise (15–25 words per item) to maintain vertical alignment across columns.

---

## 3. Micro-Copy Assurance Elements

High-converting interfaces reduce cognitive friction with adjacent assurance copy placed next to primary actions:
- *"No credit card required · 14-day full access"*
- *"Open-source Apache 2.0 · Self-hostable via Docker"*
- *"SOC2 Type II certified · End-to-end encrypted"*
- *"Integrates in 3 lines of code"*
