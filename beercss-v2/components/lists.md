# Lists

Expert guidance for BeerCSS lists based on official documentation.

Source: `beercss/docs/LISTS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard List Patterns

**Basic List:**
```html
<ul class="list border">
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

**List with Headlines & Supporting Text:**
```html
<ul class="list border">
  <li>
    <div class="max">
      <h6 class="small">Headline</h6>
      <div>Supporting text</div>
    </div>
    <label>Metadata</label>
  </li>
</ul>
```

**List with Media (Avatars/Icons):**
```html
<ul class="list border">
  <li>
    <img class="circle" src="avatar.jpg">
    <div class="max">
      <h6 class="small">User Name</h6>
      <div>Subtext...</div>
    </div>
    <i>more_vert</i>
  </li>
</ul>
```

---

## Attributes & Classes

### Container Styles (Element: `<ul>`)
- `list`: Required to apply list styling.
- `border`: Adds a border around the list.

### Item Styles (Element: `<li>`)
- `wave`: Adds a wave animation effect.
- `round`: Adds rounded corners to items.

### Child Helpers
- `max`: Fills the available horizontal space for text sections.
- `circle`, `round`: Shapes for avatars/images.
- `front`: Often used for trailing icons or buttons.

---

## Advanced Structures

### Expansion List
Use the `<details>` and `<summary>` tags for expandable list items.

```html
<ul class="list border">
  <li>
    <details>
      <summary>Expansion Header</summary>
      <ul class="list">
        <li>Sub-item 1</li>
      </ul>
    </details>
  </li>
</ul>
```

### Nested Lists
Lists can be nested inside `<li>` elements.

```html
<ul class="list border">
  <li>Parent Item
    <ul class="list border">
      <li>Child Item</li>
    </ul>
  </li>
</ul>
```

---

## Rules from Source

1. **Tag Selection:** Use `<ul>` with the `list` class. Items should be inside `<li>`.
2. **Horizontal Layout:** Use `<div class="max">` for the primary text area to ensure other elements (like icons or labels) are pushed to the edges.
3. **Links:** For clickable list items, wrap the content in an `<a>` inside the `<li>`.
4. **Metadata:** Use `<label>` or `<i>` at the end of an `<li>` for trailing information or actions.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Missing 'list' class -->
<ul class="border">
  <li>Item</li>
</ul>
```

✅ **Do:**
```html
<ul class="list border">
  <li>Item</li>
</ul>
```

❌ **Don't:**
```html
<!-- Incorrect spacing for headline/text -->
<li>
  <h6>Headline</h6>
  <span>Metadata</span>
</li>
```

✅ **Do:**
```html
<li>
  <div class="max">
    <h6>Headline</h6>
  </div>
  <span>Metadata</span>
</li>
```
