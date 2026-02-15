# Badges

Expert guidance for BeerCSS badges based on official documentation.

Source: `beercss/docs/BADGES.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Badge Patterns

**Dot Badge (Minimal):**
```html
<a>
  <i>notifications</i>
  <span class="badge min"></span>
</a>
```

**Numeric Badge:**
```html
<a>
  <i>mail</i>
  <span class="badge">12</span>
</a>
```

**Text Badge:**
```html
<a>
  <i>chat</i>
  <span class="badge">New</span>
</a>
```

---

## Attributes & Classes

### Styles
- `badge`: Base class for all badges.
- `min`: Small dot without content.
- `primary`, `secondary`, `tertiary`: MD3 semantic color backgrounds.
- `border`: Outlined style (use with `primary-border primary-text` for semantic colors).
- `no-round`: Square corners (default is round).
- `none`: Inline badge (no absolute positioning).

### Positioning (Relative to parent)
- Default: Top-Right.
- `top left`: Top-Left.
- `bottom left`: Bottom-Left.
- `bottom right`: Bottom-Right.

---

## Rules from Source

1. **Tag Selection:** Badges are implemented using a `<span class="badge">` inside a relative parent (like `<a>`, `<button>`, or `.chip`).
2. **Semantic Colors:** Use `primary`, `secondary`, or `tertiary` for background colors. For bordered variants, use the specific border/text helper combination (e.g., `badge border primary-border primary-text`).
3. **Inline Badges:** Use `class="badge none"` if the badge should be placed as a standard element within the parent's flow instead of being pinned to a corner.
4. **Minimal Badges:** The `min` class is specifically for notification dots without text.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Badge outside of its context -->
<span class="badge">1</span>
<i>home</i>
```

✅ **Do:**
```html
<!-- Badge inside a relative parent -->
<a>
  <i>home</i>
  <span class="badge">1</span>
</a>
```
