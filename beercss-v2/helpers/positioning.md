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
