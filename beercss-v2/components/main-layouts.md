# Main Layout Patterns

Expert guidance for high-level application layouts in BeerCSS based on official documentation.

Source: `beercss/docs/MAIN-LAYOUTS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Application Layout Modes

**Compact (Mobile):**
Uses a bottom navigation bar.
```html
<nav class="bottom s">
  <a><i>home</i><div>Home</div></a>
</nav>
<main class="responsive">
  <h3>Content</h3>
</main>
```

**Medium (Tablet/Desktop):**
Uses a left navigation rail.
```html
<nav class="left m l">
  <a><i>home</i><div>Home</div></a>
</nav>
<main class="responsive">
  <h3>Content</h3>
</main>
```

**Expanded (Desktop):**
Uses a wide left navigation drawer.
```html
<nav class="left max l">
  <a><i>home</i><div>Home</div></a>
</nav>
<main class="responsive">
  <h3>Content</h3>
</main>
```

---

## Responsive Panes

Using the grid system inside `main` for multi-pane layouts.

```html
<main class="responsive">
  <div class="grid">
    <div class="s12 m6">
      <!-- Left Pane -->
    </div>
    <div class="s12 m6">
      <!-- Right Pane -->
    </div>
  </div>
</main>
```

---

## Rules from Source

1. **Top-Level Tags:** Use `<nav>` for global navigation and `<main class="responsive">` for the primary view area.
2. **Device Adaptation:** Combine `nav.bottom.s` with `nav.left.m.l` to create a responsive layout that adapts between mobile and desktop.
3. **Responsive Main:** Always use the `responsive` class on `<main>` to ensure proper padding and max-widths across screen sizes.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Main content without responsive container -->
<main>...</main>
```

✅ **Do:**
```html
<main class="responsive">...</main>
```
