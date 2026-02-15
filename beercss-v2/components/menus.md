# Menus

Expert guidance for BeerCSS menus based on official documentation.

Source: `beercss/docs/MENUS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Menu Patterns

**Basic Dropdown Menu:**
```html
<div>
  <button>
    <span>Actions</span>
    <i>arrow_drop_down</i>
  </button>
  <menu>
    <li>Item 1</li>
    <li>Item 2</li>
  </menu>
</div>
```

**Positioned Menu (Right-aligned):**
```html
<div class="right-align">
  <button class="circle transparent">
    <i>more_vert</i>
  </button>
  <menu class="left no-wrap">
    <li>Edit</li>
    <li>Delete</li>
  </menu>
</div>
```

---

## Attributes & Classes

### Container Styles (Element: `<menu>`)
- `border`: Adds a border around the menu.
- `no-wrap`: Prevents text from wrapping within items.
- `no-padding`: Removes internal padding.
- `left`, `right`: Horizontal alignment relative to the trigger.
- `top`: Positions the menu above the trigger.
- `min`: Docked/Minimum width.
- `max`: Fullscreen menu.

### Content Helpers (Element: `<li>`)
- `no-padding`: Removes padding from a specific item.
- `active`: Highlights the current menu item.

---

## Advanced Structures

### Multi-level Menus
Nesting menus inside list items.

```html
<menu>
  <li>Item 1</li>
  <li>Sub-menu
    <menu>
      <li>Sub-item 1</li>
    </menu>
  </li>
</menu>
```

### Rich Content Menus
Menus can contain icons, images, and secondary text.

```html
<menu class="no-wrap">
  <li>
    <i>home</i>
    <span>Home</span>
  </li>
  <li>
    <img class="circle tiny" src="avatar.jpg">
    <div class="max">
      <div>Username</div>
      <label>Profile settings</label>
    </div>
  </li>
</menu>
```

---

## Rules from Source

1. **Tag Selection:** Use the native HTML `<menu>` tag for the dropdown container.
2. **Context:** A menu MUST be a sibling to its trigger element (typically a `<button>`) inside a shared parent container.
3. **Nesting:** For multi-level menus, nest the child `<menu>` directly inside the parent `<li>`.
4. **Visibility:** Menus are toggled by applying the `active` class to the parent container or the menu itself (depending on the implementation pattern).

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Menu outside its trigger context -->
<button>Open</button>
<menu>...</menu>
```

✅ **Do:**
```html
<!-- Sibling relationship within a container -->
<div>
  <button>Open</button>
  <menu>...</menu>
</div>
```
