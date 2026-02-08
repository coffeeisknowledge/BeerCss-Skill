# Content Display Reference

Detailed reference for components that display information.

## Card

### Purpose
Surfaces for related content and actions.

### Basic Pattern
```html
<article class="card">
  <div class="padding">
    <h5>Title</h5>
    <p>Content</p>
  </div>
</article>
```

### Variations
- **With Image:** Place `<img>` directly inside `<article>`.
- **Elevated:** `class="elevate"`.

---

## List

### Purpose
Vertical indexes of text and images.

### Basic Pattern
```html
<ul class="list">
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

### Variations
- **Rich item:** Use `div class="max"` for headline/supporting text.

---

## Table

### Purpose
Displaying data sets.

### Basic Pattern
```html
<table class="border stripes">
  <thead>
    <tr><th>Header</th></tr>
  </thead>
  <tbody>
    <tr><td>Data</td></tr>
  </tbody>
</table>
```

---

## Grid (12-column System)

### Purpose
Responsive layout organization.

### Basic Pattern
```html
<div class="grid">
  <div class="s12 m6 l4">Column</div>
</div>
```

---

## Media & Icons

### Typography
- Use `<h1>` to `<h6>` for headlines.
- Helpers: `bold`, `italic`, `upper`, `small-text`.

### Icons
- Use Material Icons font: `<i>icon_name</i>`.
- Helpers: `tiny`, `small`, `medium`, `large`, `extra`.
