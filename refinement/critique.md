# Sloppi Design Critique & Root-Cause Diagnosis

The Critique Methodology is the diagnostic framework that enables an agent to look at a visual defect, trace it past superficial symptoms to its structural origin, and identify the smallest meaningful intervention.

---

## 1. The 6 Diagnostic Critique Questions

For every identified deficiency, the agent must formulate explicit answers to six questions:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. WHAT IS WRONG?                                                      │
│    Exact physical defect (e.g. "Hero headline drops 1 orphan word").   │
│                                                                        │
│ 2. WHERE IS IT WRONG?                                                  │
│    Exact location (e.g. `src/sections/HeroSection.tsx:L24`).           │
│                                                                        │
│ 3. WHY IS IT WRONG?                                                    │
│    Cognitive or ergonomic impact (e.g. "Disrupts rapid eye scanning"). │
│                                                                        │
│ 4. WHICH DESIGN PRINCIPLE DOES IT VIOLATE?                             │
│    Principle citation (e.g. "Principle 11: Typographic Balance").      │
│                                                                        │
│ 5. HOW IMPORTANT IS THE PROBLEM?                                       │
│    Severity ranking (e.g. "MEDIUM severity · FIX NEXT").               │
│                                                                        │
│ 6. WHAT IS THE SMALLEST MEANINGFUL INTERVENTION?                       │
│    Surgical fix (e.g. "Add `text-wrap: balance;` to display title").   │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Symptom vs. Root Cause: The Diagnostic Trap

A naive coding agent attempts to solve visual symptoms by adding superficial CSS patches. Sloppi forces the agent to trace symptoms down to root causes:

```
┌────────────────────────────────────────────────────────────────────────┐
│  SYMPTOM: "The hero section feels visually weak and uninteresting."    │
├────────────────────────────────────────────────────────────────────────┤
│  ❌ NAIVE AI REFLEX:                                                    │
│     • Add a purple-to-pink gradient background mesh                    │
│     • Add a floating 3D glass sphere                                   │
│     • Add a neon glow border around the card                           │
│     • Add a spinning animated badge                                    │
├────────────────────────────────────────────────────────────────────────┤
│  ✅ SLOPPI ROOT-CAUSE TRACE:                                           │
│     1. Is the copy too vague? (Content Layer)                          │
│     2. Is the headline size ratio too timid? (Hierarchy Layer)         │
│     3. Are 3 secondary buttons screaming for attention? (Hierarchy)   │
│     4. Is there an authentic domain proof element? (Composition Layer) │
│                                                                        │
│  ✅ SLOPPI STRUCTURAL FIX:                                             │
│     • Rewrite copy to state falsifiable technical outcome              │
│     • Boost headline from 36px to 61px with tight -0.025em tracking    │
│     • Demote secondary buttons to subtle 1px outline                   │
│     • Embed a live interactive terminal showing the CLI output         │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 3. The 5-Layer Root-Cause Diagnostic Pipeline

When diagnosing an interface defect, the agent traces the issue through five architectural layers:

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. CONTENT LAYER       ──► Is the problem caused by vague copy,        │
│                            unsubstantiated claims, or bloated text?    │
│                                                                        │
│ 2. HIERARCHY LAYER     ──► Is the problem caused by missing focal      │
│                            points, equal loudness, or competing CTAs?  │
│                                                                        │
│ 3. COMPOSITION LAYER   ──► Is the problem caused by repetitive cards,  │
│                            excessive symmetry, or dead whitespace?     │
│                                                                        │
│ 4. DESIGN SYSTEM LAYER ──► Is the problem caused by an incomplete type │
│                            scale, missing semantic color, or contrast? │
│                                                                        │
│ 5. IMPLEMENTATION LAYER──► Is the problem a simple CSS bug, missing    │
│                            `:focus-visible` ring, or sub-pixel wrap?   │
└────────────────────────────────────────────────────────────────────────┘
```
