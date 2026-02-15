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

1. Use elevation to show hierarchy.
2. Higher elevation = more important.
3. Combine with components: `class="card small-elevate"`.
4. Avoid over-elevation (use sparingly).

## Elevation Scale

```
no-elevate:     0dp (flat, resting on surface)
small-elevate:  2dp (slightly raised)
elevate:        4dp (raised)
medium-elevate: 8dp (elevated)
large-elevate:  16dp (floating)
```
