# Sloppi Iconography Architecture

Iconography provides optical wayfinding, accelerates visual scanning, and reinforces interactive affordances.

In Sloppi, icons are functional waypoints, not decorative confetti. An agent must never place an icon beside every single heading, bullet point, or paragraph simply to fill visual space.

---

## 1. The Single-Family Consistency Rule

A catastrophic design system error is mixing disparate icon families across pages (e.g., pairing a 1.5px outline Lucide icon with a solid filled Material icon and a sharp-cornered Phosphor icon).

### Icon System Mandates
- **Single Curated Icon Library**: The project must select and standardize on exactly one icon family (e.g., Lucide, Phosphor, Heroicons, or Feather).
- **Uniform Stroke Weight**: Maintain a single global stroke weight (e.g., `1.5px` or `2.0px`) across all icons regardless of size.
- **Consistent Cap & Join Style**: Ensure all vector lines share identical `stroke-linecap="round"` and `stroke-linejoin="round"` properties.

---

## 2. The 4-Tier Optical Sizing Scale

Icons must align mathematically with the typography scale to ensure proper optical centering alongside text:

| Icon Size Token | Dimensions | Stroke Weight | Paired Typography Token | Typical Application |
| :--- | :--- | :--- | :--- | :--- |
| `--icon-xs` | `12px × 12px` | `1.5px` | `--font-caption` (`11px`) | Inline badge indicators, table sort arrows, tiny status dots. |
| `--icon-sm` | `16px × 16px` | `1.5px` | `--font-body-sm` (`13px`) | Button icons, input leading icons, dropdown chevrons. |
| `--icon-md` | `20px × 20px` | `1.5px – 2px` | `--font-body` (`16px`) | Navigation links, toolbar actions, card headers. |
| `--icon-lg` | `24px × 24px` | `2.0px` | `--font-heading-sm` (`25px`) | Modal header icons, empty-state feature callouts. |

---

## 3. Optical Alignment & Inset Boxes

- **Square Bounding Box**: All icons must sit inside a uniform square bounding box (`viewBox="0 0 24 24"`) with centered internal glyphs.
- **Flex Alignment**: Always pair icons with text using `inline-flex items-center gap-2`. Never apply manual top/bottom margin nudges (`margin-top: 3px`) to center an icon.
- **Standalone Hit Areas**: When an icon button has no adjacent text label (e.g., a close button `✕` or search magnifying glass), the interactive touch target must be expanded to $\ge 44\text{px} \times 44\text{px}$ using padding or an invisible wrapper.

---

## 4. Semantic Usage & Anti-Decoration Rules

1. **Icons Must Clarify, Not Duplicate**: If a button already reads *"Download macOS Binary"*, an adjacent download icon is helpful; placing five download icons in a row across bullet points is visual noise.
2. **Accessible Labeling**: Every standalone icon button must carry an explicit `aria-label="[Action Description]"` attribute for screen readers.
3. **Interactive Hover Feedback**: Interactive icon buttons should transition their stroke color or background container:
   ```css
   .icon-button {
     color: var(--color-text-secondary);
     transition: color var(--duration-fast) var(--ease-standard);
   }
   .icon-button:hover {
     color: var(--color-text-primary);
   }
   ```
