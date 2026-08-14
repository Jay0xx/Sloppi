# Sloppi Development Roadmap

This document outlines potential future enhancements and research directions for the Sloppi skill. These items represent prospective explorations rather than guaranteed feature commitments.

---

## Prospective Future Explorations

### 1. Multi-Agent Critique Delegation
- Formalize a multi-agent protocol separating the **Implementer Agent** (responsible for writing code to spec) from the **Auditor Agent** (responsible for independent visual QA, anti-slop screening, and severity scoring).

### 2. Bidirectional Design Token Sync
- Native parsing and synchronization between `tokens.json` (W3C Design Token Community Group standard / Figma Tokens) and the 25-section `DESIGN.md` contract.

### 3. Automated Headless Accessibility Harnesses
- Integration with headless browser accessibility testing engines (e.g. `@axe-core/playwright`) to programmatically output WCAG AAA contrast and ARIA tree validations directly into the 9-field audit finding schema.

### 4. Native Mobile Ergonomics Adapters
- Specialized reference channels and rule sets for React Native, Swift (SwiftUI), and Kotlin (Jetpack Compose) tailored to iOS Human Interface Guidelines and Android Material Design 3.

### 5. Dynamic Physics & Animation Analysis
- Runtime tooling for profiling frame-rate drops, layout thrashing, and spring physics curve compliance across high-refresh displays.
