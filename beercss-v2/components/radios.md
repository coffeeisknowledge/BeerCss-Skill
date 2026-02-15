# Radios

Expert guidance for BeerCSS radio buttons based on official documentation.

Source: `beercss/docs/RADIOS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Radio Patterns

**Basic Radio:**
```html
<label class="radio">
  <input type="radio" name="options">
  <span></span>
</label>
```

**Radio with Label:**
```html
<label class="radio">
  <input type="radio" name="options">
  <span>Option 1</span>
</label>
```

**Disabled Radio:**
```html
<label class="radio">
  <input type="radio" name="options" disabled>
  <span>Unavailable</span>
</label>
```

---

## Attributes & Classes

### Sizes (Element: `.radio`)
- `small`, `medium` (default), `large`, `extra`.

### Icon Radios
Use the `icon` class on the label and provide two child elements inside the `<span>` (one for unselected, one for selected).

```html
<label class="radio icon">
  <input type="radio" name="feeling">
  <span>
    <i>sentiment_neutral</i>
    <i>sentiment_very_satisfied</i>
  </span>
</label>
```

---

## Field Alignment Patterns

When grouping multiple radios within a form field:

```html
<div class="field middle-align">
  <nav>
    <label class="radio">
      <input type="radio" name="category">
      <span>Category A</span>
    </label>
    <label class="radio">
      <input type="radio" name="category">
      <span>Category B</span>
    </label>
  </nav>
  <output>Choose one category</output>
</div>
```

---

## Rules from Source

1. **Tag Selection:** Radios are implemented using a `<label class="radio">` wrapping an `<input type="radio">`.
2. **Span Element:** The `<span>` element inside the label is MANDATORY for the visual representation and text.
3. **Grouping:** Ensure all radios in a set share the same `name` attribute.
4. **Icon Logic:** For `radio icon`, the first icon is displayed when unselected, and the second when selected.
5. **Invalid State:** Use `class="invalid"` on the parent `.field` to indicate an error state for the radio group.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Missing name attribute (items won't be grouped) -->
<label class="radio">
  <input type="radio">
  <span>Choice 1</span>
</label>
<label class="radio">
  <input type="radio">
  <span>Choice 2</span>
</label>
```

✅ **Do:**
```html
<label class="radio">
  <input type="radio" name="group1">
  <span>Choice 1</span>
</label>
<label class="radio">
  <input type="radio" name="group1">
  <span>Choice 2</span>
</label>
```

❌ **Don't:**
```html
<!-- Single element inside span for icon radio -->
<label class="radio icon">
  <input type="radio">
  <span><i>check</i></span>
</label>
```

✅ **Do:**
```html
<!-- Provide both states -->
<label class="radio icon">
  <input type="radio">
  <span>
    <i>radio_button_unchecked</i>
    <i>radio_button_checked</i>
  </span>
</label>
```
