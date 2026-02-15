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

1. **Mobile-first:** Design for small screens first.
2. **Progressive enhancement:** Add features for larger screens.
3. **Grid system:** Use `s12 m6 l4` patterns.
4. **Test breakpoints:** Verify at 600px and 1240px.
