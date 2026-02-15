## Tooltip

 space: 'no-space', 'small-space', 'medium-space', 'large-space'

**Default CSS elements**
space: 'small-place'

Rule: The default CSS elements do not need to be added to the 'class'

### Default Examples

```html
<button class="chip round">
  <span>Plain tooltip</span>
  <span class="tooltip">Tooltip</span>
</button>
```

```html
<button class="chip circle">
  <i>arrow_back</i>
  <span class="tooltip left">Tooltip</span>
</button>
```

```html
<button class="chip circle">
  <i>arrow_upward</i>
  <span class="tooltip top">Tooltip</span>
</button>
```

```html
<button class="chip circle">
  <i>arrow_downward</i>
  <span class="tooltip bottom">Tooltip</span>
</button>
```

```html
<button class="chip circle">
  <i>arrow_forward</i>
  <span class="tooltip right">Tooltip</span>
</button>
```

```html
<div>
  <button class="chip round">
    <span>Wrapped tooltip</span>
  </button>
  <div class="tooltip">Tooltip</div>
</div>
```

```html
<div>
  <button class="chip round">
    <span>Rich tooltip</span>
  </button>
  <div class="tooltip max">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button>Button</button>
    </nav>
  </div>
</div>
```


### Custom Examples

 space: 'no-space' or 'medium-space' or 'large-space'

```html
<button class="chip round">
  <span>Plain tooltip</span>
  <span class="tooltip medium-space">Tooltip</span>
</button>
```

```html
<button class="chip circle">
  <i>arrow_back</i>
  <span class="tooltip left medium-space">Tooltip</span>
</button>
```

```html
<button class="chip circle">
  <i>arrow_upward</i>
  <span class="tooltip top medium-space">Tooltip</span>
</button>
```

```html
<button class="chip circle">
  <i>arrow_downward</i>
  <span class="tooltip bottom medium-space">Tooltip</span>
</button>
```

```html
<button class="chip circle">
  <i>arrow_forward</i>
  <span class="tooltip right medium-space">Tooltip</span>
</button>
```

```html
<div>
  <button class="chip round">
    <span>Wrapped tooltip</span>
  </button>
  <div class="tooltip medium-space">Tooltip</div>
</div>
```

```html
<div>
  <button class="chip round">
    <span>Rich tooltip</span>
  </button>
  <div class="tooltip max medium-space">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button>Button</button>
    </nav>
  </div>
</div>
```
