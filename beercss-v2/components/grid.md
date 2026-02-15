# Grid System

Expert guidance for the BeerCSS responsive grid system based on official documentation.

Source: `beercss/docs/GRID.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Grid Pattern

```html
<div class="grid">
  <div class="s12 m6 l3">
    <!-- Content goes here -->
  </div>
  <div class="s12 m6 l3">
    <!-- Content goes here -->
  </div>
</div>
```

---

## Attributes & Classes

### Container Styles (Element: `.grid`)
- `no-space`: Removes the gap between grid cells.
- `small-space`: 0.5rem gap.
- `space`: 1rem gap (default).
- `medium-space`: 1.5rem gap.
- `large-space`: 2rem gap.

### Cell Sizing (Child Elements)
The grid uses a 12-column system across three breakpoints:

- `s[1-12]`: Small screens (mobile).
- `m[1-12]`: Medium screens (tablet).
- `l[1-12]`: Large screens (desktop).

---

## Responsive Logic

- `s12`: Full width on mobile.
- `m6`: Half width on tablet.
- `l3`: Quarter width on desktop.

Example of a 3-column layout that stacks on mobile:
```html
<div class="grid">
  <div class="s12 l4">Column 1</div>
  <div class="s12 l4">Column 2</div>
  <div class="s12 l4">Column 3</div>
</div>
```

---

## Rules from Source

1. **Hierarchy:** All elements immediately inside a `.grid` are considered "cells".
2. **🚫 No Mixing:** Cells should only contain sizing classes (`s`, `m`, `l`). Do NOT add component classes (like `article`, `field`, `button`) directly to the cell div.
3. **✅ Correct Nesting:** Wrap the component inside the sizing div.

---

## Common Pitfalls

❌ **Don't (Incorrect Nesting):**
```html
<div class="grid">
  <!-- Error: Component class on the cell itself -->
  <article class="s12 m6 l3">...</article>
</div>
```

✅ **Do (Correct Nesting):**
```html
<div class="grid">
  <!-- Success: Cell div wraps the component -->
  <div class="s12 m6 l3">
    <article>...</article>
  </div>
</div>
```

❌ **Don't:**
```html
<!-- Mixing cells with other elements inside grid -->
<div class="grid">
  <div class="s6">Cell</div>
  <span>Not a cell</span>
</div>
```
