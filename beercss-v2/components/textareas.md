# Textareas

Expert guidance for BeerCSS textareas based on official documentation.

Source: `beercss/docs/TEXTAREAS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Textarea Patterns

**Basic Textarea (Bordered):**
```html
<div class="field border">
  <textarea></textarea>
</div>
```

**Textarea with Label:**
```html
<div class="field label border">
  <textarea></textarea>
  <label>Description</label>
</div>
```

**Textarea with Helper/Error Text:**
```html
<div class="field label border">
  <textarea></textarea>
  <label>Comments</label>
  <output>Max 500 characters</output>
</div>
```

---

## Attributes & Classes

### Styles (Container: `.field`)
- `border`: Adds a border around the textarea.
- `round`: Fully rounded corners.
- `fill`: Solid background style.
- `label`: Required when using a `<label>` inside the field.
- `prefix`: Required when adding an icon/element before the `<textarea>`.
- `suffix`: Required when adding an icon/element after the `<textarea>`.
- `invalid`: Applies error styling (use with `output.invalid`).

### Sizes
- `small`, `medium` (default), `large`, `extra`.

---

## Advanced Patterns

### Prefix and Suffix Icons

```html
<div class="field label prefix border">
  <i>edit</i>
  <textarea></textarea>
  <label>Edit content</label>
</div>
```

### Combined Styles (Fill + Border + Round)

```html
<div class="field label border round fill large">
  <textarea></textarea>
  <label>Premium feedback</label>
</div>
```

---

## Rules from Source

1. **Wrapper Required:** All textareas MUST be wrapped in a `<div class="field">`.
2. **Default Size:** `medium` is the default; do not add it to the class list.
3. **Invalid State:** Apply `invalid` to the `field` container and the `output` element for error messages.
4. **Label Positioning:** In a `field label`, the `<label>` usually comes after the `<textarea>`.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Missing field wrapper -->
<textarea class="border"></textarea>
```

✅ **Do:**
```html
<div class="field border">
  <textarea></textarea>
</div>
```

❌ **Don't:**
```html
<!-- Incorrectly placing label before textarea in a 'field label' -->
<div class="field label border">
  <label>Label</label>
  <textarea></textarea>
</div>
```

✅ **Do:**
```html
<div class="field label border">
  <textarea></textarea>
  <label>Label</label>
</div>
```
