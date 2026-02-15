# Navigation

Expert guidance for BeerCSS navigation components based on official documentation.

Source: `beercss/docs/NAVIGATIONS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Navigation Patterns

**Navigation Bar (Horizontal):**
```html
<nav>
  <button>Home</button>
  <div class="max"></div>
  <button class="circle">
    <i>person</i>
  </button>
</nav>
```

**Navigation Rail/Sidebar (Desktop):**
```html
<nav class="left l m">
  <a>
    <i>home</i>
    <span>Home</span>
  </a>
  <a>
    <i>search</i>
    <span>Search</span>
  </a>
</nav>
```

**Tabbed Navigation:**
```html
<nav class="tabbed">
  <a class="active">
    <i>info</i>
    <span>Overview</span>
  </a>
  <a>
    <i>style</i>
    <span>Specs</span>
  </a>
</nav>
```

---

## Attributes & Classes

### Container Elements
- `<nav>`: Primary container for navigation items.
- `<header>`: Used inside `nav` (rail) for the logo or menu button.

### Positioning & Modes
- `left`, `right`: For navigation rails (sidebars).
- `top`, `bottom`: For app bars or mobile navigation.
- `tabbed`: Converts the navigation into a tabbed interface.

### Alignment (within `.row` or `nav`)
- `left-align`: Default alignment.
- `center-align`: Center items horizontally.
- `right-align`: Align items to the right.

### Responsive Classes
- `s`: Show on small screens (mobile).
- `m`: Show on medium screens (tablet).
- `l`: Show on large screens (desktop).
- `responsive`: Adapts based on screen size.

---

## Navigation Tabs & Pages

BeerCSS uses a combination of `.tabbed` navigation and `.page` containers.

```html
<div>
  <nav class="tabbed">
    <a class="active">Tab 1</a>
    <a>Tab 2</a>
  </nav>
  
  <div class="page padding active">
    <!-- Content for Tab 1 -->
  </div>
  <div class="page padding">
    <!-- Content for Tab 2 -->
  </div>
</div>
```

---

## Rules from Source

1. **Flex Alignment:** Use `class="max"` on a child element to push subsequent elements to the far end (flex-grow).
2. **Default Alignment:** `left-align` is the default; do not add it explicitly unless needed for overrides.
3. **Links:** Navigation items are typically `<a>` tags with an `<i>` (icon) and `<span>` (text).
4. **Active State:** Use the `active` class to highlight the current navigation item or page.
5. **Rail Logic:** Navigation rails for desktop usually include the `m l` classes to hide them on mobile.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Hardcoded margins for spacing -->
<nav>
  <button>Home</button>
  <button style="margin-left: auto">Profile</button>
</nav>
```

✅ **Do:**
```html
<!-- Use BeerCSS 'max' helper -->
<nav>
  <button>Home</button>
  <div class="max"></div>
  <button>Profile</button>
</nav>
```

❌ **Don't:**
```html
<!-- Incorrect Tabbed Markup -->
<nav class="tabbed">
  <button>Tab 1</button>
</nav>
```

✅ **Do:**
```html
<!-- Use anchor tags for tabs -->
<nav class="tabbed">
  <a class="active">Tab 1</a>
</nav>
```
