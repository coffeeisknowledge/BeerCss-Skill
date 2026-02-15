# Tooltips

Expert guidance for BeerCSS tooltips based on official documentation.

Source: `beercss/docs/TOOLTIPS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Tooltip Patterns

**Basic Tooltip (Inside element):**
```html
<button>
  <i>help</i>
  <span class="tooltip">Helpful info</span>
</button>
```

**Positioned Tooltip:**
```html
<button>
  <i>arrow_back</i>
  <span class="tooltip left">Go back</span>
</button>
```

**Rich Tooltip (Multiple elements):**
```html
<div>
  <button>More info</button>
  <div class="tooltip max">
    <p>Detailed explanation with multiple lines and actions.</p>
    <nav>
      <button>Learn more</button>
    </nav>
  </div>
</div>
```

---

## Attributes & Classes

### Positions
- Default: Bottom.
- `top`, `bottom`, `left`, `right`.

### Styles
- `tooltip`: Base class.
- `max`: Fills width (used for rich/content-heavy tooltips).

### Spacing
- `no-space`, `small-space` (default), `medium-space`, `large-space`.

---

## Rules from Source

1. **Tag Selection:** Use a `<span>` for simple text tooltips or a `<div>` for rich content tooltips.
2. **Nesting:** For simple tooltips, nest the `span.tooltip` inside the trigger element. For rich tooltips, place the `div.tooltip` as a sibling to the trigger inside a common parent.
3. **Trigger:** The tooltip is automatically triggered when hovering over its parent or sibling (depending on nesting).
4. **Default Spacing:** `small-space` is the default. Do not add it explicitly unless needed for overrides.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Tooltip as a top-level element (won't know when to show) -->
<span class="tooltip">Missing parent</span>
```

✅ **Do:**
```html
<!-- Tooltip inside its trigger parent -->
<button>
  <span>Trigger</span>
  <span class="tooltip">Correct context</span>
</button>
```
