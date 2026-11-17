# Workflow: UI Component & Primitive Engineering

This workflow guides an agent through building or refining a reusable UI component primitive with complete state coverage, keyboard accessibility, and token discipline.

---

## Operational Recipe

```
[ Component Workflow ]
        │
        ├──────► STEP 1: Determine Taxonomy Tier & Discover Fit
        │                • Classify Primitive vs. Component vs. Compound (`implementation/component-strategy.md`).
        │                • If external: query `shadcn` MCP / `Dissolve` MCP (RN/Expo) & check `Context7` docs.
        ├──────► STEP 2: Install (if external) & Map Semantic Tokens
        │                • Install into app via existing package manager; adapt to `--color-*`/`--radius-*` tokens.
        ├──────► STEP 3: Implement 12 Component States & Real State Binding
        ├──────► STEP 4: Enforce Keyboard & Focus (2px high-contrast focus ring with offset)
        ├──────► STEP 5: Touch Target & Repeated-Activation Verification (>= 44px; rapid-click safe)
        ├──────► STEP 6: Reduced Motion Fallback (@media prefers-reduced-motion respected)
        └──────► STEP 7: Review & Export (`web-design-guidelines` + `vercel-react-best-practices` if React)
```
