# Containers

Expert guidance for BeerCSS containers and structural elements based on official documentation.

Source: `beercss/docs/CONTAINERS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Main Content

**Standard Main:**
```html
<main>
  <!-- Content -->
</main>
```

**Responsive Main:**
```html
<main class="responsive">
  <!-- Content that adapts to max-width -->
</main>
```

### Side Content (Asides)

**Right Sidebar:**
```html
<div>
  <aside class="right small-width padding">
    <img class="responsive" src="image.jpg">
  </aside>
  <h5>Main Title</h5>
  <p>Content text...</p>
</div>
```

---

## Attributes & Classes

### Responsiveness
- `responsive`: When applied to `<main>`, it centers the content and applies a maximum width based on breakpoints.

### Side Content Positioning (Element: `<aside>`)
- `left`: Positions the aside to the left of its sibling content.
- `right`: Positions the aside to the right of its sibling content.

---

## Rules from Source

1. **Tag Selection:** Use `<main>` for the primary content area and `<aside>` for supplementary content.
2. **Side Content Layout:** `aside` elements are designed to be placed alongside text or other content within a container (typically a `div`).
3. **Responsiveness:** The `responsive` class on `<main>` is the standard way to ensure a consistent Material Design layout across different screen sizes.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Custom CSS for centering main content -->
<main style="max-width: 1200px; margin: 0 auto">
```

✅ **Do:**
```html
<main class="responsive">
```
