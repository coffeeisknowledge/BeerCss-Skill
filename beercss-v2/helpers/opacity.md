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
