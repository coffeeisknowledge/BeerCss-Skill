# Inputs

Expert guidance for BeerCSS input fields based on official documentation.

Source: `beercss/docs/INPUTS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Input Patterns

**Basic Input (Bordered & Rounded):**
```html
<div class="field border round">
  <input type="text">
</div>
```

**Input with Label:**
```html
<div class="field label border">
  <input type="text">
  <label>Username</label>
</div>
```

**Input with Helper/Error Text:**
```html
<div class="field label border">
  <input type="text">
  <label>Email</label>
  <output>Required for login</output>
</div>
```

---

## Attributes & Classes

### Styles (Container: `.field`)
- `border`: Adds a border around the input.
- `round`: Fully rounded corners.
- `fill`: Solid background style.
- `label`: Required when using a `<label>` inside the field.
- `prefix`: Required when adding an icon/element before the `<input>`.
- `suffix`: Required when adding an icon/element after the `<input>`.
- `invalid`: Applies error styling (use with `output.invalid`).

### Sizes
- `small`, `medium` (default), `large`, `extra`.

### Input Types
Standard HTML types: `text`, `number`, `password`, `file`, `color`, `date`, `time`.

---

## Advanced Patterns

### Prefix and Suffix Icons
Icons inside the input field.

```html
<div class="field label prefix suffix border">
  <i>person</i>
  <input type="text">
  <label>User</label>
  <i class="front">check_circle</i>
</div>
```
*Note: Suffix icons often use the `front` class.*

### Custom Input Triggers (File/Color/Date)
Using a button to trigger a hidden input.

```html
<div>
  <button class="circle">
    <i>attach_file</i>
  </button>
  <input type="file">
</div>
```

---

## Rules from Source

1. **Wrapper Required:** All inputs MUST be wrapped in a `<div class="field">`.
2. **Default Size:** `medium` is the default; do not add it to the class list.
3. **Invalid State:** Apply `invalid` to the `field` container and the `output` element for error messages.
4. **Label Positioning:** In a `field label`, the `<label>` usually comes after the `<input>`.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Missing field wrapper -->
<input type="text" class="border">
```

✅ **Do:**
```html
<div class="field border">
  <input type="text">
</div>
```

❌ **Don't:**
```html
<!-- Incorrect prefix/suffix markup -->
<div class="field">
  <i>search</i>
  <input type="text">
</div>
```

✅ **Do:**
```html
<!-- Include 'prefix' class on wrapper -->
<div class="field prefix border">
  <i>search</i>
  <input type="text">
</div>
```
