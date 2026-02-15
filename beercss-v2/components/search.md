# Search

Expert guidance for BeerCSS search patterns based on official documentation.

Source: `beercss/docs/SEARCH.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Search Patterns

**Docked Search (Inside Field):**
```html
<div class="field large prefix round fill active">
  <i class="front">search</i>
  <input type="text" placeholder="Search...">
  <menu class="min">
    <li><i>history</i><div>Previous Search</div></li>
  </menu>
</div>
```

**Fullscreen Search Menu:**
```html
<div>
  <button class="extra circle fill">
    <i>search</i>
  </button>
  <menu class="max">
    <li>
      <div class="field large prefix">
        <i class="front">arrow_back</i>
        <input type="text">
      </div>
    </li>
    <!-- Search results... -->
  </menu>
</div>
```

---

## Attributes & Classes

### Container Styles
- `active`: Applied to the search field or parent to show the search results menu.
- `min`: Docked menu (search suggestions).
- `max`: Fullscreen search interface.

### Sizing & Shape
- `large`: Standard size for prominent search fields.
- `round`: Pill-shaped search bar.
- `fill`: Material Design filled style.

---

## Rules from Source

1. **Hierarchy:** Search is typically implemented using a `.field` for the input and a sibling `<menu>` for the results/suggestions.
2. **Icons:** Use `<i>search</i>` as a prefix and `<i>arrow_back</i>` inside the results menu to allow users to exit the search context.
3. **Visibility:** The `active` class controls whether the results menu is displayed.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Search results outside of parent context -->
<div class="field">...</div>
<menu>...</menu>
```

✅ **Do:**
```html
<div class="field active">
  <input>
  <menu>...</menu>
</div>
```
