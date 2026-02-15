# Snackbars

Expert guidance for BeerCSS snackbars based on official documentation.

Source: `beercss/docs/SNACKBARS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Snackbar Patterns

**Basic Snackbar (Bottom/Indeterminate):**
```html
<div class="snackbar">Message sent.</div>
```

**Snackbar with Action:**
```html
<div class="snackbar">
  <div class="max">Updating application...</div>
  <a class="inverse-primary-text">RETRY</a>
</div>
```

**Top Positioned Snackbar:**
```html
<div class="snackbar top primary">
  Notification at the top.
</div>
```

---

## Attributes & Classes

### Positions
- Default: Bottom.
- `top`: Positions the snackbar at the top of the screen.

### Semantic Colors
- `primary`, `secondary`, `tertiary`: MD3 semantic backgrounds.
- `error`: Destructive/Error state background.

### Content Helpers
- `max`: Fills space for the text, pushing actions to the end.
- `active`: Class to show/trigger the snackbar.

---

## Rules from Source

1. **Tag Selection:** Use a `<div>` with the `snackbar` class.
2. **Action Styling:** Actions inside snackbars typically use `<a>` tags with `inverse-primary-text` for high contrast against the snackbar's dark background.
3. **Trigger:** Snackbars are global UI elements. Use the `active` class to control visibility.
4. **Coloring:** For semantic coloring (e.g., `error`), add the color class directly to the `snackbar` div.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Incorrectly placing text and actions without 'max' -->
<div class="snackbar">
  <span>Text</span>
  <a>Action</a>
</div>
```

✅ **Do:**
```html
<div class="snackbar">
  <div class="max">Text</div>
  <a>Action</a>
</div>
```

❌ **Don't:**
```html
<!-- Hardcoding bottom position -->
<div class="snackbar bottom">...</div>
```

✅ **Do:**
```html
<!-- Use default (no class) for bottom -->
<div class="snackbar">...</div>
```
