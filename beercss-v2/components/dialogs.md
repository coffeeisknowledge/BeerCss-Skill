# Dialogs

Expert guidance for BeerCSS dialogs (modals) based on official documentation.

Source: `beercss/docs/DIALOGS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Dialog Patterns

**Basic Dialog:**
```html
<dialog>
  <h5>Title</h5>
  <div>Content goes here...</div>
  <nav class="right-align no-space">
    <button class="transparent link">Cancel</button>
    <button class="transparent link">Confirm</button>
  </nav>
</dialog>
```

**Modal Dialog (with Overlay):**
```html
<div class="overlay"></div>
<dialog class="modal">
  <h5>Modal Title</h5>
  <div>Detailed message...</div>
  <nav class="right-align">
    <button class="border">Close</button>
  </nav>
</dialog>
```

---

## Attributes & Classes

### Container Styles
- `modal`: Center-aligned floating dialog.
- `left`, `right`, `top`, `bottom`: Positions the dialog against the specified screen edge (Drawer pattern).
- `max`: Fullscreen dialog.

### Associated Elements
- `<div class="overlay">`: Background backdrop for modals.
- `blur`: Add to `overlay` for a frosted glass effect.
- `<header>`: Optional top section for titles and close buttons.
- `active`: Class to show/open the dialog.

---

## Navigation & Actions
Dialogs typically use a `<nav class="right-align">` at the bottom for action buttons.

```html
<nav class="right-align">
  <button class="border">Secondary</button>
  <button>Primary</button>
</nav>
```

---

## Rules from Source

1. **Tag:** Use the native HTML `<dialog>` tag.
2. **Action Alignment:** Actions inside the dialog should be right-aligned using `<nav class="right-align">`.
3. **Overlays:** For proper modal behavior, use `<div class="overlay">` immediately before the `<dialog>`.
4. **Drawers:** Positioning classes like `left` or `right` transform the dialog into a navigation drawer or side panel.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Custom positioning via CSS -->
<dialog style="margin: 0 auto">...</dialog>
```

✅ **Do:**
```html
<!-- Use BeerCSS 'modal' class -->
<dialog class="modal">...</dialog>
```

❌ **Don't:**
```html
<!-- Missing action alignment -->
<dialog>
  ...
  <button>OK</button>
</dialog>
```

✅ **Do:**
```html
<dialog>
  ...
  <nav class="right-align">
    <button>OK</button>
  </nav>
</dialog>
```
