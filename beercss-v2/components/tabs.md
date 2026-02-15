# Tabs

Expert guidance for BeerCSS tabs based on official documentation.

Source: `beercss/docs/TABS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Tab Patterns

**Basic Tabs:**
```html
<div>
  <div class="tabs">
    <a class="active">Tab 1</a>
    <a>Tab 2</a>
    <a>Tab 3</a>
  </div>
  <div class="page padding active">
    <h5>Content 1</h5>
  </div>
  <div class="page padding">
    <h5>Content 2</h5>
  </div>
</div>
```

**Tabs with Icons:**
```html
<div class="tabs">
  <a class="active">
    <i>home</i>
    <span>Home</span>
  </a>
  <a>
    <i>settings</i>
    <span>Settings</span>
  </a>
</div>
```

---

## Attributes & Classes

### Container Styles (Element: `.tabs`)
- `min`: Narrow indicator (matching text width).
- `max`: Wide indicator (matching tab width - DEFAULT).
- `center-align`, `right-align`: Alignment of the tabs.

### Item Styles (Element: `<a>`)
- `active`: Highlights the current tab.
- `vertical`: Switches tab layout to vertical (icon on top of text).

### Page Transitions (Element: `.page`)
- `left`: Transition page from the left.
- `right`: Transition page from the right.
- `active`: Shows the current page content.

---

## Rules from Source

1. **Tag Selection:** Tabs are implemented using a `<div class="tabs">` containing `<a>` tags.
2. **Page Association:** Each tab should correspond to a `<div class="page">` container.
3. **Indicator:** The indicator defaults to `max`. Use `min` on the `.tabs` container for a more subtle indicator.
4. **Orientation:** Default is horizontal. For vertical tabs (icon above text), use `class="vertical"` on the `<a>` tag.
5. **Transitions:** The `active` class on a `.page` determines visibility.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Redundant alignment/orientation classes -->
<div class="tabs left-align horizontal">
```

✅ **Do:**
```html
<!-- Clean markup using defaults -->
<div class="tabs">
```

❌ **Don't:**
```html
<!-- Missing 'active' class on current page -->
<div class="tabs">
  <a class="active">Tab 1</a>
</div>
<div class="page">Tab 1 Content</div>
```

✅ **Do:**
```html
<div class="tabs">
  <a class="active">Tab 1</a>
</div>
<div class="page active">Tab 1 Content</div>
```
