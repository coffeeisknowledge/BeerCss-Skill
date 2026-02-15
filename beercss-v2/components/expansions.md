# Expansions

Expert guidance for BeerCSS expansions (accordions) based on official documentation.

Source: `beercss/docs/EXPANSIONS.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Expansion Patterns

**Basic Expansion:**
```html
<details>
  <summary>Click to expand</summary>
  <p>Expanded content goes here.</p>
</details>
```

**Custom Trigger Expansion:**
```html
<details>
  <summary>
    <button class="transparent">
      <span>Options</span>
      <i>expand_more</i>
    </button>
  </summary>
  <article>
    <p>Content inside a card-like expansion.</p>
  </article>
</details>
```

---

## Nested Expansions

Expansions can be nested for hierarchical content.

```html
<details>
  <summary>Parent Level</summary>
  <details>
    <summary>Child Level</summary>
    <p>Hierarchical content.</p>
  </details>
</details>
```

---

## Rules from Source

1. **Tag Selection:** Use the native HTML `<details>` and `<summary>` tags.
2. **Custom Summaries:** You can nest buttons, icons, or complex layouts inside the `<summary>` tag.
3. **Nesting:** BeerCSS supports multiple levels of nesting for expansions.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Custom JavaScript based accordions -->
<div class="accordion">...</div>
```

✅ **Do:**
```html
<details>
  <summary>Header</summary>
  ...
</details>
```
