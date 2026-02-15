# Form Controls Reference

Detailed reference for all user input components in BeerCSS.

## Input

### Purpose
Used for single-line text input from the user.

### Basic Pattern
```html
<div class="field label border">
  <input type="text">
  <label>Label</label>
</div>
```

### Variations
- **Filled (Default):** `class="field label border"`
- **Outlined:** `class="field label outline"`
- **With Prefix Icon:**
  ```html
  <div class="field label prefix border">
    <i>search</i>
    <input type="text">
    <label>Search</label>
  </div>
  ```
- **With Suffix Icon:**
  ```html
  <div class="field label suffix border">
    <input type="password">
    <label>Password</label>
    <i>visibility</i>
  </div>
  ```

### States
- **Active:** Add `class="active"` to input and label (managed automatically by `beer.min.js`).
- **Invalid:** Add `class="invalid"` to the `field` container.
- **Disabled:** Add `disabled` attribute to the `input`.

### Accessibility
- Always use a `<label>` inside the field.
- Ensure `id` on input matches `for` on label (if using explicit labels).

---

## Textarea

### Purpose
Used for multi-line text input.

### Basic Pattern
```html
<div class="field label border">
  <textarea></textarea>
  <label>Comments</label>
</div>
```

### Variations
- **Auto-resize:** Enabled by default (pure CSS in Chromium).
- **Fixed Height:** Define `rows` attribute.

---

## Select

### Purpose
Allows users to choose one option from a dropdown list.

### Basic Pattern
```html
<div class="field label border">
  <select>
    <option disabled selected>Pick one</option>
    <option>Option 1</option>
    <option>Option 2</option>
  </select>
  <label>Category</label>
</div>
```

---

## Checkbox

### Purpose
Allows selecting one or more items from a set.

### Basic Pattern
```html
<label class="checkbox">
  <input type="checkbox">
  <span>Option label</span>
</label>
```

### Variations
- **Icon variant:**
  ```html
  <label class="checkbox icon">
    <input type="checkbox">
    <span>
      <i>close</i>
      <i>done</i>
    </span>
  </label>
  ```

---

## Radio

### Purpose
Allows selecting exactly one option from a set.

### Basic Pattern
```html
<label class="radio">
  <input type="radio" name="group1">
  <span>Option label</span>
</label>
```

---

## Switch

### Purpose
Toggles a single setting on or off.

### Basic Pattern
```html
<label class="switch">
  <input type="checkbox">
  <span>Label</span>
</label>
```

---

## Slider

### Purpose
Allows selecting a value from a range.

### Basic Pattern
```html
<div class="slider">
  <input type="range">
  <span></span>
</div>
```

### Variations
- **With Tooltip:** Add `<div class="tooltip"></div>` inside.
- **With Icon:** Use `medium`, `large` or `extra` helpers on the slider and place icon inside `span`.
