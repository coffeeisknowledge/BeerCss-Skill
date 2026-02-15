# Color Helpers

Source: BeerCSS Helpers - Colors

## Material Design Colors

Each color has 10 shades (1-10) plus base, border, and text variants.

### Color Names

amber, blue, blue-grey, brown, cyan, deep-orange, deep-purple, green, grey, indigo, light-blue, light-green, lime, orange, pink, purple, red, teal, yellow

### Variants

For each color (example with `red`):

**Background:**
- `red1` through `red10` (lightest to darkest shades)
- `red` (base shade)

**Border:**
- `red-border` (applies red to border)

**Text:**
- `red-text` (applies red to text)

## Theme Colors (Tokens)

Material Design semantic colors. These correspond to the tokens defined in `@./rules/color-system.md`.

### Primary
- `primary` - Primary background
- `primary-text` - Primary text color
- `primary-border` - Primary border color
- `primary-container` - Primary container background

### Secondary
- `secondary`
- `secondary-text`
- `secondary-border`
- `secondary-container`

### Tertiary
- `tertiary`
- `tertiary-text`
- `tertiary-border`
- `tertiary-container`

### Error
- `error`
- `error-text`
- `error-border`
- `error-container`

### Surface
- `surface` - Surface background
- `surface-variant` - Variant surface
- `inverse-surface` - Inverted surface
- `background` - Page background

### Inverse
- `inverse-primary`
- `inverse-primary-text`
- `inverse-primary-border`

### Monochrome
- `black`, `black-text`, `black-border`
- `white`, `white-text`, `white-border`
- `transparent`, `transparent-text`, `transparent-border`

## Examples

```html
<!-- Background colors -->
<div class="primary">Primary background</div>
<div class="red5">Light red background</div>

<!-- Text colors -->
<span class="error-text">Error message</span>
<span class="blue-text">Blue text</span>

<!-- Border colors -->
<button class="border primary-border">Primary border</button>

<!-- Combining -->
<article class="surface primary-text">
  Surface with primary text
</article>
```

## Theme Switching

Colors automatically adapt to light/dark theme based on the current body class:

```html
<body class="light">
  <div class="primary">Adapts to light theme</div>
</body>

<body class="dark">
  <div class="primary">Adapts to dark theme</div>
</body>
```

## Rules

1. Use semantic colors (`primary`, `secondary`) for theme consistency.
2. Use named colors (`red`, `blue`) for specific decorative needs.
3. Colors auto-adjust for light/dark themes.
4. Combine with other helpers: `class="primary padding"`.
5. Prefer CSS variables `var(--name)` for custom styles as per `@./rules/color-system.md`.
