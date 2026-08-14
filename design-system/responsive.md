# Sloppi Responsive & Mobile Composition Architecture

Responsive design in Sloppi is treated as **compositional re-architecture**, not merely proportional desktop scaling. Grounded in research from **Loadmo.re**, mobile viewports are designed as independent ergonomic touch environments.

A coding agent must never assume that shrinking a 3-column desktop table into three tiny cramped columns fulfills responsive requirements. Wide desktop grids must be fundamentally reorganized into mobile-native narrative sequences.

---

## 1. Breakpoint Architecture

Sloppi standardizes on four functional responsive thresholds:

```
[ Mobile (<640px) ] ──► Single-column stream, bottom-anchored controls, 44px hit areas
[ Tablet (640px – 1024px) ] ──► 2-column adaptive grid, side rail navigation
[ Desktop (1024px – 1440px) ] ──► Full multi-column dock, bento grids, hover interactions
[ Ultrawide (>1440px) ] ──► Centered container bounds or high-density multi-pane HUD
```

### Breakpoint Tokens
```css
:root {
  --breakpoint-sm: 640px;
  --breakpoint-md: 768px;
  --breakpoint-lg: 1024px;
  --breakpoint-xl: 1280px;
  --breakpoint-2xl: 1536px;
}
```

---

## 2. The 5 Structural Mobile Transformations

When refactoring a desktop interface for mobile screens:

### 1. Navigation Transformation
- **Desktop**: Horizontal header bar with 6 link anchors and utility controls.
- **Mobile Transformation**: Persistent bottom tab bar (for core app routes) or a bottom-anchored slide-up sheet (for documentation menus). The top hamburger button is relocated to the thumb reach zone.

### 2. Multi-Column Data Tables → Vertical Narrative Cards
- **Desktop**: 8-column wide data table with sorting and inline sparklines.
- **Mobile Transformation**: Stacked vertical cards where each row becomes a self-contained card showing the primary entity name, status badge, and an expandable "View Details" accordion disclosure.

### 3. Comparison Grids → Horizontal Swipe Rails / Tab Selectors
- **Desktop**: 3-column side-by-side pricing tier comparison table.
- **Mobile Transformation**: Interactive segment tab control (`[Starter] [Pro] [Enterprise]`) displaying one plan at a time, or a horizontal swipe carousel with page-dot indicators.

### 4. Interactive Hero Split → Stacked Proof-First Flow
- **Desktop**: 50% left headline/CTA + 50% right interactive live sandbox.
- **Mobile Transformation**: Headline $\rightarrow$ Immediate Primary CTA $\rightarrow$ Simplified interactive demo widget underneath.

### 5. Dialogs & Modals → Bottom Drawer Sheets
- **Desktop**: Centered floating modal overlay.
- **Mobile Transformation**: Bottom-anchored sliding sheet (`border-radius: 20px 20px 0 0`) with a pull-down drag handle.

---

## 3. Touch Ergonomics & The Thumb Zone

- **Minimum Hit Target**: Every interactive element (button, link, tab, checkbox, dropdown) must occupy at least $\ge 44\text{px} \times 44\text{px}$ in touch area, even if the visible icon is only $16\text{px}$.
- **Thumb Reach Zones**:
  - *Natural Zone (Bottom 40% of screen)*: Primary conversion buttons, tab navigation, bottom sheet action triggers.
  - *Stretch Zone (Middle 35% of screen)*: Content cards, secondary links, scrollable feeds.
  - *Hard-to-Reach Zone (Top 25% of screen)*: Static breadcrumbs, logos, non-critical timestamps.

---

## 4. Zero Horizontal Overflow Mandate

- **Strict Overflow Prohibition**: Unintended horizontal scrolling on mobile viewports (`overflow-x: hidden` on root + rigorous component width constraints) is an automatic failure.
- **Safe Viewport Padding**: Maintain a minimum `--page-gutter` of $16\text{px}$ on all mobile screens so content never touches raw display glass edges.
