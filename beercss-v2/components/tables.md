# Tables

Expert guidance for BeerCSS tables based on official documentation.

Source: `beercss/docs/TABLES.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Standard Table Patterns

**Basic Table:**
```html
<table>
  <thead>
    <tr>
      <th>Header</th>
      <th>Header</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cell</td>
      <td>Cell</td>
    </tr>
  </tbody>
</table>
```

**Striped Table:**
```html
<table class="stripes">
  ...
</table>
```

**Bordered Table:**
```html
<table class="border">
  ...
</table>
```

---

## Attributes & Classes

### Container Styles (Element: `<table>`)
- `stripes`: Alternating row colors.
- `border`: Adds borders around the table and cells.
- `center-align`, `right-align`: Alignment of text within cells.
- `no-space`, `small-space` (default), `medium-space`, `large-space`: Padding within cells.

### Section Styles
- `<thead class="fixed">`: Fixes the header during scrolling.
- `<tfoot class="fixed">`: Fixes the footer during scrolling.

---

## Scrollable Tables

To create a scrollable table with a fixed header, wrap the table in a scrollable container.

```html
<div class="medium-height scroll surface">
  <table class="border">
    <thead class="fixed">
      <tr>
        <th>Fixed Header</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Data...</td>
      </tr>
      <!-- Many rows here -->
    </tbody>
  </table>
</div>
```

---

## Rules from Source

1. **Tag Selection:** Use standard HTML table tags: `<table>`, `<thead>`, `<tbody>`, `<tfoot>`, `<tr>`, `<th>`, `<td>`.
2. **Alignment:** Default alignment is `left-align`. Use classes on the `table` tag to align all cells.
3. **Spacing:** Default spacing is `small-space`.
4. **Scrolling:** For `fixed` headers/footers to work, the parent container must have the `scroll` class and a defined height (e.g., `medium-height`).

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Redundant alignment/spacing classes -->
<table class="left-align small-space">
```

✅ **Do:**
```html
<!-- Use defaults -->
<table>
```

❌ **Don't:**
```html
<!-- Trying to fix header without a scrollable parent -->
<table class="border">
  <thead class="fixed">...</thead>
</table>
```

✅ **Do:**
```html
<div class="scroll medium-height">
  <table class="border">
    <thead class="fixed">...</thead>
  </table>
</div>
```
