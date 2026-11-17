# Sloppi v2.0

> **Creative Direction & Anti-Slop Design Intelligence Skill for Coding Agents**

Coding agents are very good at producing interfaces.  
They are also very good at producing the *exact same* interfaces—even when told not to.

**Sloppi v2.0** transforms coding agents (Antigravity, Claude Code, Codex, Cursor) from passive template regurgitators—and rigid checklist bureaucrats—into **Creative Directors and Design Engineers**.

---

## Why Sloppi v2.0 Exists: The Two Generations of AI Slop

1. **Generation-1 AI Slop (Default LLM Autopilot)**:
   - Centered H1 + two pill buttons + tilted 3D dashboard mockup.
   - Glowing purple/cyan background blur orbs (`filter: blur(120px)`).
   - Identical 3-card icon grids, fake testimonials, and `Inter` on `#0f172a`.
2. **Generation-2 "Anti-Slop" Monoculture (The Overfit Wireframe Trap)**:
   - When agents are merely told *"don't use gradients, shadows, or 3 cards"*, they over-correct into a second cliché: **flat white or dark rectangles with `1px solid` borders everywhere**, `11px` uppercase monospace labels on every section, `Inter` + `JetBrains Mono` by default, Midnight Tungsten + Phosphor Green CLI terminals for every dev tool, and cookie-cutter `8+4` bento grids.

**Sloppi v2.0 defeats both.** Design-system consistency without original art direction produces neat, accessible boredom. Sloppi v2.0 combines **3-direction creative divergence** with **visual-first prototyping** and **engineering discipline**.

---

## The 6 Core Pillars of Sloppi v2.0

1. **Question-Driven Live Reference Inspection**: Agents route research by design question across [references/source-registry.md](references/source-registry.md) and [research/source-routing.md](research/source-routing.md)—including **Typewolf**, **Unsection**, **Spotted in Prod**, **Hover States**, **Dead Simple Sites**, **Cosmos**, **Eyecandy**, **DesignEng Tools**, **Awwwards**, **Godly**, **Minimal Gallery**, **60fps.design**, **Dribbble**, **SaaSPO**, **Loadmo.re**, **Refero Styles**, and verified interactive demos (`libraries.dev/waves`, `dissolve.rselmi.com`, `oxyn.space`, `wobli.space`)—opening actual examples/clips, logging deep links, 4-part motion captures, `[INFERRED]` markers, adaptable principles, and product fit rather than name-dropping from memory.
2. **Three Distinct Design Directions Before Code**: Before locking `DESIGN.md` or writing component code, the agent must generate **3 structurally and aesthetically orthogonal directions** (`Direction A`, `Direction B`, `Direction C`) differing in composition, typography, and interaction (including quiet hierarchy/spacing directions vs. motion-led directions naming the exact product moment improving feedback, orientation, or continuity).
3. **Pre-Implementation Design Originality Gate**: Concepts that resemble standard SaaS templates OR repeat overused "anti-slop" wireframes (`1px` border boxes, default dark-green CLI terminals) are rejected *before* implementation begins.
4. **Behavior-First Motion & Stack-Fit Craft**: Expressive Google Font pairings, tactile materiality, and motion specs that start from intended behavior, check stack fit, dependency cost, and licensing (never auto-importing demo packages), and define trigger, end state, touch, keyboard, repeated activation, and reduced motion.
5. **Visual-First Implementation (Primary Composition Gate)**: The agent prototypes the **primary above-the-fold composition (plus any proposed effect) first**, verifying layout and hierarchy via **screenshots** and timing/continuity via a **browser recording or interaction trace** before scaling.
6. **Real Visual Regression Testing**: Refinements require **Before vs. After viewport screenshot comparisons** (`390px` Mobile, `768px` Tablet, `1280px+` Desktop) and interaction-trace checks when motion changes.

---

## The 8-Stage Creative Director Lifecycle

```
1. Understand & Inspect Live References
        │
        ▼
2. Diverge: Generate 3 Distinct Creative Directions (A vs. B vs. C)
        │
        ▼
3. Pass Originality Gate & Lock Streamlined 10-Section DESIGN.md
        │
        ▼
4. Prototype Primary Composition First (Above-the-Fold / Core Workspace)
        │
        ▼
5. Live Browser Visual Proof Gate (Inspect Screenshot Before Scaling)
        │
        ▼
6. Scale Full Interface & Bespoke Spring Choreography
        │
        ▼
7. Multi-Viewport Visual QA & 30-Signal Anti-Slop Audit
        │
        ▼
8. Side-by-Side Before/After Screenshot Regression & Ship
```

---

## Installation

### 1. Antigravity Global Skill Installation
```bash
git clone https://github.com/Jay0xx/Sloppi.git ~/.gemini/config/skills/sloppi
```

### 2. Codex / Claude Code / Workspace Installation
```bash
# Codex
git clone https://github.com/Jay0xx/Sloppi.git ~/.codex/skills/sloppi

# Claude Code
git clone https://github.com/Jay0xx/Sloppi.git ~/.claude/skills/sloppi

# Project Workspace (.agents)
mkdir -p .agents/skills
git clone https://github.com/Jay0xx/Sloppi.git .agents/skills/sloppi
```

---

## Controlled A/B Testing Protocol (Verifying Skill Impact)

To evaluate Sloppi v2.0 on any frontend prompt, run the exact same brief in two fresh sessions with the same model:
- **Test A (Sloppi v2 Enabled)**: Explicitly invoke `sloppi` and verify that the agent logs live reference observations, diverges into 3 distinct creative directions (A/B/C), passes the Originality Gate in `DESIGN.md`, and prototypes the primary composition first.
- **Test B (Baseline Disabled)**: Run the identical brief without Sloppi to compare art direction distinctiveness, typographic voice, interactive depth, and layout originality.

---

## License

Sloppi is open-source software licensed under the [MIT License](LICENSE).
