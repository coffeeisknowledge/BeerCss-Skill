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
