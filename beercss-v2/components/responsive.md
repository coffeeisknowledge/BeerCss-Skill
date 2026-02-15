# Responsive Visibility

Expert guidance for BeerCSS responsive visibility and device-specific layouts based on official documentation.

Source: `beercss/docs/RESPONSIVE.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Visibility Classes

**Show ONLY on Mobile:**
```html
<div class="s">Visible only on small screens</div>
```

**Show ONLY on Tablet/Desktop:**
```html
<div class="m l">Visible on medium and large screens</div>
```

**Combined Layout Patterns:**
```html
<nav>
  <!-- Mobile icon -->
  <button class="s circle"><i>phone_android</i></button>
  
  <!-- Desktop button with border -->
  <button class="m l border circle"><i>laptop_windows</i></button>
</nav>
```

---

## Breakpoints

- `s`: Small (Mobile, 0 - 600px).
- `m`: Medium (Tablet, 601 - 1240px).
- `l`: Large (Desktop, 1241px+).

---

## Rules from Source

1. **Usage:** Apply `s`, `m`, or `l` classes to any element to control its visibility based on the device's screen width.
2. **Combination:** You can combine multiple classes (e.g., `m l`) to show an element on a range of devices.
3. **BeerCSS Philosophy:** Use these classes to provide tailored experiences for different form factors without custom media queries.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Custom CSS media queries for simple hiding -->
<style>
  @media (max-width: 600px) { .hide-on-mobile { display: none; } }
</style>
```

✅ **Do:**
```html
<div class="m l">Hide me on mobile</div>
```
