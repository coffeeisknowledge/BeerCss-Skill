# Toolbars

Expert guidance for BeerCSS toolbars based on official documentation.

Source: `beercss/docs/TOOLBARS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Toolbar Patterns

**Basic Toolbar:**
```html
<nav class="toolbar">
  <a><i>videocam_off</i></a>
  <a><i>mic</i></a>
  <a class="active"><i>front_hand</i></a>
</nav>
```

**Floating Toolbar:**
```html
<nav class="center-align">
  <nav class="toolbar">
    <a><i>mic</i></a>
    <a><i>videocam</i></a>
  </nav>
  <button class="extra round circle error">
    <i>call_end</i>
  </button>
</nav>
```

---

## Attributes & Classes

### Container Styles (Element: `.toolbar`)
- `fill`: Solid background style.
- `primary-container`, `secondary-container`, `tertiary-container`: MD3 semantic backgrounds.
- `vertical`: Switches orientation to vertical.
- `small-elevate`, `medium-elevate`, `large-elevate`: Elevation shadows.
- `max`: Docked/Full-width mode.

### Item Styles (Element: `<a>`)
- `active`: Highlights the current action.

---

## Rules from Source

1. **Tag Selection:** Toolbars are implemented using `<nav class="toolbar">`.
2. **Items:** Actions inside are typically `<a>` tags containing an `<i>`. You can optionally add `<span>` or `<div>` for text labels.
3. **Floating Mode:** To create a floating toolbar, wrap the `nav.toolbar` and other buttons in a parent `nav` with alignment helpers (e.g., `center-align`).
4. **Docked Mode:** Use `class="max"` on the toolbar to make it span the full width of its container.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Incorrect element for toolbar -->
<div class="toolbar">...</div>
```

✅ **Do:**
```html
<nav class="toolbar">...</nav>
```

❌ **Don't:**
```html
<!-- Mixing buttons and toolbars without proper alignment -->
<nav class="toolbar">
  <a>...</a>
  <button class="error">...</button>
</nav>
```

✅ **Do:**
```html
<!-- Proper floating toolbar pattern -->
<nav class="center-align">
  <nav class="toolbar">...</nav>
  <button class="error">...</button>
</nav>
```
