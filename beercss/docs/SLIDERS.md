## Sliders

Sliders let users make selections from a range of values. Default range is 0-100.

### Element

```html
<div class="slider">
  <input type="range">
  <span></span>
</div>
```

### Examples

Default:

```html
<div class="slider">
  <input type="range" value="25">
  <span></span>
</div>
```

```html
<div class="slider">
  <input type="range" value="5" min="4" max="8">
  <span></span>
</div>
```

```html
<div class="slider">
  <input type="range" value="25">
  <input type="range" value="50">
  <span></span>
</div>
```

```html
<div class="slider">
  <input type="range" value="25" disabled>
  <span></span>
</div>
```


### Value indicator example

Default:

```html
<div class="slider">
  <input type="range" value="25">
  <span></span>
  <span class="tooltip"></span>
</div>
```

```html
<div class="slider">
  <input type="range" value="5" min="4" max="8">
  <span></span>
  <span class="tooltip"></span>
</div>
```

```html
<div class="slider">
  <input type="range" value="25">
  <input type="range" value="50">
  <span></span>
  <span class="tooltip"></span>
  <span class="tooltip"></span>
</div>
```

```html
<div class="slider">
  <input type="range" value="25" disabled>
  <span></span>
  <span class="tooltip"></span>
</div>
```

Bottom:

```html
<div class="slider">
  <input type="range" value="25">
  <span></span>
  <span class="tooltip bottom"></span>
</div>
```

```html
<div class="slider">
  <input type="range" value="5" min="4" max="8">
  <span></span>
  <span class="tooltip bottom"></span>
</div>
```

```html
<div class="slider">
  <input type="range" value="25">
  <input type="range" value="50">
  <span></span>
  <span class="tooltip bottom"></span>
  <span class="tooltip bottom"></span>
</div>
```

```html
<div class="slider">
  <input type="range" value="25" disabled>
  <span></span>
  <span class="tooltip bottom"></span>
</div>
```

### Inset icon example

The icon will show only with `tiny`, `small`, `medium`, `large` or `extra` helpers.

```html
<div class="slider medium">
  <input type="range">
  <span>
    <i>volume_up</i>
  </span>
</div>
```

```html
<div class="slider medium">
  <input type="range">
  <span>
    <i>add</i>
  </span>
</div>
```

```html
<div class="slider medium">
  <input type="range" value="25">
  <span>
    <i>sunny</i>
  </span>
</div>
```

### In field elements example

```html
<div class="field middle-align">
  <div class="slider">
    <input type="range" value="25">
    <span></span>
  </div>
  <output>Helper</output>
</div>
```

```html
<div class="field middle-align">
  <div class="slider">
    <input type="range" value="25">
    <span></span>
  </div>
  <output class="invalid">Error text</output>
</div>
```

```html
<div class="field middle-align prefix suffix">
  <nav>
    <i>sunny</i>
    <div class="slider">
      <input type="range" value="25">
      <span></span>
    </div>
    <i>rainy</i>
  </nav>
  <output>Helper</output>
</div>
```

### Custom slider example

```html
<article>
  <div class="slider max">
    <input type="range">
    <span></span>
  </div>
<article>

```

```html
<div class="small-width small-height round fill">
  <div class="slider max vertical">
    <input type="range" value="30" max="100">
    <span></span>
  </div>
</div>
```
