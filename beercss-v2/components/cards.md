# Cards

Expert guidance for BeerCSS cards based on official documentation.

Source: `beercss/docs/CARDS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Card Patterns

**Basic Card:**
```html
<article>
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

**Rounded & Bordered Card:**
```html
<article class="border round">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

**Card with Media (Full-Bleed Header):**
```html
<article class="no-padding">
  <img class="responsive small" src="image.jpg">
  <div class="padding">
    <h5>Title</h5>
    <p>Description...</p>
    <nav>
      <button>Action</button>
    </nav>
  </div>
</article>
```

---

## Attributes & Classes

### Styles (Element: `<article>`)
- `default`: Standard card appearance.
- `border`: Adds a thin outline.
- `round`: Applies border-radius (rounded corners).
- `no-padding`: Removes internal padding (essential for full-bleed images).
- `primary-container`, `secondary-container`, `tertiary-container`: MD3 semantic color backgrounds.
- `fill`: Solid background (use without suffixes).

### Content Helpers
- `padding`: Restores padding inside a `no-padding` card for text sections.
- `row`: Align elements (like avatars and titles) horizontally.
- `max`: Fills remaining space in a row.

---

## Advanced Layouts

### Card with Side Media
Use the BeerCSS grid system inside the card.

```html
<article class="no-padding">
  <div class="grid no-space">
    <div class="s6">
      <img class="responsive" src="image.jpg">
    </div>
    <div class="s6">
      <div class="padding">
        <h5>Title</h5>
        <p>Text...</p>
      </div>
    </div>
  </div>
</article>
```

### Image Overlay
Position text over an image using absolute positioning.

```html
<article class="no-padding round">
  <img class="responsive medium" src="image.jpg">
  <div class="row absolute bottom left right padding bottom-shadow bottom-round white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

---

## Rules from Source

1. **Tag Selection:** Cards are implemented using the `<article>` tag.
2. **Media Handling:** Use `class="no-padding"` on the `<article>` when including images that should touch the edges.
3. **Responsive Images:** Always add `class="responsive"` to images inside cards to ensure they fit correctly.
4. **Header Images:** If the card is rounded (`round`), the top image should also have `top-round` to match the corners.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Redundant/Mixed Styles -->
<article class="card primary-container-fill">
```

✅ **Do:**
```html
<!-- Use clean semantic classes -->
<article class="primary-container">
```

❌ **Don't:**
```html
<!-- Missing top-round on image for a rounded card -->
<article class="round no-padding">
  <img class="responsive" src="...">
</article>
```

✅ **Do:**
```html
<article class="round no-padding">
  <img class="responsive top-round" src="...">
</article>
```
