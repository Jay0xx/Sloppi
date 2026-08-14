# Sloppi Task Routing & Complexity Scaling

The Task Router determines the exact subset of Sloppi modules, research protocols, and audit passes required for a given task, preventing bureaucratic over-engineering on simple fixes while guaranteeing comprehensive rigor on complex projects.

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
│ Protocol: Inspect existing tokens → implement component → audit state. │
│ Modules:  [ component-strategy.md, interaction-implementation.md,      │
│             responsive-audit.md ]                                      │
├────────────────────────────────────────────────────────────────────────┤
│ 3. MEDIUM TASK                                                         │
│ Scope:    Redesign a hero section, build new feature bento, fix page.  │
│ Protocol: Content architecture → compose layout → implement → audit →   │
│           targeted refinement.                                         │
│ Modules:  [ content/page-architecture.md, layout-implementation.md,    │
│             audit/visual-audit.md, refinement/iteration.md ]           │
├────────────────────────────────────────────────────────────────────────┤
│ 4. LARGE TASK                                                          │
│ Scope:    Greenfield web application, full landing page, redesign.     │
│ Protocol: Full 14-Stage Closed-Loop Lifecycle.                         │
│ Modules:  [ All Research, Content, Design System, DESIGN.md,           │
│             Implementation, Audit, and Refinement Modules ]            │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Context-Specific Workflow Mapping

| Incoming User Request | Required Operational Workflow | Primary Modules to Load |
| :--- | :--- | :--- |
| **New Full Project / Website** | `workflows/new-project.md` | Full 14-stage lifecycle (`research/`, `content/`, `design-system/`, `DESIGN.md`, `implementation/`, `audit/`, `refinement/`). |
| **Existing Codebase Redesign** | `workflows/redesign.md` | `implementation/project-inspection.md`, `research/`, `content/`, `design-system/`, `audit/`. |
| **Component Library Extension** | `workflows/component.md` | `implementation/component-strategy.md`, `interaction-implementation.md`, `audit/accessibility-audit.md`. |
| **Mobile / Responsive Layout Bug**| `workflows/visual-fix.md` | `implementation/responsive-implementation.md`, `audit/responsive-audit.md`, `refinement/regression.md`. |
| **Generic / Ugly AI Slop Cleanup**| `workflows/visual-fix.md` | `audit/anti-slop-audit.md`, `audit/hierarchy-audit.md`, `refinement/critique.md`. |

---

## 3. The Sloppi Conflict Resolution Hierarchy

When project constraints, user instructions, and design heuristics conflict, resolve in strict order:

```
1. EXPLICIT USER REQUIREMENTS (User's intentional directives outrank defaults)
       ↓
2. CORE PRODUCT & FUNCTIONAL REQUIREMENTS (Task completion & business logic)
       ↓
3. ACCESSIBILITY & USABILITY STANDARDS (WCAG AA/AAA, keyboard traversal, touch ergonomics)
       ↓
4. EXISTING CODEBASE ARCHITECTURE & CONSTRAINTS (Framework maturity & existing tokens)
       ↓
5. PROJECT DESIGN.MD CONTRACT (Persistent design decisions & ratios)
       ↓
6. SYNTHESIZED RESEARCH EVIDENCE (Transferable principles from source registry)
       ↓
7. SLOPPI HEURISTIC GUIDELINES (Anti-default rules & layout best practices)
       ↓
8. AGENT PERSONAL PREFERENCE (Strictly lowest priority; never override requirements)
```
