# Sloppi v2.0 Task Routing & Complexity Scaling

The Task Router determines the exact subset of Sloppi v2.0 modules, creative divergence passes, and visual verification gates required for a given task—preventing bureaucratic over-engineering on quick fixes while guaranteeing bold art direction and engineering rigor on full builds.

---

## 1. The 4 Task Complexity Tiers

```
┌────────────────────────────────────────────────────────────────────────┐
│ 1. MICRO TASK                                                          │
│ Scope:    1-line CSS adjustment, color token fix, font size tweak.     │
│ Protocol: Direct code modification + verify `:focus-visible` & contrast│
│ Modules:  [ implementation/token-implementation.md ]                   │
├────────────────────────────────────────────────────────────────────────┤
│ 2. SMALL TASK                                                          │
│ Scope:    Redesign a button primitive, improve navbar, fix mobile tap. │
│ Protocol: Inspect project DESIGN.md → implement 6 states → verify DOM. │
│ Modules:  [ design-system/component-rules.md,                          │
│             implementation/interaction-implementation.md,              │
│             audit/responsive-audit.md ]                                │
├────────────────────────────────────────────────────────────────────────┤
│ 3. MEDIUM TASK                                                         │
│ Scope:    Redesign a hero section, build a new section, fix AI slop.   │
│ Protocol: Capture Before screenshot → formulate 2–3 distinct section   │
│           concepts → implement winning concept → compare Before/After. │
│ Modules:  [ doctrine/creative-direction.md,                            │
│             content/page-architecture.md,                              │
│             audit/visual-audit.md, refinement/regression.md ]          │
├────────────────────────────────────────────────────────────────────────┤
│ 4. LARGE TASK                                                          │
│ Scope:    Greenfield web app, full landing page, full app redesign.    │
│ Protocol: Full 8-Stage Creative Director Lifecycle (Live References →  │
│           3-Direction Divergence → Originality Gate → DESIGN.md →      │
│           Primary Composition Prototype → Visual Proof Gate → Scale).  │
│ Modules:  [ doctrine/creative-direction.md, references/source-registry,│
│             design-system/typography.md, templates/DESIGN.template.md, │
│             implementation/protocol.md, audit/anti-slop-audit.md ]     │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Context-Specific Workflow Mapping

| Incoming User Request | Required Operational Workflow | Primary Modules & Companion Tools (Load Only What Fits) |
| :--- | :--- | :--- |
| **New Full Project / Website / Web App** | [workflows/new-project.md](workflows/new-project.md) | [doctrine/creative-direction.md](doctrine/creative-direction.md), [research/source-routing.md](research/source-routing.md), [references/source-registry.md](references/source-registry.md), [implementation/dependency-policy.md](implementation/dependency-policy.md), [implementation/interaction-implementation.md](implementation/interaction-implementation.md), [templates/DESIGN.template.md](templates/DESIGN.template.md), [implementation/protocol.md](implementation/protocol.md). Optional tools by stack: `frontend-design`, `shadcn`, `context7`, `dissolve` (RN/Expo), `playwright`, `web-design-guidelines`, `vercel-react-best-practices` (React/Next). |
| **Existing Codebase Redesign** | [workflows/redesign.md](workflows/redesign.md) | [doctrine/creative-direction.md](doctrine/creative-direction.md), [research/source-routing.md](research/source-routing.md), [implementation/project-inspection.md](implementation/project-inspection.md), [audit/anti-slop-audit.md](audit/anti-slop-audit.md), [refinement/regression.md](refinement/regression.md). Tools by stack: `playwright`, `context7`, `web-design-guidelines`, `vercel-react-best-practices`. |
| **Component Library / Widget Extension** | [workflows/component.md](workflows/component.md) | [design-system/component-rules.md](design-system/component-rules.md), [implementation/component-strategy.md](implementation/component-strategy.md), [implementation/dependency-policy.md](implementation/dependency-policy.md), [implementation/interaction-implementation.md](implementation/interaction-implementation.md), [audit/accessibility-audit.md](audit/accessibility-audit.md). Tools by stack: `shadcn`, `context7`, `dissolve` (RN/Expo), `web-design-guidelines`. |
| **Mobile / Responsive Layout Bug** | [workflows/visual-fix.md](workflows/visual-fix.md) | [implementation/responsive-implementation.md](implementation/responsive-implementation.md), [audit/responsive-audit.md](audit/responsive-audit.md), [refinement/regression.md](refinement/regression.md). Tool: `playwright` (viewport resize + screenshots). |
| **Generic AI Slop or Flat Wireframe Cleanup** | [workflows/visual-fix.md](workflows/visual-fix.md) | [doctrine/creative-direction.md](doctrine/creative-direction.md), [audit/anti-slop-audit.md](audit/anti-slop-audit.md), [refinement/critique.md](refinement/critique.md). Optional: `frontend-design`, `playwright`, `web-design-guidelines`. |

---

## 3. The Sloppi Conflict Resolution Hierarchy

When project constraints, user instructions, and design heuristics conflict, resolve in strict order:

```
1. EXPLICIT USER REQUIREMENTS (User's intentional directives always win)
       ↓
2. CORE PRODUCT & FUNCTIONAL REQUIREMENTS (Task completion & business logic)
       ↓
3. ACCESSIBILITY & USABILITY STANDARDS (WCAG AA/AAA, keyboard focus, ≥44px targets)
       ↓
4. EXISTING CODEBASE ARCHITECTURE & CONSTRAINTS (Framework & existing system)
       ↓
5. PROJECT DESIGN.MD CREATIVE CONTRACT (Winning direction, font voice, materiality)
       ↓
6. OBSERVED LIVE REFERENCE EVIDENCE (Transferable mechanics from source registry)
       ↓
7. SLOPPI ORIGINALITY & ANTI-SLOP GUARDRAILS (Defeating Gen-1 & Gen-2 clichés)
       ↓
8. AGENT DEFAULT HABITS (Strictly lowest priority; never fall back to autopilot)
```
