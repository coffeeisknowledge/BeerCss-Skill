# Chips

Expert guidance for BeerCSS chips based on official documentation.

Source: `beercss/docs/CHIPS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Chip Patterns

**Basic Suggestion Chip (Bordered):**
```html
<button class="chip">Suggestion</button>
```

**Input Chip (with Close Icon):**
```html
<button class="chip">
  <span>Input Name</span>
  <i>close</i>
</button>
```

**Filter Chip (with Leading Icon):**
```html
<button class="chip">
  <i>done</i>
  <span>Selected</span>
</button>
```

**Filled Chip:**
```html
<button class="chip fill">Filled Chip</button>
```

---

## Attributes & Classes

### Styles (Element: `.chip`)
- `fill`: Solid background (default is border-only).
- `round`: Fully rounded corners.
- `no-elevate`: Default flat appearance.
- `small-elevate`, `medium-elevate`: Elevation shadows.

### Sizes
- `small` (default), `medium`, `large`.

---

## Rules from Source

1. **Tag Selection:** Use the `<button>` tag for interactive chips.
2. **Default Styling:** `small` and `no-elevate` are the defaults. Do not add them to the class list.
3. **Internal Structure:** Use `<span>` for text and `<i>` for icons. Images should use `<img>` or `img class="responsive"`.
4. **Shapes:** Chips are square-ish by default. Use `round` for the pill-shaped Material Design look.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Redundant default classes -->
<button class="chip small no-elevate">Chip</button>
```

✅ **Do:**
```html
<button class="chip">Chip</button>
```

❌ **Don't:**
```html
<!-- Mixing text and icons without spans -->
<button class="chip">close Delete</button>
```

✅ **Do:**
```html
<button class="chip">
  <span>Delete</span>
  <i>close</i>
</button>
```
