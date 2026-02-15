# Orientation & Directions

Expert guidance for BeerCSS orientation and direction helpers based on official documentation.

Source: `beercss/docs/DIRECTIONS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Horizontal Layout (Default)
Most elements default to horizontal flex layout.

```html
<button>
  <i>home</i>
  <span>Home</span>
</button>
```

### Vertical Layout
Use the `vertical` class to switch to a column-based layout.

```html
<button class="vertical">
  <i>home</i>
  <span>Home</span>
</button>
```

---

## Attributes & Classes

### Orientation
- `horizontal`: Standard row layout (default).
- `vertical`: Switches the flex-direction to column.

---

## Rules from Source

1. **Tag Selection:** Orientation helpers can be applied to buttons, chips, tabs, and nav items.
2. **Icons:** When using `vertical` orientation, the icon (`<i>`) is typically displayed above the text (`<span>`).
3. **Default:** Do not add `horizontal` explicitly as it is the default state for these components.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Redundant horizontal class -->
<button class="horizontal">...</button>
```

✅ **Do:**
```html
<button>...</button>
```
