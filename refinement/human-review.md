# Sloppi Human Review Boundaries & Strategic Alignment

Human Review defines the explicit threshold where algorithmic design rules end and human strategic judgment begins.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   THE HUMAN REVIEW PRINCIPLE                           │
│                                                                        │
│ "Human review must NEVER replace visual QA or basic design reasoning.   │
│  The agent executes its full audit, resolves blockers, and presents    │
│  targeted strategic decisions with clear trade-offs, rather than asking│
│  vague open-ended questions like 'How does this look?'"                │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 1. When Human Review is Strictly Required

The agent pauses the automated refinement loop and requests human intervention under six specific conditions:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. BRAND DIRECTION AMBIGUITY   ──► Choosing between two fundamentally  │
│                                    distinct personality axes (e.g.,    │
│                                    Stark Minimalist vs. Dense HUD).    │
│ 2. STRATEGIC POSITIONING       ──► Product messaging trade-offs        │
│                                    (Enterprise Security vs. Dev Speed).│
│ 3. LEGAL / COMPLIANCE UNCERTAINTY► Unverified benchmark figures or     │
│                                    unauthorized partner brand logos.   │
│ 4. MAJOR ARCHITECTURAL PIVOT   ──► Deciding whether to restructure     │
│                                    single-page flow into multi-route.  │
│ 5. EQUALLY VIABLE DIRECTIONS   ──► Research supports both an Editorial │
│                                    and a Live Terminal hero model.     │
│ 6. IRRECONCILABLE CONSTRAINTS  ──► Design requirement conflicts with    │
│                                    strict enterprise accessibility.    │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Anatomy of a High-Quality Human Review Request

| ❌ Lazy, Low-Value Request | ✅ High-Precision Sloppi Review Request |
| :--- | :--- |
| *"What do you think of the new hero section?"* | *"We have resolved all accessibility and mobile responsive blockers. Two viable Hero paradigms remain supported by our research: <br>• **Option A (Interactive REPL)**: Emphasizes instant developer utility with live CLI execution.<br>• **Option B (Editorial Benchmark)**: Emphasizes enterprise trust with verified p99 latency tables.<br>Which direction aligns closer with your current Q3 launch priority?"* |
| *"Is this color okay?"* | *"The secondary brand cyan passes WCAG AAA contrast (8.2:1), but gives the interface a more consumer-tech feel. An alternative steel-slate maintains equal contrast with higher enterprise gravitas. Do you prefer Option A (Cyan) or Option B (Steel-Slate)?"* |

---

## 3. Human Approval Protocol

1. **Pre-Audit First**: The agent must complete Steps 10 and 11 (Visual QA and Anti-Slop Audit) before presenting work for review.
2. **Present Rendered Artifacts**: Provide exact file paths, component selectors, and screenshot references.
3. **State Clear Recommendation**: State the agent's recommended default choice based on the Design Thesis and research evidence.
