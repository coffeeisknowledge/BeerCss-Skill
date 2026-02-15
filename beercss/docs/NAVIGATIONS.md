## Navigations

### Rows

align: left-align, center-align, right-align

**Default CSS elements**
align: left-align

Rule: The default CSS elements do not need to be added to the 'class'

#### 'center-align'/'right-align' examples

```html
<div class="row center-align">
  <div>min</div>
  <div>min</div>
  <div>min</div>
</div>
```

```html
<div class="row center-align">
  <div>min</div>
  <div>min</div>
  <div class="max">max</div>
</div>
```

```html
<div class="row center-align">
  <div>min</div>
  <div class="max">max</div>
  <div>min</div>
</div>
```

```html
<div class="row center-align">
  <div class="max">max</div>
  <div>min</div>
  <div>min</div>
</div>
```

#### 'left-align' examples

```html
<div class="row">
  <div>min</div>
  <div>min</div>
  <div>min</div>
</div>
```

```html
<div class="row">
  <div>min</div>
  <div>min</div>
  <div class="max">max</div>
</div>
```

```html
<div class="row">
  <div>min</div>
  <div class="max">max</div>
  <div>min</div>
</div>
```

```html
<div class="row">
  <div class="max">max</div>
  <div>min</div>
  <div>min</div>
</div>
```

### Navigations with other elements

align: left-align, center-align, right-align

**Default CSS elements**
align: left-align

Rule: The default CSS elements do not need to be added to the 'class'

#### 'center-align'/'right-align' examples

```html
<nav class="center-align">
  <button>Button</button>
  <button class="chip">Chip</button>
  <i>home</i>
  <img class="circle" src="/beer-and-woman.svg">
</nav>
```

```html
<nav class="center-align">
  <button>Button</button>
  <button class="chip">Chip</button>
  <i>home</i>
  <div class="max">max</div>
  <img class="circle" src="/beer-and-woman.svg">
</nav>
```

```html
<nav class="center-align">
  <button>Button</button>
  <button class="chip">Chip</button>
  <i>home</i>
  <div class="max">max</div>
  <img class="circle" src="/beer-and-woman.svg">
</nav>
```

```html
<nav class="center-align">
  <button>Button</button>
  <div class="max">max</div>
  <button class="chip">Chip</button>
  <i>home</i>
  <img class="circle" src="/beer-and-woman.svg">
</nav>
```

```html
<nav class="center-align">
  <div class="max">max</div>
  <button>Button</button>
  <button class="chip">Chip</button>
  <i>home</i>
  <img class="circle" src="/beer-and-woman.svg">
</nav>
```

#### 'left-align' examples

```html
<nav>
  <button>Button</button>
  <button class="chip">Chip</button>
  <i>home</i>
  <img class="circle" src="/beer-and-woman.svg">
</nav>
```

```html
<nav>
  <button>Button</button>
  <button class="chip">Chip</button>
  <i>home</i>
  <div class="max">max</div>
  <img class="circle" src="/beer-and-woman.svg">
</nav>
```

```html
<nav>
  <button>Button</button>
  <button class="chip">Chip</button>
  <div class="max">max</div>
  <i>home</i>
  <img class="circle" src="/beer-and-woman.svg">
</nav>
```

```html
<nav>
  <button>Button</button>
  <div class="max">max</div>
  <button class="chip">Chip</button>
  <i>home</i>
  <img class="circle" src="/beer-and-woman.svg">
</nav>
```

```html
<nav>
  <div class="max">max</div>
  <button>Button</button>
  <button class="chip">Chip</button>
  <i>home</i>
  <img class="circle" src="/beer-and-woman.svg">
</nav>
```

### Navigation rail/bar

modes: left or right

```html
<nav class="m l max left">
  <header>
    <button class="extra circle transparent">
      <i>menu_open</i>
    </button>
    <button class="extend square round">
      <i>widgets</i>
      <span>Explore</span>
    </button>
  </header>
  <a>
    <i>arrow_back</i>
    <span>Left</span>
  </a>
  <a>
    <i>arrow_forward</i>
    <span>Right</span>
  </a>
  <a>
    <i>checklist_rtl</i>
    <span>RTL</span>
  </a>
  <a>
    <i>checklist</i>
    <span>LTR</span>
  </a>
  <a>
    <i>code</i>
    <span>Code</span>
  </a>
</nav>
```

### Navigation tabbed

size: small, medium, large
page transition: 'page default', 'page left', 'page right'

**Default CSS elements**
size: medium
page transition: 'page default'

Rule: The default CSS elements do not need to be added to the 'class'

### Default example

```html
<div>
  <nav class="tabbed">
    <a class="active">
      <i>info</i>
      <span>Overview</span>
    </a>
    <a>
      <i>style</i>
      <span>Specs</span>
    </a>
    <a>
      <i>design_services</i>
      <span>Guidelines</span>
    </a>
    <a>
      <i>accessibility_new</i>
      <span>Acessibility</span>
    </a>
  </nav>
  <div class="page padding active">
    <h5>Overview</h5>
  </div>
  <div class="page padding">
    <h5>Specs</h5>
  </div>
  <div class="page padding">
    <h5>Guidelines</h5>
  </div>
  <div class="page padding">
    <h5>Acessibility</h5>
  </div>
</div>
```

### 'small', 'large'/'page left' 'page right' example

```html
<div>
  <nav class="tabbed small">
    <a class="active">
      <i>info</i>
      <span>Overview</span>
    </a>
    <a>
      <i>style</i>
      <span>Specs</span>
    </a>
    <a>
      <i>design_services</i>
      <span>Guidelines</span>
    </a>
    <a>
      <i>accessibility_new</i>
      <span>Acessibility</span>
    </a>
  </nav>
  <div class="page padding active right">
    <h5>Overview</h5>
  </div>
  <div class="page padding right">
    <h5>Specs</h5>
  </div>
  <div class="page padding right">
    <h5>Guidelines</h5>
  </div>
  <div class="page padding right">
    <h5>Acessibility</h5>
  </div>
</div>
```

