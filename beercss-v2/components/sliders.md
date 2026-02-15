# Sliders

Expert guidance for BeerCSS sliders based on official documentation.

Source: `beercss/docs/SLIDERS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Slider Patterns

**Basic Slider:**
```html
<div class="slider">
  <input type="range" value="25">
  <span></span>
</div>
```

**Slider with Value Indicator (Tooltip):**
```html
<div class="slider">
  <input type="range" value="50">
  <span></span>
  <span class="tooltip"></span>
</div>
```

**Dual Range Slider:**
```html
<div class="slider">
  <input type="range" value="25">
  <input type="range" value="75">
  <span></span>
</div>
```

---

## Attributes & Classes

### Container Styles (Element: `.slider`)
- `vertical`: Switches the slider to a vertical orientation.
- `max`: Fills the width of the parent container.
- `small`, `medium`, `large`, `extra`: Adjusts the track and thumb size (required for inset icons).

### Indicator Position
- `tooltip`: Standard top indicator.
- `tooltip bottom`: Indicator below the slider.

---

## Advanced Patterns

### Inset Icons
Icons inside the slider thumb. Requires a size class on the `.slider`.

```html
<div class="slider medium">
  <input type="range">
  <span>
    <i>sunny</i>
  </span>
</div>
```

### In-Field Layout
Using a slider as part of a form field with icons and labels.

```html
<div class="field middle-align prefix suffix">
  <nav>
    <i>volume_down</i>
    <div class="slider max">
      <input type="range">
      <span></span>
    </div>
    <i>volume_up</i>
  </nav>
</div>
```

---

## Rules from Source

1. **Structure:** A slider requires a container with `class="slider"`, a child `<input type="range">`, and an empty `<span>` for the track.
2. **Default Range:** 0 to 100 unless `min` and `max` attributes are specified.
3. **Dual Inputs:** Two `<input type="range">` elements can be used in the same `.slider` container for range selection.
4. **Icons:** For icons to appear correctly inside the slider thumb, a size helper (like `medium` or `large`) must be added to the `.slider` container.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Missing the track span -->
<div class="slider">
  <input type="range">
</div>
```

✅ **Do:**
```html
<div class="slider">
  <input type="range">
  <span></span>
</div>
```
