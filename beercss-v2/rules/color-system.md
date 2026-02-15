# Color System Rule

## SOURCE OF TRUTH (DESIGN TOKENS)

**CRITICAL:** Every color decision MUST reference these CSS variables. These tokens define the Material Design 3 theme for both Light and Dark modes.

---

## Valid Design Tokens

### 1. Primary Actions
- `--primary`: Main brand color for prominent actions.
- `--on-primary`: Text/icon color on top of primary.
- `--primary-container`: Less prominent container color.
- `--on-primary-container`: Text/icon color on top of primary-container.

### 2. Secondary Actions
- `--secondary`: Less prominent brand color.
- `--on-secondary`: Text/icon color on top of secondary.
- `--secondary-container`: Secondary container color.
- `--on-secondary-container`: Text/icon color on top of secondary-container.

### 3. Tertiary Actions
- `--tertiary`: Accent color for contrasting elements.
- `--on-tertiary`: Text/icon color on top of tertiary.
- `--tertiary-container`: Tertiary container color.
- `--on-tertiary-container`: Text/icon color on top of tertiary-container.

### 4. Error States
- `--error`: Color for errors and destructive actions.
- `--on-error`: Text/icon color on top of error.
- `--error-container`: Error container color.
- `--on-error-container`: Text/icon color on top of error-container.

### 5. Background & Surface
- `--background`: Default page background.
- `--on-background`: Default text color on background.
- `--surface`: Background for containers (cards, dialogs).
- `--on-surface`: Text/icon color on surface.
- `--surface-variant`: Alternative surface color.
- `--on-surface-variant`: Text/icon color on surface-variant.
- `--surface-dim`: Dimmed surface for specific contexts.
- `--surface-bright`: Brightened surface.
- `--surface-container-lowest`: Lowest elevation container.
- `--surface-container-low`: Low elevation container.
- `--surface-container`: Standard container color.
- `--surface-container-high`: High elevation container.
- `--surface-container-highest`: Highest elevation container.

### 6. Layout & Feedback
- `--outline`: Color for borders and outlines.
- `--outline-variant`: Lower contrast borders.
- `--shadow`: Shadow color.
- `--scrim`: Backdrop color for overlays.

### 7. Inverse States
- `--inverse-surface`: Inverted background for dark-on-light or light-on-dark contrast.
- `--inverse-on-surface`: Text/icon color on inverse-surface.
- `--inverse-primary`: Primary color variant for inverted surfaces.

---

## Implementation Rules

### ✅ Rule 1: Use Design Tokens
Always prefer the use of these tokens via CSS variables for custom styling:
```css
/* Custom element using design tokens */
.my-custom-element {
  background-color: var(--primary-container);
  color: var(--on-primary-container);
  border: 1px solid var(--outline);
}
```

### ✅ Rule 2: BeerCSS Utility Classes
If a BeerCSS utility class name matches the token name, it is the preferred way to apply the color within HTML:
```html
<!-- Preferred: Using BeerCSS semantic classes -->
<button class="primary">Primary Action</button>
<article class="surface-variant">Content Card</article>
<span class="error-text">Error message</span>
```

### ❌ Rule 3: No Hardcoded Hex Codes
NEVER use hardcoded hex values (e.g., `#0061a4`). All colors must be derived from the theme tokens to ensure they adapt correctly between Light and Dark modes.

---

## Theme Reference (Values)

### Light Theme
- **Primary:** `--primary:#0061a4; --on-primary:#ffffff;`
- **Secondary:** `--secondary:#535f70; --on-secondary:#ffffff;`
- **Error:** `--error:#ba1a1a; --on-error:#ffffff;`
- **Surface:** `--surface:#faf9fc; --on-surface:#1a1c1e;`

### Dark Theme
- **Primary:** `--primary:#9ecaff; --on-primary:#003258;`
- **Background:** `--background:#1a1c1e; --on-background:#e2e2e6;`
- **Surface:** `--surface:#121316;`

*Note: For all other standard MD3 variables not explicitly listed here, follow the standard Material Design 3 mapping based on these base values.*
