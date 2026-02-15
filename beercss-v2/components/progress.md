# Progress Indicators

Expert guidance for BeerCSS progress indicators based on official documentation.

Source: `beercss/docs/PROGRESS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Progress Patterns

**Linear Progress (Indeterminate):**
```html
<progress></progress>
```

**Linear Progress (Determinate):**
```html
<progress value="45" max="100"></progress>
```

**Circular Progress:**
```html
<progress class="circle"></progress>
```

**Wavy Progress (Material Expressive):**
```html
<progress class="wavy"></progress>
```

---

## Attributes & Classes

### Styles (Element: `<progress>`)
- `circle`: Circular progress indicator.
- `wavy`: Expressive wavy animation.
- `max`: Fills the width of its parent container.
- `light-green`, `orange`: Semantic color overrides (default is primary).

---

## Contextual Usage

### Inside Components

**In a Card:**
```html
<article>
  <progress class="max" value="30" max="100"></progress>
  <h5>Uploading...</h5>
</article>
```

**In a Field (Prefix):**
```html
<div class="field border prefix">
  <progress class="circle"></progress>
  <input type="text" placeholder="Searching...">
</div>
```

---

## Rules from Source

1. **Tag Selection:** Use the native HTML `<progress>` tag.
2. **Determinate State:** Use `value` and `max` attributes to show specific progress.
3. **Indeterminate State:** Omit the `value` attribute for a continuous loading animation.
4. **Circular Pattern:** Always add the `circle` class for the circular variant.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Custom CSS for circular progress -->
<div class="spinner"></div>
```

✅ **Do:**
```html
<progress class="circle"></progress>
```
