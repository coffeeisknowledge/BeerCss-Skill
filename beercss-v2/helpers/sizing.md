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
