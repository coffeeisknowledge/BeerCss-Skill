# Selects

Expert guidance for BeerCSS select dropdowns based on official documentation.

Source: `beercss/docs/SELECTS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Select Patterns

**Basic Select (Bordered):**
```html
<div class="field suffix border">
  <select>
    <option>Item 1</option>
    <option>Item 2</option>
    <option>Item 3</option>
  </select>
  <i>arrow_drop_down</i>
</div>
```

**Select with Label:**
```html
<div class="field label suffix border">
  <select>
    <option>Item 1</option>
    <option>Item 2</option>
  </select>
  <label>Choose option</label>
  <i>arrow_drop_down</i>
</div>
```

---

## Attributes & Classes

### Styles (Container: `.field`)
- `border`: Adds a border around the select.
- `round`: Fully rounded corners.
- `fill`: Solid background style.
- `label`: Required when using a `<label>` inside the field.
- `suffix`: Required when adding the dropdown arrow icon.
- `invalid`: Applies error styling (use with `output.invalid`).

### Sizes
- `small`, `medium` (default), `large`, `extra`.

---

## Rules from Source

1. **Wrapper Required:** All selects MUST be wrapped in a `<div class="field">`.
2. **Dropdown Icon:** Always include an `<i>arrow_drop_down</i>` (or similar) as a suffix for better UX.
3. **Default Size:** `medium` is the default; do not add it to the class list.
4. **Invalid State:** Apply `invalid` to the `field` container and the `output` element for error messages.
5. **Label Positioning:** In a `field label`, the `<label>` usually comes after the `<select>`.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Missing field wrapper and suffix class -->
<select class="border">
  <option>Item 1</option>
</select>
```

✅ **Do:**
```html
<div class="field suffix border">
  <select>
    <option>Item 1</option>
  </select>
  <i>arrow_drop_down</i>
</div>
```
