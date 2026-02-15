# Estructura Modular de Helpers (desde HELPERS.md)

## Archivos a Crear en helpers/

### 1. helpers/alignment.md

```markdown
# Alignment Helpers

Source: BeerCSS Helpers - Alignment

## Horizontal Alignment
- `left-align` - Align content to the left
- `right-align` - Align content to the right
- `center-align` - Center content horizontally

## Vertical Alignment
- `top-align` - Align content to top
- `bottom-align` - Align content to bottom
- `middle-align` - Center content vertically

## Examples

```html
<!-- Horizontal -->
<div class="center-align">Centered text</div>
<div class="right-align">Right-aligned text</div>

<!-- Vertical (flex container) -->
<div class="row middle-align">
  <span>Vertically centered</span>
</div>
```

## Usage with Flexbox

```html
<div class="row middle-align center-align">
  Content centered both ways
</div>
```
```

---

### 2. helpers/colors.md

```markdown
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

## Theme Colors

Material Design semantic colors:

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

Colors automatically adapt to light/dark theme:

```html
<body class="light">
  <div class="primary">Adapts to light theme</div>
</body>

<body class="dark">
  <div class="primary">Adapts to dark theme</div>
</body>
```

## Rules

1. Use semantic colors (primary, secondary) for theme consistency
2. Use named colors (red, blue) for specific needs
3. Colors auto-adjust for light/dark themes
4. Combine with other helpers: `class="primary padding"`
```

---

### 3. helpers/spacing.md

```markdown
# Spacing Helpers

Source: BeerCSS Helpers - Margins, Paddings, Spaces

## Margin

### All Sides
- `no-margin` - Remove all margin
- `tiny-margin` - 0.25rem (4px)
- `small-margin` - 0.5rem (8px)
- `margin` - 1rem (16px) - DEFAULT
- `medium-margin` - 1.5rem (24px)
- `large-margin` - 2rem (32px)
- `auto-margin` - Auto margin (centering)

### Directional
- `left-margin`, `right-margin`
- `top-margin`, `bottom-margin`
- `horizontal-margin` - Left + right
- `vertical-margin` - Top + bottom

## Padding

### All Sides
- `no-padding` - Remove all padding
- `tiny-padding` - 0.25rem (4px)
- `small-padding` - 0.5rem (8px)
- `padding` - 1rem (16px) - DEFAULT
- `medium-padding` - 1.5rem (24px)
- `large-padding` - 2rem (32px)

### Directional
- `left-padding`, `right-padding`
- `top-padding`, `bottom-padding`
- `horizontal-padding` - Left + right
- `vertical-padding` - Top + bottom

## Space (Gap for Flexbox/Grid)

- `no-space` - Remove gap
- `small-space` - 0.5rem gap
- `space` - 1rem gap - DEFAULT
- `medium-space` - 1.5rem gap
- `large-space` - 2rem gap

## Examples

```html
<!-- Margin -->
<div class="large-margin">Large margin all sides</div>
<div class="horizontal-margin">Margin left + right only</div>
<section class="vertical-margin">Margin top + bottom only</section>

<!-- Padding -->
<article class="card padding">Card with padding</article>
<div class="horizontal-padding">Padding left + right</div>

<!-- Space (Grid gap) -->
<div class="grid large-space">
  <div class="s12 m6">Column 1</div>
  <div class="s12 m6">Column 2</div>
</div>

<!-- Combining -->
<div class="padding margin">Both padding and margin</div>
```

## Responsive Spacing

Combine with breakpoints:

```html
<!-- Small padding on mobile, large on desktop -->
<div class="small-padding s large-padding l">
  Responsive padding
</div>

<!-- No margin on mobile, margin on desktop -->
<div class="no-margin s margin l">
  Responsive margin
</div>
```
```

---

### 4. helpers/sizing.md

```markdown
# Sizing Helpers

Source: BeerCSS Helpers - Sizes

## Element Sizes

### General
- `tiny` - Extra small size
- `small` - Small size
- `medium` - Medium size (often default)
- `large` - Large size
- `extra` - Extra large size

## Width

- `auto-width` - Auto width
- `small-width` - Small width
- `medium-width` - Medium width
- `large-width` - Large width
- `max` - Maximum width (fill container)

## Height

- `auto-height` - Auto height
- `small-height` - Small height
- `medium-height` - Medium height
- `large-height` - Large height

## Text Wrapping

- `wrap` - Allow text wrapping (default)
- `no-wrap` - Prevent text wrapping

## Examples

```html
<!-- Button sizes -->
<button class="small">Small</button>
<button class="medium">Medium</button>
<button class="large">Large</button>
<button class="extra">Extra</button>

<!-- Width -->
<div class="max">Full width</div>
<div class="small-width">Small width</div>

<!-- Height -->
<img class="medium-height" src="image.jpg">

<!-- Responsive max width -->
<div class="max">Full width on all screens</div>

<!-- No wrap text -->
<span class="no-wrap">This text won't wrap</span>
```

## Usage with Components

```html
<!-- Small button -->
<button class="fill small">Small Button</button>

<!-- Large icon -->
<i class="large">home</i>

<!-- Max width card -->
<article class="card max">Full width card</article>
```
```

---

### 5. helpers/elevation.md

```markdown
# Elevation Helpers

Source: BeerCSS Helpers - Elevates, Shadows

## Elevate (Material Design Elevation)

- `no-elevate` - No elevation (flat) - DEFAULT
- `small-elevate` - Small elevation (2dp)
- `elevate` - Medium elevation (4dp)
- `medium-elevate` - Medium-high elevation (8dp)
- `large-elevate` - Large elevation (16dp)

## Shadows (Directional)

- `shadow` - Default shadow
- `left-shadow` - Shadow on left
- `right-shadow` - Shadow on right
- `top-shadow` - Shadow on top
- `bottom-shadow` - Shadow on bottom

## Examples

```html
<!-- Elevated card -->
<article class="card small-elevate">
  Slightly elevated
</article>

<!-- Highly elevated dialog -->
<dialog class="large-elevate">
  Floating dialog
</dialog>

<!-- Button with elevation -->
<button class="fill medium-elevate">
  Elevated button
</button>

<!-- Directional shadow -->
<div class="bottom-shadow">
  Shadow below
</div>
```

## Usage Guidelines

1. Use elevation to show hierarchy
2. Higher elevation = more important
3. Combine with components: `class="card small-elevate"`
4. Avoid over-elevation (use sparingly)

## Elevation Scale

```
no-elevate:     0dp (flat, resting on surface)
small-elevate:  2dp (slightly raised)
elevate:        4dp (raised)
medium-elevate: 8dp (elevated)
large-elevate:  16dp (floating)
```
```

---

### 6. helpers/shapes.md

```markdown
# Shape Helpers

Source: BeerCSS Helpers - Forms, Rounds

## Border Styles

- `border` - Add border
- `no-border` - Remove border

## Shapes

- `square` - Square shape (sharp corners)
- `circle` - Circular shape
- `none` - No specific shape

## Border Radius

### All Corners
- `no-round` - No border radius (square)
- `small-round` - Small radius (4px)
- `round` - Medium radius (8px)
- `medium-round` - Medium-large radius (12px)
- `large-round` - Large radius (16px)

### Directional
- `left-round` - Round left corners
- `right-round` - Round right corners
- `top-round` - Round top corners
- `bottom-round` - Round bottom corners

## Button Fills

- `fill` - Filled background
- `extend` - Extended width
- `tabbed` - Tab-like appearance

## Examples

```html
<!-- Rounded card -->
<article class="card round">
  Rounded corners
</article>

<!-- Circular button -->
<button class="circle">
  <i>add</i>
</button>

<!-- Top rounded only -->
<div class="top-round">
  Rounded top
</div>

<!-- Bordered + rounded -->
<div class="border round">
  Border with rounded corners
</div>

<!-- Filled button -->
<button class="fill">Primary</button>
```

## Common Patterns

```html
<!-- Rounded card with border -->
<article class="card border round padding">
  Card content
</article>

<!-- Circular FAB -->
<button class="circle large-elevate">
  <i>add</i>
</button>

<!-- Pill-shaped button -->
<button class="fill large-round">
  Pill Button
</button>
```
```

---

### 7. helpers/responsive.md

```markdown
# Responsive Helpers

Source: BeerCSS Helpers - Responsive, Breakpoints

## Breakpoints

- `s` - Small devices (0-600px) - Mobile
- `m` - Medium devices (601-1240px) - Tablet
- `l` - Large devices (1241px+) - Desktop

## Usage

### Show/Hide on Breakpoints

```html
<!-- Show only on small (mobile) -->
<div class="s">Mobile only</div>

<!-- Show on medium and large (tablet + desktop) -->
<div class="m l">Tablet and desktop</div>

<!-- Hide on small -->
<div class="m l">Hidden on mobile</div>
```

### Responsive Grid

```html
<div class="grid">
  <!-- Full width on mobile, half on tablet, third on desktop -->
  <div class="s12 m6 l4">Column</div>
  <div class="s12 m6 l4">Column</div>
  <div class="s12 m6 l4">Column</div>
</div>
```

### Responsive Sizing

```html
<!-- Small padding on mobile, large on desktop -->
<div class="small-padding s large-padding l">
  Responsive padding
</div>
```

### Responsive Images

```html
<img class="responsive" src="image.jpg">
<!-- Scales to container width -->
```

## Common Patterns

### Mobile-First Navigation

```html
<!-- Bottom bar on mobile -->
<nav class="bottom s">
  <a><i>home</i></a>
  <a><i>search</i></a>
</nav>

<!-- Sidebar on desktop -->
<nav class="left l">
  <a><i>home</i><span>Home</span></a>
  <a><i>search</i><span>Search</span></a>
</nav>
```

### Responsive Content

```html
<!-- Stack on mobile, side-by-side on desktop -->
<div class="grid">
  <div class="s12 l6">Content 1</div>
  <div class="s12 l6">Content 2</div>
</div>
```

### Conditional Spacing

```html
<!-- No margin on mobile, margin on desktop -->
<section class="no-margin s margin l">
  Content
</section>
```

## Rules

1. **Mobile-first:** Design for small screens first
2. **Progressive enhancement:** Add features for larger screens
3. **Grid system:** Use s12 m6 l4 patterns
4. **Test breakpoints:** Verify at 600px and 1240px
```

---

### 8. helpers/positioning.md

```markdown
# Positioning Helpers

Source: BeerCSS Helpers - Positions, Directions

## Alignment Positions

- `left` - Align to left
- `right` - Align to right
- `center` - Center horizontally
- `top` - Align to top
- `bottom` - Align to bottom
- `middle` - Center vertically

## Z-Index Layers

- `front` - Bring to front
- `back` - Send to back

## Directions

- `horizontal` - Horizontal layout (default for flex)
- `vertical` - Vertical layout (flex-direction: column)

## Examples

```html
<!-- Positioned elements -->
<div class="top right">Top-right corner</div>
<div class="bottom center">Bottom center</div>

<!-- Z-index -->
<div class="front">Front layer</div>
<div class="back">Back layer</div>

<!-- Flex direction -->
<div class="row vertical">
  <span>Item 1</span>
  <span>Item 2</span>
</div>
```

## Layout Positioning

```html
<!-- Sidebar left -->
<nav class="left">Left navigation</nav>

<!-- Sidebar right -->
<nav class="right">Right sidebar</nav>

<!-- Top bar -->
<header class="top">Top header</header>

<!-- Bottom bar -->
<footer class="bottom">Bottom footer</footer>
```

## Flexbox Alignment

```html
<!-- Center content in row -->
<div class="row center middle">
  Centered content
</div>

<!-- Right-aligned buttons -->
<nav class="right-align">
  <button>Cancel</button>
  <button class="fill">Save</button>
</nav>
```
```

---

### 9. helpers/opacity.md

```markdown
# Opacity Helpers

Source: BeerCSS Helpers - Opacities

## Opacity Levels

- `no-opacity` - Fully opaque (opacity: 1)
- `small-opacity` - Slight transparency (opacity: 0.87)
- `opacity` - Medium transparency (opacity: 0.6)
- `medium-opacity` - More transparent (opacity: 0.38)
- `large-opacity` - Very transparent (opacity: 0.12)

## Examples

```html
<!-- Slightly transparent overlay -->
<div class="small-opacity surface">
  Subtle overlay
</div>

<!-- Disabled state -->
<button class="medium-opacity" disabled>
  Disabled button
</button>

<!-- Watermark -->
<div class="large-opacity">
  Watermark text
</div>
```

## Common Uses

```html
<!-- Disabled text -->
<span class="medium-opacity">Disabled text</span>

<!-- Overlay -->
<div class="overlay opacity">
  Modal backdrop
</div>

<!-- Faded image -->
<img class="small-opacity" src="bg.jpg">
```
```

---

### 10. helpers/utilities.md

```markdown
# Utility Helpers

Source: BeerCSS Helpers - Misc Utilities

## Scrolling

- `scroll` - Enable scrolling
- `no-scroll` - Disable scrolling

## Ripple Effects

- `ripple` - Material ripple effect
- `slow-ripple` - Slow ripple animation
- `fast-ripple` - Fast ripple animation

## Waves

- `wave` - Wave animation
- `no-wave` - Disable wave

## Blur Effects

- `blur` - Medium blur
- `small-blur` - Light blur
- `medium-blur` - Medium blur
- `large-blur` - Heavy blur
- `light` - Light blur variant
- `dark` - Dark blur variant

## Zoom

- `zoom` - Default zoom
- `tiny-zoom` - Tiny zoom level
- `small-zoom` - Small zoom
- `medium-zoom` - Medium zoom
- `large-zoom` - Large zoom
- `extra-zoom` - Extra large zoom

## Triggers

- `active` - Active state styling

## Theme

- `light` - Light theme
- `dark` - Dark theme

## Examples

```html
<!-- Scrollable container -->
<div class="scroll medium-height">
  Long content...
</div>

<!-- Button with ripple -->
<button class="ripple">
  Click me
</button>

<!-- Blurred background -->
<div class="blur">
  Blurred content
</div>

<!-- Active tab -->
<a class="active">Current tab</a>

<!-- Theme switching -->
<body class="dark">
  Dark mode content
</body>
```

## Common Patterns

```html
<!-- Scrollable list -->
<ul class="scroll large-height">
  <li>Item 1</li>
  <li>Item 2</li>
  ...
</ul>

<!-- Interactive button -->
<button class="fill ripple">
  Interactive
</button>

<!-- Frosted glass effect -->
<div class="blur surface small-opacity">
  Glassmorphism
</div>
```
```

---

## Resumen de Archivos Creados

```
helpers/
├── alignment.md (left-align, right-align, center-align, etc.)
├── colors.md (full palette + theme colors)
├── spacing.md (margin, padding, space/gap)
├── sizing.md (tiny, small, medium, large, extra, widths, heights)
├── elevation.md (elevate, shadows)
├── shapes.md (border, round, circle, fills)
├── responsive.md (s, m, l breakpoints)
├── positioning.md (left, right, top, bottom, front, back)
├── opacity.md (opacity levels)
├── typography.md (→ Ya existe como TYPOGRAPHY.md componente)
└── utilities.md (scroll, ripple, wave, blur, zoom, active, theme)
```

## Uso en SKILL.md

```markdown
## Helpers Reference

### Spacing
@./helpers/spacing.md

### Colors
@./helpers/colors.md

### Responsive
@./helpers/responsive.md

### All Helpers
- Alignment: @./helpers/alignment.md
- Colors: @./helpers/colors.md
- Spacing: @./helpers/spacing.md
- Sizing: @./helpers/sizing.md
- Elevation: @./helpers/elevation.md
- Shapes: @./helpers/shapes.md
- Responsive: @./helpers/responsive.md
- Positioning: @./helpers/positioning.md
- Opacity: @./helpers/opacity.md
- Utilities: @./helpers/utilities.md
```
