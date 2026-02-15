# Checkboxes

Expert guidance for BeerCSS checkboxes based on official documentation.

Source: `beercss/docs/CHECKBOXES.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Checkbox Patterns

**Basic Checkbox:**
```html
<label class="checkbox">
  <input type="checkbox">
  <span></span>
</label>
```

**Checkbox with Label:**
```html
<label class="checkbox">
  <input type="checkbox">
  <span>Accept terms</span>
</label>
```

**Disabled Checkbox:**
```html
<label class="checkbox">
  <input type="checkbox" disabled>
  <span>Cannot change this</span>
</label>
```

---

## Attributes & Classes

### Sizes (Element: `.checkbox`)
- `small`, `medium` (default), `large`, `extra`.

### Icon Checkboxes
Use the `icon` class on the label and provide two child elements inside the `<span>` (one for unchecked, one for checked).

```html
<label class="checkbox icon">
  <input type="checkbox">
  <span>
    <i>favorite_border</i>
    <i>favorite</i>
  </span>
</label>
```

---

## Field Alignment Patterns

When grouping multiple checkboxes within a form field:

```html
<div class="field middle-align">
  <nav>
    <label class="checkbox">
      <input type="checkbox">
      <span>Item 1</span>
    </label>
    <label class="checkbox">
      <input type="checkbox">
      <span>Item 2</span>
    </label>
  </nav>
  <output>Select at least one</output>
</div>
```

---

## Rules from Source

1. **Tag Selection:** Checkboxes are implemented using a `<label class="checkbox">` wrapping an `<input type="checkbox">`.
2. **Span Element:** The `<span>` element inside the label is MANDATORY for the visual representation and text.
3. **Icon Logic:** For `checkbox icon`, the first icon is displayed when unchecked, and the second when checked.
4. **Invalid State:** Use `class="invalid"` on the parent `.field` to indicate an error state for a group of checkboxes.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Missing span element -->
<label class="checkbox">
  <input type="checkbox">
  I agree
</label>
```

✅ **Do:**
```html
<label class="checkbox">
  <input type="checkbox">
  <span>I agree</span>
</label>
```

❌ **Don't:**
```html
<!-- Single icon for icon checkbox -->
<label class="checkbox icon">
  <input type="checkbox">
  <span><i>done</i></span>
</label>
```

✅ **Do:**
```html
<!-- Provide both states -->
<label class="checkbox icon">
  <input type="checkbox">
  <span>
    <i>close</i>
    <i>done</i>
  </span>
</label>
```
