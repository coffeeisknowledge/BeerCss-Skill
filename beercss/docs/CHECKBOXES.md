## Checkboxes

Rule: It does not feature any distinctive styles or CSS elements. Use elements exactly as they are in the examples.

### Default Checkboxes examples

Checkbox:

```html
<label class="checkbox">
  <input type="checkbox">
  <span></span>
</label>
```

Checkbox with text:

```html
<label class="checkbox">
  <input type="checkbox">
  <span>Enabled</span>
</label>
```

Disable Checkbox with text:

```html
<label class="checkbox">
  <input type="checkbox" disabled>
  <span>Disabled</span>
</label>
```

Checked Disable Checkbox with text:

```html
<label class="checkbox">
  <input type="checkbox" checked disabled>
  <span>Disabled</span>
</label>
```

Small Checkbox:

```html
<label class="checkbox small">
  <input type="checkbox">
  <span></span>
</label>
```

Default Checkbox:

```html
<label class="checkbox">
  <input type="checkbox">
  <span></span>
</label>
```

Large Checkbox:

```html
<label class="checkbox large">
  <input type="checkbox">
  <span></span>
</label>
```

Extra Checkbox:

```html
<label class="checkbox extra">
  <input type="checkbox">
  <span></span>
</label>
```

### Checkbox with icons examples

Icon Checkbox:

```html
<label class="checkbox icon">
  <input type="checkbox">
  <span>
    <i>close</i>
    <i>done</i>
  </span>
</label>
```

Image Checkbox:

```html
<label class="checkbox icon">
  <input type="checkbox">
  <span>
    <i>
      <img src="/favicon.png">
    </i>
    <i>
      <img src="/beer-and-woman.svg">
    </i>
  </span>
</label>
```

SVG Checkbox:

```html
<label class="checkbox icon">
  <input type="checkbox">
  <span>
    <i>
      <svg viewBox="0 0 24 24">
        <path d="M19,15H23V3H19M15,3H6C5.17,3 4.46,3.5 4.16,4.22L1.14,11.27C1.05,11.5 1,11.74 1,12V14A2,2 0 0,0 3,16H9.31L8.36,20.57C8.34,20.67 8.33,20.77 8.33,20.88C8.33,21.3 8.5,21.67 8.77,21.94L9.83,23L16.41,16.41C16.78,16.05 17,15.55 17,15V5C17,3.89 16.1,3 15,3Z"></path>
      </svg>
    </i>
    <i>
      <svg viewBox="0 0 24 24">
        <path d="M23,10C23,8.89 22.1,8 21,8H14.68L15.64,3.43C15.66,3.33 15.67,3.22 15.67,3.11C15.67,2.7 15.5,2.32 15.23,2.05L14.17,1L7.59,7.58C7.22,7.95 7,8.45 7,9V19A2,2 0 0,0 9,21H18C18.83,21 19.54,20.5 19.84,19.78L22.86,12.73C22.95,12.5 23,12.26 23,12V10M1,21H5V9H1V21Z"></path>
      </svg>
    </i>
  </span>
</label>
```

### Field Elements examples

Field Midle Align Chexbox:

```html
<div class="field middle-align">
  <nav>
    <label class="checkbox">
      <input type="checkbox">
      <span>Item 1</span>
    </label>
    <label class="checkbox">
      <input type="checkbox">
      <span>Item 2</span>
    </label>
    <label class="checkbox">
      <input type="checkbox">
      <span>Item 3</span>
    </label>
  </nav>
</div>
```

Field Midle Align Chexbox with Helper Text:

```html
<div class="field middle-align">
  <nav>
    <label class="checkbox">
      <input type="checkbox">
      <span>Item 1</span>
    </label>
    <label class="checkbox">
      <input type="checkbox">
      <span>Item 2</span>
    </label>
    <label class="checkbox">
      <input type="checkbox">
      <span>Item 3</span>
    </label>
  </nav>
  <output>Helper text</output>
</div>
```

Field Midle Align Chexbox with Error Text:

```html
<div class="field middle-align invalid">
  <nav>
    <label class="checkbox">
      <input type="checkbox">
      <span>Item 1</span>
    </label>
    <label class="checkbox">
      <input type="checkbox">
      <span>Item 2</span>
    </label>
    <label class="checkbox">
      <input type="checkbox">
      <span>Item 3</span>
    </label>
  </nav>
  <output class="invalid">Error text</output>
</div>
```
