# Sloppi Responsive & Multi-Viewport Audit

The Responsive Audit evaluates whether an interface refactors gracefully across viewport dimensions, preserving cognitive clarity, spatial rhythm, and touch ergonomics.

```
┌────────────────────────────────────────────────────────────────────────┐
│                      THE RESPONSIVE AUDIT TEST                         │
│                                                                        │
│ "Do not merely ask: 'Does it fit on the screen without horizontal      │
│  scrollbars?'                                                          │
│  Ask: 'Does the composition, reading flow, and touch ergonomics        │
│  still make complete sense on this viewport?'"                         │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 1. The 6-Point Responsive Audit Checklist

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. ZERO HORIZONTAL OVERFLOW    ──► document.body.scrollWidth ===       │
│                                    window.innerWidth across all sizes. │
│ 2. TOUCH TARGET ERGONOMICS     ──► All mobile tap targets >= 44x44px;  │
│                                    no tiny clustered link targets.     │
│ 3. NAVIGATION REFACTORING      ──► Desktop top bar refactors to clean  │
│                                    mobile drawer / bottom dock.        │
│ 4. TABLE / DATA REFACTORING    ──► Wide tables transform to stacked    │
│                                    cards or scrollable swipe blocks.   │
│ 5. HERO COMPOSITION COHERENCE  ──► Split 50/50 hero refactors to clean │
│                                    headline → CTA → demo sequence.     │
│ 6. INPUT AUTO-ZOOM PREVENTION  ──► All form inputs have font-size >=16px│
│                                    on mobile to prevent iOS zoom jump. │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Responsive Deficiency Catalog & Fixes

| Responsive Flaw | Diagnostic Symptom | Severity | Sloppi Remediation |
| :--- | :--- | :--- | :--- |
| **Horizontal Body Overflow** | Mobile screen (390px) wobbles horizontally with a scrollbar due to an unconstrained 600px width element. | **BLOCKER** | Locate element causing overflow; apply `max-width: 100%;` and `overflow-x: clip;` at root. |
| **Sub-44px Tap Targets** | Mobile buttons or navigation links measure only $28\text{px} \times 28\text{px}$, causing mis-taps. | **BLOCKER** | Set `min-height: 44px; min-width: 44px;` on all mobile touch interactive elements. |
| **Crushed Desktop Grid** | 3-column bento grid forced into 390px screen, creating unreadable 80px wide slivers. | **HIGH** | Switch layout to `grid-template-columns: 1fr;` below 768px. |
| **Unresponsive Data Tables** | 6-column matrix spills offscreen with columns truncated. | **HIGH** | Refactor table to stacked key-value cards (`.spec-card`) below 1024px. |
| **Buried Mobile Action Trigger**| Primary CTA is buried 12 scrolls down on mobile with no sticky action trigger. | **MEDIUM** | Introduce a compact fixed bottom action bar on mobile viewports (`fixed bottom-0`). |
