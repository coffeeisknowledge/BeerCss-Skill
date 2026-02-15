# Typography

Expert guidance for BeerCSS typography based on official documentation.

Source: `beercss/docs/TYPOGRAPHY.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Headings (Display & Headline)

**Standard Sizes:**
```html
<h1>Display (h1)</h1>
<h2>Display (h2)</h2>
<h3>Display (h3)</h3>
<h4>Headline (h4)</h4>
<h5>Headline (h5)</h5>
<h6>Headline (h6)</h6>
```

**Large Variations:**
```html
<h1 class="large">Large Display</h1>
<h5 class="large">Large Headline</h5>
```

---

## Formatting Utilities

- `link`: Class for custom link styling: `<a class="link">Link</a>`.
- `italic`: `class="italic"`.
- `bold`: `class="bold"`.
- `underline`, `overline`: Classes for text decoration.
- `upper`, `lower`, `capitalize`: Text transformation classes.
- `small-text`, `medium-text`, `large-text`: Font size helpers.

### Semantic Tags
- `<code>`: Inline code.
- `<pre>`: Preformatted block.
- `<blockquote>`: Quotations.
- `<em>`, `<strong>`, `<b>`: Standard formatting tags.

---

## Line Spacing

Applied to a parent container to control the line height of its children.

- `no-line`: Compact.
- `tiny-line`.
- `small-line`: Default (no class needed).
- `medium-line`.
- `large-line`.
- `extra-line`.

```html
<div class="large-line">
  <p>Paragraph with generous line spacing...</p>
</div>
```

---

## Rules from Source

1. **Tag Selection:** Use standard HTML tags (`h1`-`h6`, `p`, `blockquote`, etc.).
2. **Default Size:** `medium` is the default for display/headline sizes and line spacing.
3. **Headlines:** `h1`-`h3` are categorized as **Display**, while `h4`-`h6` are **Headline**.
4. **Code Blocks:** Wrap `<code>` inside `<pre>` for blocks of code.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Redundant default line spacing -->
<div class="small-line">
  <p>Text</p>
</div>
```

✅ **Do:**
```html
<div>
  <p>Text</p>
</div>
```
