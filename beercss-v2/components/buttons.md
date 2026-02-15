# Buttons

Expert guidance for BeerCSS buttons based on official documentation.

Source: `beercss/docs/BUTTONS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Button Patterns

**Default Button (Tertiary/Text):**
```html
<button>Button</button>
```

**Primary (Filled):**
```html
<button class="fill">Primary</button>
```

**Secondary (Border):**
```html
<button class="border">Secondary</button>
```

**Primary (Semantic Color):**
```html
<button class="primary">Primary Color</button>
```

---

## Attributes & Classes

### Styles
- `default`: Standard appearance.
- `fill`: Solid background (primary action).
- `border`: Outline only (secondary action).
- `primary`, `secondary`, `tertiary`: MD3 semantic color backgrounds.
- `transparent`: No background or border.

### Sizes
- `small`: Compact.
- `medium`: Default (no class needed).
- `large`: Prominent.
- `extra`: Largest size, often used for FABs.

### Shapes
- `small-round`: Slightly rounded corners.
- `round`: Fully rounded corners.
- `circle`: Circular shape (for icons).
- `square`: Square shape.

### Elevation
- `no-elevate`: Default flat.
- `small-elevate`: 2dp.
- `medium-elevate`: 4dp.
- `large-elevate`: 8dp.

---

## Specialized Buttons

### FAB (Floating Action Button)
Use `circle` or `square` with `extra` size and elevation.

```html
<button class="circle extra large-elevate">
  <i>add</i>
</button>
```

**Extended FAB:**
```html
<button class="extend circle">
  <i>add</i>
  <span>Action</span>
</button>
```

### Icon Buttons
Use `transparent` with `circle` or `square`.

```html
<button class="transparent circle">
  <i>search</i>
</button>
```

### Button Groups
Wrap buttons in a `<nav class="group">`.

```html
<nav class="group connected">
  <button class="left-round">Left</button>
  <button class="no-round">Middle</button>
  <button class="right-round">Right</button>
</nav>
```

---

## Rules from Source

1. **Default Elements:** Do NOT add `default`, `medium`, `no-elevate`, or `horizontal` to the `class` list as they are the default styles.
2. **Icons + Text:** Use `<i>` for the icon and `<span>` for the text inside the `<button>`.
3. **Responsive:** Use `class="responsive"` to make a button fill its container width.
4. **Semantic Borders:** When using `border` with semantic colors, you can use `primary-border primary-text` for consistency.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Redundant classes -->
<button class="default medium horizontal no-elevate">Button</button>
```

✅ **Do:**
```html
<!-- Clean and semantic -->
<button>Button</button>
```

❌ **Don't:**
```html
<!-- Incorrect icon/text wrapping -->
<button>home Button</button>
```

✅ **Do:**
```html
<!-- Correct BeerCSS pattern -->
<button>
  <i>home</i>
  <span>Button</span>
</button>
```
