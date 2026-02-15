# App Bars

Expert guidance for BeerCSS app bars (top and bottom) based on official documentation.

Source: `beercss/docs/APP-BARS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Top App Bar Patterns

**Basic Top App Bar:**
```html
<header>
  <nav>
    <button class="circle transparent">
      <i>menu</i>
    </button>
    <h6 class="max">App Title</h6>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
</header>
```

**Filled Top App Bar:**
```html
<header class="fill primary">
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <h6 class="max">View Title</h6>
  </nav>
</header>
```

### Bottom App Bar Patterns

```html
<footer>
  <nav>
    <button class="circle transparent">
      <i>menu</i>
    </button>
    <div class="max"></div>
    <button class="square round extra primary">
      <i>add</i>
    </button>
  </nav>
</footer>
```

---

## Attributes & Classes

### Container Elements
- `<header>`: Standard tag for Top App Bars.
- `<footer>`: Standard tag for Bottom App Bars.

### Styles
- `fill`: Solid background using the surface color.
- `primary-container`, `secondary-container`, `tertiary-container`: MD3 semantic backgrounds.
- `transparent`: Used on buttons inside the bar to remove their background.

### Content Helpers
- `nav`: Internal wrapper for alignment.
- `max`: Applied to the title (e.g., `h6`) or a `div` to fill space and align other elements.

---

## Rules from Source

1. **Tag Selection:** Use `<header>` for top bars and `<footer>` for bottom bars.
2. **Nesting:** All content inside the bar should be wrapped in a `<nav>` tag for proper flex alignment.
3. **Buttons:** Primary actions in app bars should use `class="circle transparent"` for icon buttons.
4. **FAB in Bottom Bar:** A Bottom App Bar often includes a prominent FAB (use `extra` size and semantic colors).

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Missing 'nav' wrapper inside header -->
<header>
  <i>menu</i>
  <h6>Title</h6>
</header>
```

✅ **Do:**
```html
<header>
  <nav>
    <i>menu</i>
    <h6 class="max">Title</h6>
  </nav>
</header>
```
