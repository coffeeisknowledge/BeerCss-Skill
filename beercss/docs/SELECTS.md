## Selects

Multiple Styles: border, round, fill
Rule: These styles can be used together, individually, or simply not used.

Sizes: small, medium, large, extra

**Default CSS elements**
- size: medium

Rule: The default CSS elements do not need to be added to the 'class'

### Examples

```html
<div class="field suffix border">
  <select>
    <option>Item 1</option>
    <option>Item 2</option>
    <option>Item 3</option>
  </select>
  <i>arrow_drop_down</i>
</div>
```

```html
<div class="field suffix border">
  <select>
    <option>Item 1</option>
    <option>Item 2</option>
    <option>Item 3</option>
  </select>
  <i>arrow_drop_down</i>
  <output>Helper text</output>
</div>
```

```html
<div class="field suffix invalid border">
  <select>
    <option>Item 1</option>
    <option>Item 2</option>
    <option>Item 3</option>
  </select>
  <i>arrow_drop_down</i>
  <output class="invalid">Error text</output>
</div>
```

```html
<div class="field label suffix border">
  <select>
    <option>Item 1</option>
    <option>Item 2</option>
    <option>Item 3</option>
  </select>
  <label>Label</label>
  <i>arrow_drop_down</i>
</div>
```

```html
<div class="field label suffix border">
  <select>
    <option>Item 1</option>
    <option>Item 2</option>
    <option>Item 3</option>
  </select>
  <label>Label</label>
  <i>arrow_drop_down</i>
  <output>Helper text</output>
</div>
```

```html
<div class="field label suffix invalid border">
  <select>
    <option>Item 1</option>
    <option>Item 2</option>
    <option>Item 3</option>
  </select>
  <label>Label</label>
  <i>arrow_drop_down</i>
  <output class="invalid">Error text</output>
</div>
```

