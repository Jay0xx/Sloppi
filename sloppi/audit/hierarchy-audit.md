# Sloppi Information & Visual Hierarchy Audit

The Hierarchy Audit evaluates whether an interface directs user attention with intentional optical contrast and clear cognitive priority, or suffers from **Equal Loudness Syndrome**.

---

## 1. The 5 Core Hierarchy Inquiries

When evaluating a rendered viewport, the agent must ask and answer five diagnostic questions:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. WHAT DO I NOTICE FIRST?                                             │
│    Is the primary visual focal point the most important assertion or   │
│    proof element for the user's decision?                              │
│                                                                        │
│ 2. WHAT DO I NOTICE SECOND?                                            │
│    Does the eye naturally glide to the supporting explanation or action│
│    trigger, or does it scatter randomly?                               │
│                                                                        │
│ 3. IS THE HIERARCHY INTENTIONAL?                                       │
│    Is visual prominence governed by the 7-tier Attention Budget, or did│
│    secondary elements accidentally receive dominant styling?           │
│                                                                        │
│ 4. ARE COMPETING ELEMENTS STEALING ATTENTION?                          │
│    Are flashing animated badges, high-contrast borders, or secondary   │
│    tags screaming with equal loudness alongside the main headline?     │
│                                                                        │
│ 5. DOES THE READING SCANWAY HOLD?                                      │
│    Does the page support natural scanning (Z-pattern for landing flows, │
│    F-pattern for technical docs, Layer-cake for dashboards)?           │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Hierarchy Deficiency Catalog & Audit Checks

| Hierarchy Flaw | Visual Diagnostic Indicator | Severity | Sloppi Remediation |
| :--- | :--- | :--- | :--- |
| **Equal Loudness Syndrome** | 4 distinct cards in the same viewport all use bold 24px headings, glowing badges, and bright buttons. | **HIGH** | Establish 1 dominant focal point; drop secondary card titles to 18px and secondary actions to subtle 1px outlines. |
| **Missing Visual Anchor** | Hero section contains long, low-contrast text blocks with no clear display hook or proof container. | **HIGH** | Boost primary headline to `display-2xl` ($61\text{px}$) with compressed leading ($0.95$) or introduce a high-contrast terminal. |
| **Competing Action Buttons** | Two adjacent buttons both use solid brand fill (`--color-brand`), confusing user decision flow. | **MEDIUM** | Demote secondary button to 1px outline (`1px solid var(--color-border)`) with transparent background. |
| **Muddled Heading Scale** | H2 ($22\text{px}$) is visually indistinguishable from body lead ($20\text{px}$). | **MEDIUM** | Re-align typography to the mathematical scale ($39\text{px}$ H2 $\longrightarrow$ $20\text{px}$ lead $\longrightarrow$ $16\text{px}$ body). |
| **Buried Critical Proof** | The core technical benchmark or SOC2 assurance is tucked into a tiny footnote. | **MEDIUM** | Elevate proof into a bounded Tier 3 surface container with elevated ground and clear metric typography. |
