# Pages

Expert guidance for BeerCSS page components based on official documentation.

Source: `beercss/docs/PAGES.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Page Patterns

**Basic Page (Visible):**
```html
<div class="page active">
  <h5>Page Title</h5>
  <p>Content goes here...</p>
</div>
```

**Positioned Page (Transitions):**
```html
<div class="page right">
  <h5>Right Transition Page</h5>
</div>
```

---

## Attributes & Classes

### Visibility
- `active`: Class required to make the page visible.

### Transitions/Positions
- `left`: Transition from left.
- `right`: Transition from right.
- `top`: Transition from top.
- `bottom`: Transition from bottom.

---

## Rules from Source

1. **Tag Selection:** Use a `<div>` with the `page` class for view containers.
2. **Tabbed Integration:** Pages are commonly used alongside `<div class="tabs">`. The `active` class on a page corresponds to the selected tab.
3. **Responsive:** Pages typically fill their parent container. Use `padding` helper inside the page for text content.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Page hidden by default without active class -->
<div class="page">...</div>
```

✅ **Do:**
```html
<!-- Ensure active view has the class -->
<div class="page active">...</div>
```
