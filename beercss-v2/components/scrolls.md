# Scrolls

Expert guidance for scrollable containers in BeerCSS based on official documentation.

Source: `beercss/docs/SCROLLS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Horizontal Scroll Patterns

**Scrolling Chips:**
```html
<nav class="scroll">
  <button class="chip">Option 1</button>
  <button class="chip">Option 2</button>
  <!-- More chips... -->
</nav>
```

**Scrolling Cards:**
```html
<div class="row scroll">
  <article class="small-width">Card 1</article>
  <article class="small-width">Card 2</article>
  <!-- More cards... -->
</div>
```

---

## Attributes & Classes

### Behavior
- `scroll`: Enables scrolling on the container.
- `row scroll`: Standard combination for horizontal scrolling of child elements.

---

## Rules from Source

1. **Horizontal Layout:** Combine `row` and `scroll` on a `div` to create a horizontal list of items (like cards or images).
2. **Fixed Width Items:** For card carousels, apply a width helper (e.g., `small-width`) to the children to ensure they don't shrink and the scroll behavior is triggered.
3. **Chip Navigation:** A `<nav class="scroll">` is the preferred way to handle a long list of chips.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Items might wrap instead of scroll -->
<div class="scroll">
  <article>Card</article>
</div>
```

✅ **Do:**
```html
<!-- Use row to force horizontal layout -->
<div class="row scroll">
  <article class="small-width">Card</article>
</div>
```
