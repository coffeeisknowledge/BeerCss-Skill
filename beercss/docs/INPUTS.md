## Inputs

Multiple Styles: border, round, fill
Rule: These styles can be used together, individually, or simply not used.

Sizes: small, medium, large, extra
type input data: text, number, password, file, color, date, time

**Default CSS elements**
- size: medium

Rule: The default CSS elements do not need to be added to the 'class'

### Examples

```html
<div class="field border round">
  <input type="text">
</div>
```

```html
<div class="field border round">
  <input type="text">
  <output>Helper text</output>
</div>
```

```html
<div class="field invalid border round">
  <input type="text">
  <output class="invalid">Error text</output>
</div>
```

```html
<div class="field label border round">
  <input type="text">
  <label>Label</label>
</div>
```

```html
<div class="field label border round">
  <input type="text">
  <label>Label</label>
  <output>Helper text</output>
</div>
```

```html
<div class="field label invalid border round">
  <input type="text">
  <label>Label</label>
  <output class="invalid">Error text</output>
</div>
```

```html
<div class="field label prefix border round">
  <i>search</i>
  <input type="text">
  <label>Label</label>
</div>
```

```html
<div class="field label suffix border round">
  <input type="text">
  <label>Label</label>
  <i class="front">search</i>
</div>
```

```html
<div class="field label prefix suffix border round">
  <i>search</i>
  <input type="text">
  <label>Label</label>
  <i class="front">search</i>
</div>
```

### Custom Inputs

#### Examples

```html
<div>
  <button class="circle">
    <i>attach_file</i>
  </button>
  <input type="file">
</div>
```

```html
<div>
  <button class="circle">
    <i>palette</i>
  </button>
  <input type="color">
</div>
```

```html
<div>
  <button class="circle">
    <i>today</i>
  </button>
  <input type="date">
</div>
```

```html
<div>
  <button class="circle">
    <i>schedule</i>
  </button>
  <input type="time">
</div>
```

```html
<div>
  <button>
    <i>attach_file</i>
    <span>File</span>
  </button>
  <input type="file">
</div>
```

```html
<div>
  <button>
    <i>palette</i>
    <span>Color</span>
  </button>
  <input type="color">
</div>
```

```html
<div>
  <button>
    <i>today</i>
    <span>Date</span>
  </button>
  <input type="date">
</div>
```

```html
<div>
  <button>
    <i>schedule</i>
    <span>Time</span>
  </button>
  <input type="time">
</div>
```
