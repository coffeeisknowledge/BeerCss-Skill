# Switches

Expert guidance for BeerCSS switches based on official documentation.

Source: `beercss/docs/SWITCHES.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Switch Patterns

**Basic Switch:**
```html
<label class="switch">
  <input type="checkbox">
  <span></span>
</label>
```

**Disabled Switch:**
```html
<label class="switch">
  <input type="checkbox" disabled>
  <span></span>
</label>
```

**Checked & Disabled:**
```html
<label class="switch">
  <input type="checkbox" checked disabled>
  <span></span>
</label>
```

---

## Attributes & Classes

### Icon Switches
Use the `icon` class on the label and provide one or two icons inside the `<span>`.

**Single Icon (Inside thumb):**
```html
<label class="switch icon">
  <input type="checkbox">
  <span>
    <i>dark_mode</i>
  </span>
</label>
```

**Double Icon (Unchecked/Checked states):**
```html
<label class="switch icon">
  <input type="checkbox">
  <span>
    <i>close</i>
    <i>done</i>
  </span>
</label>
```

---

## Field Alignment Patterns

Switches are often used in settings lists with a title and description.

```html
<div class="field middle-align">
  <nav>
    <div class="max">
      <h6>Enable Notifications</h6>
      <div>Receive alerts on your device</div>
    </div>
    <label class="switch">
      <input type="checkbox">
      <span></span>
    </label>
  </nav>
</div>
```

---

## Rules from Source

1. **Tag Selection:** Switches are implemented using a `<label class="switch">` wrapping an `<input type="checkbox">`.
2. **Span Element:** The `<span>` element inside the label is MANDATORY for the visual representation.
3. **Icon Logic:** For `switch icon`, a single `<i>` stays in the thumb. Two `<i>` elements act as state indicators (off/on).
4. **Layout:** Use `<div class="max">` within a `nav` to push the switch to the opposite side of the text.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Incorrectly placing text inside the switch label -->
<label class="switch">
  <input type="checkbox">
  <span>Enable WiFi</span>
</label>
```

✅ **Do:**
```html
<!-- Place text outside the label, typically using 'max' helper -->
<nav>
  <span class="max">Enable WiFi</span>
  <label class="switch">
    <input type="checkbox">
    <span></span>
  </label>
</nav>
```

❌ **Don't:**
```html
<!-- Missing span element -->
<label class="switch">
  <input type="checkbox">
</label>
```

✅ **Do:**
```html
<label class="switch">
  <input type="checkbox">
  <span></span>
</label>
```
