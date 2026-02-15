# Shapes

Expert guidance for BeerCSS decorative and functional shapes based on official documentation.

Source: `beercss/docs/SHAPES.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Shape Patterns

**Shape Wrapper:**
```html
<div class="shape sided-cookie7 small">
  <img class="responsive" src="image.png">
</div>
```

**Shape inside Button:**
```html
<button class="circle extra">
  <span class="shape sided-cookie7 max"></span>
</button>
```

---

## Available Shapes

- `loading-indicator`
- `boom`, `burst`, `soft-boom`, `soft-burst`
- `clamshell`, `diamond`, `flower`, `puffy`
- `sided-cookie6`, `sided-cookie7`, `sided-cookie9`, `sided-cookie12`
- `sunny`, `very-sunny`

---

## Attributes & Classes

### Behavior
- `rotate`: Animates the shape with a continuous rotation.
- `max`: Fills the width of its parent element.

### Sizes
- `small`, `medium`, `large`, `extra`.

---

## Rules from Source

1. **Tag Selection:** Shapes are typically `div` or `span` elements with the `shape` class and a specific shape identifier (e.g., `sided-cookie7`).
2. **Media Wrapping:** You can wrap images, videos, or buttons inside a shape container to apply the mask.
3. **Usage:** Shapes are often used for decorative avatars, loading states, or specialized icon backgrounds.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Missing shape class -->
<div class="sunny"></div>
```

✅ **Do:**
```html
<div class="shape sunny"></div>
```
