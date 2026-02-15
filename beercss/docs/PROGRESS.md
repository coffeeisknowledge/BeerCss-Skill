## Progress

Material Expressive Style: wavy

percent/value: 0, 30, 60, 100
style: default, light-green, orange

**Default CSS elements**
- style: default

Rule: The default CSS elements do not need to be added to the 'class'

### Linear Progress

Examples:

```html
<progress></progress>
```

```html
<progress value="30" max="100"></progress>
```

```html
<progress class="wavy"></progress>
```

```html
<progress class="wavy" value="30" max="100"></progress>
```

### Circular Progress

Examples:

```html
<progress class="circle"></progress>
```

```html
<progress class="circle" value="30" max="100"></progress>
```

```html
<progress class="circle wavy"></progress>
```

```html
<progress class="circle wavy" value="30" max="100"></progress>
```

### Custom Progress

Examples:

```html
<article>
  <progress class="max" value="30" max="100"></progress>
  <h5>Card</h5>
</article>
```

```html
<button class="chip">
  <progress class="max" value="30" max="100"></progress>
  <span>Chip</span>
</button>
```

```html
<button>
  <progress class="max" value="30" max="100"></progress>
  <span>Button</span>
</button>
```

```html
<div class="field border prefix">
  <progress class="circle"></progress>
  <input>
</div>
```
