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
