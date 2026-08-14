# Sloppi Accessibility & Usability Standards

In Sloppi, accessibility is an integral component of the design system's mathematical and semantic definition. It is never treated as an optional post-implementation cleanup step.

A coding agent must construct design tokens, HTML structures, and interactive states to be accessible by default across visual, motor, and cognitive dimensions.

---

## 1. Contrast Ratios & Verification Standards

All color pairings defined in `DESIGN.md` must be mathematically verified against Web Content Accessibility Guidelines (WCAG 2.1):

| Content Type | WCAG Minimum Ratio | Sloppi Default Standard | Target Token Roles |
| :--- | :--- | :--- | :--- |
| **Normal Body Copy (<18px)** | `4.5:1` (AA) | **$\ge 7:1$ (AAA)** | `--color-text-primary` against `--color-canvas` |
| **Large Text ($\ge 18\text{px}$ bold / $24\text{px}$)** | `3.0:1` (AA) | **$\ge 4.5:1$ (AA)** | `--font-heading-md` / `--font-display-xl` |
| **Supporting Copy & Subtitles**| `4.5:1` (AA) | **$\ge 4.5:1$ (AA)** | `--color-text-secondary` against `--color-canvas` |
| **UI Boundaries & Controls** | `3.0:1` (AA) | **$\ge 3.0:1$ (AA)** | Form input borders, active tab outlines |
| **Text on Brand Signature Fills** | `4.5:1` (AA) | **$\ge 4.5:1$ (AA)** | `--color-brand-contrast` against `--color-brand` |

---

## 2. Keyboard Focus Rings & Navigation Flow

Every interactive element (buttons, links, inputs, tabs, checkboxes, disclosure accordions) must possess an unmistakable, high-contrast focus indicator when navigated via keyboard.

### The Focus Ring Standard
```css
/* Sloppi Global Focus Ring Rule */
:focus-visible {
  outline: 2px solid var(--color-focus-ring);
  outline-offset: 2px;
}

/* Never suppress focus outlines without a replacement */
:focus:not(:focus-visible) {
  outline: none;
}
```
- **Focus Order**: The visual tab order must strictly match the logical DOM sequence. Never manipulate `tabindex` with arbitrary positive integers.
- **Skip Links**: Long-scroll pages with deep header navigations must include a hidden-until-focused `<a href="#main-content" class="skip-link">Skip to main content</a>` anchor.

---

## 3. Semantic HTML5 & Landmark Hierarchy

Coding agents must use appropriate semantic HTML5 elements rather than nesting endless generic `<div>` containers:

```html
<header>          <!-- Global branding & primary navigation -->
  <nav aria-label="Main Navigation"> ... </nav>
</header>
<main id="main-content"> <!-- Primary unique page content -->
  <article>       <!-- Self-contained editorial or entity unit -->
    <h1> ... </h1><!-- Exactly ONE H1 per page -->
    <section> ... </section>
  </article>
</main>
<footer>          <!-- Global footer, sitemap & legal disclosures -->
</footer>
```

### Strict Heading Hierarchy Rule
- **Exactly one `<h1>` per page**: The primary page or product title.
- **No Skipping Heading Levels**: An `<h3>` must never directly follow an `<h1>` without an intervening `<h2>`.

---

## 4. Redundant State Indicators (Color Independence)

Never convey critical status or error feedback through color alone:
- **Form Errors**: Pair a red input border with a visible descriptive error message (`aria-describedby="email-error"`) and an error icon glyph.
- **Status Badges**: Pair a green/amber/red color token with explicit text labels (*"Active"*, *"Degraded"*, *"Offline"*).

---

## 5. Screen Reader Announcements & ARIA Attributes

- **Dynamic Content Updates**: Use `aria-live="polite"` on notification toasts and filter result counts so screen readers announce changes without interrupting the user.
- **Interactive Disclosures**: Toggle buttons for accordions and mobile menus must explicitly declare `aria-expanded="true|false"` and `aria-controls="panel-id"`.
- **Standalone Icons**: Icon-only buttons must have `aria-label="[Exact action name]"` and the SVG icon itself must be marked `aria-hidden="true"`.
