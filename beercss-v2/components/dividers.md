# Dividers

Expert guidance for BeerCSS dividers based on official documentation.

Source: `beercss/docs/DIVIDERS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Divider Patterns

**Default Divider:**
```html
<hr>
```

**Small Divider:**
```html
<hr class="small">
```

**Medium Divider:**
```html
<hr class="medium">
```

**Large Divider:**
```html
<hr class="large">
```

---

## Rules from Source

1. **Tag Selection:** Use the native HTML `<hr>` tag for dividers.
2. **Default Size:** The default `hr` doesn't need a size class. Use `small`, `medium`, or `large` for specific thickness/spacing requirements.
3. **Context:** Dividers are used to separate content sections or list items.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Redundant default class -->
<hr class="default">
```

✅ **Do:**
```html
<hr>
```
