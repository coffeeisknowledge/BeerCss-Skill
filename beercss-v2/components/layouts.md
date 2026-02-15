# Layouts & Positioning

Expert guidance for BeerCSS layouts and alignment based on official documentation.

Source: `beercss/docs/LAYOUTS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Absolute Positioning (Applied to element)

**Top-Right:**
```html
<div class="absolute top right">Pinned to top-right</div>
```

**Center-Middle:**
```html
<div class="absolute middle center">Perfectly centered</div>
```

### Parent Alignment (Applied to container)

**Right-Bottom Align:**
```html
<div class="right-align bottom-align">
  <div>Children pushed to corner</div>
</div>
```

---

## Attributes & Classes

### Positions (Self)
- `left`, `center`, `right`: Horizontal axis.
- `top`, `middle`, `bottom`: Vertical axis.
- `absolute`, `fixed`: CSS positioning modes.

### Alignments (Container)
- `left-align`, `center-align`, `right-align`: Horizontal alignment of children.
- `top-align`, `middle-align`, `bottom-align`: Vertical alignment of children.

### Header & Footer Patterns
Use `<header>` and `<footer>` with `fixed` for sticky sections.

```html
<article class="scroll">
  <header class="fixed">Fixed Header</header>
  <p>Content...</p>
  <footer class="fixed">Fixed Footer</footer>
</article>
```

---

## Specialized Patterns

### Empty States
Use `middle-align center-align` on a container.

```html
<article class="medium middle-align center-align">
  <div>
    <i class="extra">mail</i>
    <h5>Empty Inbox</h5>
    <p>Check back later.</p>
  </div>
</article>
```

### Visual Effects
- `blur`: Frosty background effect.
- `shadow`: Adds elevation shadows.

---

## Rules from Source

1. **Self vs. Parent:** Use `left`, `top`, etc. for absolute/fixed elements. Use `left-align`, `top-align`, etc. on containers to align multiple children.
2. **Fixed Elements:** For `header fixed` or `footer fixed` to work inside an element, that element MUST have the `scroll` class.
3. **Empty States:** Center everything vertically and horizontally for prominent empty state screens.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Incorrectly applying container alignment to self -->
<button class="center-align">Centered?</button>
```

✅ **Do:**
```html
<!-- Apply alignment to parent -->
<div class="center-align">
  <button>Centered</button>
</div>
```

OR

```html
<!-- Apply position to self (if absolute) -->
<button class="absolute center">Centered</button>
```
