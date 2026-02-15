# Get started

## From CDN

```
<link href="https://cdn.jsdelivr.net/npm/beercss@4.0.2/dist/cdn/beer.min.css" rel="stylesheet">
<script type="module" src="https://cdn.jsdelivr.net/npm/beercss@4.0.2/dist/cdn/beer.min.js"></script>
<script type="module" src="https://cdn.jsdelivr.net/npm/material-dynamic-colors@1.1.4/dist/cdn/material-dynamic-colors.min.js"></script>
```

## From NPM

```
// installing
npm i beercss
npm i material-dynamic-colors

// importing
import "beercss";
import "material-dynamic-colors";
```

*Use  material-dynamic-colors  lib only for theme changes at runtime with ui("theme").

---

## Main Layouts

### Compact Example

```html
<nav class="bottom">
  <a>
    <i>home</i>
    <div>Home</div>
  </a>
  <a>
    <i>search</i>
    <div>Search</div>
  </a>
  <a>
    <i>share</i>
    <div>share</div>
  </a>
</nav>
<main class="responsive">
  <h3>Compact</h3>
</main>
```

### Medium Example

```html
<nav class="left">
  <a>
    <i>home</i>
    <div>Home</div>
  </a>
  <a>
    <i>search</i>
    <div>Search</div>
  </a>
  <a>
    <i>share</i>
    <div>share</div>
  </a>
</nav>
<main class="responsive">
  <h3>Medium</h3>
</main>
```

### Expanded Example

```html
<nav class="left max">
  <a>
    <i>home</i>
    <div>Home</div>
  </a>
  <a>
    <i>search</i>
    <div>Search</div>
  </a>
  <a>
    <i>share</i>
    <div>share</div>
  </a>
</nav>
<main class="responsive">
  <h3>Expanded</h3>
</main>
```

### Multi panes Example

```html
<nav class="left">
  <a>
    <i>home</i>
    <div>Home</div>
  </a>
  <a>
    <i>search</i>
    <div>Search</div>
  </a>
  <a>
    <i>share</i>
    <div>share</div>
  </a>
</nav>
<main class="responsive">
  <div class="grid">
    <div class="s6">
      <h3>Pane 1</h3>
    </div>
    <div class="s6">
      <h3>Pane 2</h3>
    </div>
  </div>
</main>
```

### Custom Example

```html
<nav class="left">
  <a>
    <i>home</i>
    <div>Home</div>
  </a>
  <a>
    <i>search</i>
    <div>Search</div>
  </a>
  <a>
    <i>share</i>
    <div>share</div>
  </a>
</nav>
<main class="responsive">
  <div class="grid">
    <div class="s12 m12 l6">
      <h3>Pane 1</h3>
    </div>
    <div class="s12 m12 l6">
      <h3>Pane 2</h3>
    </div>
    <div class="s12 m12 l6">
      <h3>Pane 3</h3>
    </div>
    <div class="s12 m12 l6">
      <h3>Pane 4</h3>
    </div>
  </div>
</main>
```

---

## App Bars

### Top App Bars

styles: default, fill, primary, secondary, tertiary

#### Default Style

##### Type 1 Example:

```html
<header>
  <nav>
    <button class="circle transparent">
      <i>menu</i>
    </button>
    <h6 class="max center-align">Headline</h6>
    <button class="circle transparent">
      <img class="responsive" src="/favicon.png">
    </button>
  </nav>
</header>
```


##### Type 2 Example:

```html
<header>
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <h6 class="max">Headline</h6>
    <button class="circle transparent">
      <i>attach_file</i>
    </button>
    <button class="circle transparent">
      <i>today</i>
    </button>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
</header>
```

##### Type 3 Example:

```html
<header>
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <div class="max"></div>
    <button class="circle transparent">
      <i>attach_file</i>
    </button>
    <button class="circle transparent">
      <i>today</i>
    </button>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
  <div class="small-padding">
    <h5>Headline</h5>
  </div>
</header>
```

##### Type 4 Example:

```html
<header>
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <div class="max"></div>
    <button class="circle transparent">
      <i>attach_file</i>
    </button>
    <button class="circle transparent">
      <i>today</i>
    </button>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
  <div class="small-padding">
    <h4>Headline</h4>
  </div>
</header>
```

#### Fill Style

##### Type 1 Example:

```html
<header class="fill">
  <nav>
    <button class="circle transparent">
      <i>menu</i>
    </button>
    <h6 class="max center-align">Headline</h6>
    <button class="circle transparent">
      <img class="responsive" src="/favicon.png">
    </button>
  </nav>
</header>
```

##### Type 2 Example:

```html
<header class="fill">
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <h6 class="max">Headline</h6>
    <button class="circle transparent">
      <i>attach_file</i>
    </button>
    <button class="circle transparent">
      <i>today</i>
    </button>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
</header>
```

##### Type 3 Example:

```html
<header class="fill">
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <div class="max"></div>
    <button class="circle transparent">
      <i>attach_file</i>
    </button>
    <button class="circle transparent">
      <i>today</i>
    </button>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
  <div class="small-padding">
    <h5>Headline</h5>
  </div>
</header>
```

##### Type 4 Example:

```html
<header class="fill">
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <div class="max"></div>
    <button class="circle transparent">
      <i>attach_file</i>
    </button>
    <button class="circle transparent">
      <i>today</i>
    </button>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
  <div class="small-padding">
    <h4>Headline</h4>
  </div>
</header>
```


#### Primary, Secondary, Tertiary Style

Use: "primary-container" or "secondary-container" or "tertiary-container"

##### Type 1 Example:

```html
<header class="primary-container">
  <nav>
    <button class="circle transparent">
      <i>menu</i>
    </button>
    <h6 class="max center-align">Headline</h6>
    <button class="circle transparent">
      <img class="responsive" src="/favicon.png">
    </button>
  </nav>
</header>```

##### Type 2 Example:

```html
<header class="primary-container">
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <h6 class="max">Headline</h6>
    <button class="circle transparent">
      <i>attach_file</i>
    </button>
    <button class="circle transparent">
      <i>today</i>
    </button>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
</header>
```

##### Type 3 Example:

```html
<header class="primary-container">
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <div class="max"></div>
    <button class="circle transparent">
      <i>attach_file</i>
    </button>
    <button class="circle transparent">
      <i>today</i>
    </button>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
  <div class="small-padding">
    <h5>Headline</h5>
  </div>
</header>```

##### Type 4 Example:

```html
<header class="primary-container">
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <div class="max"></div>
    <button class="circle transparent">
      <i>attach_file</i>
    </button>
    <button class="circle transparent">
      <i>today</i>
    </button>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
  <div class="small-padding">
    <h4>Headline</h4>
  </div>
</header>
```

### Bottom App Bars

styles: default, fill, primary, secondary, tertiary

#### Default Style Example

```html
<footer>
  <nav>
    <button class="circle transparent">
      <i>check_box</i>
    </button>
    <button class="circle transparent">
      <i>brush</i>
    </button>
    <button class="circle transparent">
      <i>mic</i>
    </button>
    <button class="circle transparent">
      <i>image</i>
    </button>
    <div class="max"></div>
    <button class="square round extra primary">
      <i>add</i>
    </button>
  </nav>
</footer>
```


#### Fill Style Example

```html
<footer class="fill">
  <nav>
    <button class="circle transparent">
      <i>check_box</i>
    </button>
    <button class="circle transparent">
      <i>brush</i>
    </button>
    <button class="circle transparent">
      <i>mic</i>
    </button>
    <button class="circle transparent">
      <i>image</i>
    </button>
    <div class="max"></div>
    <button class="square round extra">
      <i>add</i>
    </button>
  </nav>
</footer>
```


#### Primary, Secondary, Tertiary Style Example

Use: "primary-container" or "secondary-container" or "tertiary-container"

```html
<footer class="primary-container">
  <nav>
    <button class="circle transparent">
      <i>check_box</i>
    </button>
    <button class="circle transparent">
      <i>brush</i>
    </button>
    <button class="circle transparent">
      <i>mic</i>
    </button>
    <button class="circle transparent">
      <i>image</i>
    </button>
    <div class="max"></div>
    <button class="square round extra primary">
      <i>add</i>
    </button>
  </nav>
</footer>
```

---

## Badges

### Common Badges

Styles: default, primary, secondary, tertiary

Alignment badge 'span': default, top left, bottom left, bottom right

### Default Style and Default Alignment badge 'span'

#### Examples:

```html
<a>
  <i>home</i>
  <span class="badge min"></span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge">1</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge">10</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge">New</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge no-round">New</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border">New</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border">10</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border">1</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border no-round">New</span>
</a>
```

```html
<button class="circle">
  <i>home</i>
  <span class="badge">1</span>
</button>
```

```html
<button>
  <i>home</i>
  <span class="badge">1</span>
</button>
```

```html
<button class="chip circle">
  <i>home</i>
  <span class="badge">1</span>
</button>
```

```html
<button class="chip">
  <i>home</i>
  <span class="badge">1</span>
</button>
```

### Primary/Secondary/Tertiary Style and Default Alignment badge 'span'

Use: primary or secondary or tertiary

#### Examples:

```html
<a>
  <i>home</i>
  <span class="badge min primary"></span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge primary">1</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge primary">10</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge primary">New</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge no-round primary">New</span>
</a>
```


Use: 'primary-border and primary-text' or 'secondary-border and secondary-text' or 'tertiary-border and tertiary-text'

```html
<a>
  <i>home</i>
  <span class="badge border primary-border primary-text">New</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border primary-border primary-text">10</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border primary-border primary-text">1</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border no-round primary-border primary-text">New</span>
</a>
```


Use: primary or secondary or tertiary

```html
<button class="circle">
  <i>home</i>
  <span class="badge primary">1</span>
</button>
```

```html
<button>
  <i>home</i>
  <span class="badge primary">1</span>
</button>
```

```html
<button class="chip circle">
  <i>home</i>
  <span class="badge primary">1</span>
</button>
```

```html
<button class="chip">
  <i>home</i>
  <span class="badge primary">1</span>
</button>
```


### Primary/Secondary/Tertiary Style and Top-left/Bottom-left/Bottom-right Alignment badge 'span'

Use: 'primary or secondary or tertiary' and 'top left or bottom left or bottom right'

#### Examples:

```html
<a>
  <i>home</i>
  <span class="badge min primary top left"></span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge primary top left">1</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge primary top left">10</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge primary top left">New</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge no-round primary top left">New</span>
</a>
```


Use: 'primary-border and primary-text' or 'secondary-border and secondary-text' or 'tertiary-border and tertiary-text'
Use: 'top left or bottom left or bottom right'

```html
<a>
  <i>home</i>
  <span class="badge border primary-border primary-text top left">New</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border primary-border primary-text top left">10</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border primary-border primary-text top left">1</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border no-round primary-border primary-text top left">New</span>
</a>
```


Use: primary or secondary or tertiary
Use: 'top left or bottom left or bottom right'

```html
<button class="circle">
  <i>home</i>
  <span class="badge primary top left">1</span>
</button>
```

```html
<button>
  <i>home</i>
  <span class="badge primary top left">1</span>
</button>
```

```html
<button class="chip circle">
  <i>home</i>
  <span class="badge primary top left">1</span>
</button>
```

```html
<button class="chip">
  <i>home</i>
  <span class="badge primary top left">1</span>
</button>
```


### Default Style and Top-left/Bottom-left/Bottom-right Alignment badge 'span'

Use: 'top left or bottom left or bottom right'

#### Examples:

```html
<a>
  <i>home</i>
  <span class="badge min top left"></span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge top left">1</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge top left">10</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge top left">New</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge no-round top left">New</span>
</a>
```


Use: 'top left' or 'bottom left' or 'bottom right'

```html
<a>
  <i>home</i>
  <span class="badge border top left">New</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border top left">10</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border top left">1</span>
</a>
```

```html
<a>
  <i>home</i>
  <span class="badge border no-round top left">New</span>
</a>
```


Use: 'top left' or 'bottom left' or 'bottom right'

```html
<button class="circle">
  <i>home</i>
  <span class="badge top left">1</span>
</button>
```

```html
<button>
  <i>home</i>
  <span class="badge top left">1</span>
</button>
```

```html
<button class="chip circle">
  <i>home</i>
  <span class="badge top left">1</span>
</button>
```

```html
<button class="chip">
  <i>home</i>
  <span class="badge top left">1</span>
</button>
```


### Inline Badges

### Examples:

```html
<button>
  <i>home</i>
  <span class="badge none">1</span>
</button>
```

```html
<button>
  <span>Button</span>
  <span class="badge none">1</span>
</button>
```

```html
<button class="chip">
  <i>home</i>
  <span class="badge none">1</span>
</button>
```

```html
<button class="chip">
  <span>Button</span>
  <span class="badge none">1</span>
</button>
```

---

## Buttons

### Common buttons

Styles: default, fill, primary, secondary, tertiary
Sizes: small, medium, large, extra
Elevate: no-elevate, small-elevate, medium-elevate, large-elevate
Orientation: horizontal, vertical

**Default CSS elements**
- style: default
- size: medium
- elevate: no-elevate
- orientation: horizontal

Rule: The default CSS elements do not need to be added to the 'class'

#### Examples 1:

Style: default
Size: small/large/extra
Elevate: no-elevate
Orientation: horizontal

> In this case, it is not necessary to add the 'default' style, the 'no-elevate' elevation, and the 'horizontal' orientation.

```html
<button class="small">Button</button>
```

```html
<button class="small">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="small">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="small">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Rounded Border Button: small-round

```html
<button class="small-round small">Button</button>
```

```html
<button class="small-round small">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="small-round small">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="small-round small">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```


Only Border Button: border

```html
<button class="border small">Button</button>
```

```html
<button class="border small">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="border small">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="border small">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Rounded Border and Only Border Button: 'border small-round'

```html
<button class="border small-round small">Button</button>
```

```html
<button class="border small-round small">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="border small-round small">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="border small-round small">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```


#### Examples 2:

Style: fill
Size: medium
Elevate: small-elevate/large-elevate/
Orientation: vertical

> In this case, it is not necessary to add the 'medium' size.

```html
<button class="fill small-elevate vertical">Button</button>
```

```html
<button class="fill small-elevate vertical">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="fill small-elevate vertical">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="fill small-elevate vertical">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Rounded Border Button: small-round

```html
<button class="small-round fill small-elevate vertical">Button</button>
```

```html
<button class="small-round fill small-elevate vertical">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="small-round fill small-elevate vertical">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="small-round fill small-elevate vertical">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```


Only Border Button: border

```html
<button class="border small-elevate vertical">Button</button>
```

```html
<button class="border small-elevate vertical">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="border small-elevate vertical">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="border small-elevate vertical">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Rounded Border and Only Border Button: 'border small-round'

```html
<button class="border small-round small-elevate vertical">Button</button>
```

```html
<button class="border small-round small-elevate vertical">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="border small-round small-elevate vertical">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="border small-round small-elevate vertical">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```


#### Examples 3:

Style: primary/secondary/tertiary
Size: medium
Elevate: small-elevate/large-elevate
Orientation: horizontal

> In this case, it is not necessary to add the 'medium' Size and the 'horizontal' orientation.

```html
<button class="primary large-elevate">Button</button>
```

```html
<button class="primary large-elevate">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="primary large-elevate">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="primary large-elevate">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Rounded Border Button: small-round

```html
<button class="small-round primary large-elevate">Button</button>
```

```html
<button class="small-round primary large-elevate">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="small-round primary large-elevate">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="small-round primary large-elevate">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```


Only Border Button: border
Can use: 'primary-border primary-text' or 'secondary-border secondary-text' or 'tertiary-border tertiary-text'

```html
<button class="border primary-border primary-text large-elevate">Button</button>
```

```html
<button class="border primary-border primary-text large-elevate">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="border primary-border primary-text large-elevate">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="border primary-border primary-text large-elevate">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Rounded Border and Only Border Button: 'border small-round'
Can use: 'primary-border primary-text' or 'secondary-border secondary-text' or 'tertiary-border tertiary-text'

```html
<button class="border small-round primary-border primary-text large-elevate">Button</button>
```

```html
<button class="border small-round primary-border primary-text large-elevate">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="border small-round primary-border primary-text large-elevate">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```

```html
<button class="border small-round primary-border primary-text large-elevate">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```


### Responsive buttons (falta completar)

Styles: default, fill, primary, secondary, tertiary
Sizes: small, medium, large, extra
Elevate: no-elevate, small-elevate, medium-elevate, large-elevate
Orientation: horizontal, vertical

**Default CSS elements**
- style: default
- size: medium
- elevate: no-elevate
- orientation: horizontal

Rule: The default CSS elements do not need to be added to the 'class'

#### Examples

```html
<button class="responsive">Button</button>
```

```html
<button class="responsive">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="responsive">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```


Rounded Button:

```html
<button class="responsive round">Button</button>
```

```html
<button class="responsive round">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="responsive round">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```


Only Border Button:

```html
<button class="responsive border">Button</button>
```

```html
<button class="responsive border">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="responsive border">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```


Only Border and Rounded Button:

```html
<button class="responsive border round">Button</button>
```

```html
<button class="responsive border round">
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="responsive border round">
  <img src="/favicon.png">
  <span>Button</span>
</button>
```


### FABs buttons (falta completar)

Styles: default, fill, primary, secondary, tertiary
Sizes: small, medium, large, extra
Elevate: no-elevate, small-elevate, medium-elevate, large-elevate

**Default CSS elements**
- style: default
- size: medium
- elevate: no-elevate

Rule: The default CSS elements do not need to be added to the 'class'

#### Examples

Square FAB Button:

```html
<button class="square extra">
  <i>add</i>
</button>
```

Square Rounded FAB Button:

```html
<button class="square round extra">
  <i>add</i>
</button>
```

Circle FAB Button:

```html
<button class="circle extra">
  <i>add</i>
</button>
```

Circle Left-Top Rounded FAB Button:

```html
<button class="circle left-round top-round extra">
  <i>add</i>
</button>
```

Circle Left-Bottom Rounded FAB Button:

```html
<button class="circle left-round bottom-round extra">
  <i>add</i>
</button>
```

Circle Right-Top Rounded FAB Button:

```html
<button class="circle right-round top-round extra">
  <i>add</i>
</button>
```

Circle Right-Bottom Rounded FAB Button:

```html
<button class="circle right-round bottom-round extra">
  <i>add</i>
</button>
```

Circle Left Rounded FAB Button:

```html
<button class="circle left-round extra">
  <i>add</i>
</button>
```

Circle Right Rounded FAB Button:

```html
<button class="circle right-round extra">
  <i>add</i>
</button>
```

Square Only Border FAB Button:

```html
<button class="border square extra">
  <i>add</i>
</button>
```

Square Rounded Only Border FAB Button:

```html
<button class="border square round extra">
  <i>add</i>
</button>
```

Circle Only Border FAB Button:

```html
<button class="border circle extra">
  <i>add</i>
</button>
```

Circle Only Border Left-Top Rounded FAB Button:

```html
<button class="border circle left-round top-round extra">
  <i>add</i>
</button>
```

Circle Only Border Left-Bottom Rounded FAB Button:

```html
<button class="border circle left-round bottom-round extra">
  <i>add</i>
</button>
```

Circle Only Border Right-Top Rounded FAB Button:

```html
<button class="border circle right-round top-round extra">
  <i>add</i>
</button>
```

Circle Only Border Right-Bottom Rounded FAB Button:

```html
<button class="border circle right-round bottom-round extra">
  <i>add</i>
</button>
```

Circle Only Border Left Rounded FAB Button:

```html
<button class="border circle left-round extra">
  <i>add</i>
</button>
```

Circle Only Border Right Rounded FAB Button:

```html
<button class="border circle right-round extra">
  <i>add</i>
</button>
```

Square Image FAB Button:

```html
<button class="border square extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Square Image Rounded FAB Button:

```html
<button class="border square round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Circle Image FAB Button:

```html
<button class="border circle extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Circle Image Left-Top Rounded FAB Button:

```html
<button class="border circle left-round top-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Circle Image Left-Bottom Rounded FAB Button:

```html
<button class="border circle left-round bottom-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Circle Image Right-top Rounded FAB Button:

```html
<button class="border circle right-round top-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Circle Image Right-Bottom Rounded FAB Button:

```html
<button class="border circle right-round bottom-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Circle Image Left Rounded FAB Button:

```html
<button class="border circle left-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Circle Image Right Rounded FAB Button:

```html
<button class="border circle right-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

### Extended FABs Buttons (falta completar)

Styles: default, fill, primary, secondary, tertiary
Elevate: no-elevate, small-elevate, medium-elevate, large-elevate

**Default CSS elements**
- style: default
- elevate: no-elevate

Rule: The default CSS elements do not need to be added to the 'class'

#### Examples

Extend FAB Square Button:

```html
<button class="extend square">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Square Rounded Button:

```html
<button class="extend square round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Button:

```html
<button class="extend circle">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Left-Top Rounded Button:

```html
<button class="extend circle left-round top-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Left-Bottom Rounded Button:

```html
<button class="extend circle left-round bottom-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Right-Top Rounded Button:

```html
<button class="extend circle right-round top-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Right-Bottom Rounded Button:

```html
<button class="extend circle right-round bottom-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Left Rounded Button:

```html
<button class="extend circle left-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Right Rounded Button:

```html
<button class="extend circle right-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Square Only Border Button:

```html
<button class="extend border square">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Square Rounded Only Border Button:

```html
<button class="extend border square round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Only Border Button:

```html
<button class="extend border circle">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Left-Top Only Border Rounded Button:

```html
<button class="extend border circle left-round top-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Left-Bottom Only Border Rounded Button:

```html
<button class="extend border circle left-round bottom-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Right-Top Only Border Rounded Button:

```html
<button class="extend border circle right-round top-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Right-Bottom Only Border Rounded Button:

```html
<button class="extend border circle right-round bottom-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Left Rounded Only Border Rounded Button:

```html
<button class="extend border circle left-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Extend FAB Circle Right Rounded Only Border Rounded Button:

```html
<button class="extend border circle right-round">
  <i>add</i>
  <span>Button</span>
</button>
```

Square Image Extend FAB Button:

```html
<button class="extend border square">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Square Rounded Image Extend FAB Button:

```html
<button class="extend border square round">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Circle Image Extend FAB Button:

```html
<button class="extend border circle">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Circle Image Left-Top Rounded Extend FAB Button:

```html
<button class="extend border circle left-round top-round">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Circle Image Left-Bottom Rounded Extend FAB Button:

```html
<button class="extend border circle left-round bottom-round">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Circle Image Right-Top Rounded Extend FAB Button:

```html
<button class="extend border circle right-round top-round">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Circle Image Right-Bottom Rounded Extend FAB Button:

```html
<button class="extend border circle right-round bottom-round">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Circle Image Left Rounded Extend FAB Button:

```html
<button class="extend border circle left-round">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

Circle Image Right Rounded Extend FAB Button:

```html
<button class="extend border circle right-round">
  <img class="responsive" src="/favicon.png">
  <span>Button</span>
</button>
```

### FABs Menu

#### Examples

FAB Menu Top-Left Button:

```html
<div>
  <button class="extra circle">
    <i>north_east</i>
  </button>
  <menu class="top transparent no-wrap">
    <li>
      <button class="fill">
        <i>search</i>
        <span>Search</span>
      </button>
    </li>
    <li>
      <button class="fill">
        <i>home</i>
        <span>Home</span>
      </button>
    </li>
    <li>
      <button class="fill">
        <i>more_vert</i>
        <span>About us</span>
      </button>
    </li>
  </menu>
</div>
```

FAB Menu Top-Right Button:

```html
<div>
  <button class="extra circle">
    <i>north_west</i>
  </button>
  <menu class="top transparent no-wrap left right-align">
    <li>
      <button class="fill">
        <i>search</i>
        <span>Search</span>
      </button>
    </li>
    <li>
      <button class="fill">
        <i>home</i>
        <span>Home</span>
      </button>
    </li>
    <li>
      <button class="fill">
        <i>more_vert</i>
        <span>About us</span>
      </button>
    </li>
  </menu>
</div>
```

FAB Menu Bottom-Left Button:

```html
<div>
  <button class="extra circle">
    <i>south_east</i>
  </button>
  <menu class="bottom transparent no-wrap">
    <li>
      <button class="fill">
        <i>search</i>
        <span>Search</span>
      </button>
    </li>
    <li>
      <button class="fill">
        <i>home</i>
        <span>Home</span>
      </button>
    </li>
    <li>
      <button class="fill">
        <i>more_vert</i>
        <span>About us</span>
      </button>
    </li>
  </menu>
</div>
```

FAB Menu Bottom-Right Button:

```html
<div>
  <button class="extra circle">
    <i>south_west</i>
  </button>
  <menu class="bottom transparent no-wrap left right-align">
    <li>
      <button class="fill">
        <i>search</i>
        <span>Search</span>
      </button>
    </li>
    <li>
      <button class="fill">
        <i>home</i>
        <span>Home</span>
      </button>
    </li>
    <li>
      <button class="fill">
        <i>more_vert</i>
        <span>About us</span>
      </button>
    </li>
  </menu>
</div>
```

### Icon Buttons

Sizes: small, medium, large, extra

**Default CSS elements**
- size: medium

Rule: The default CSS elements do not need to be added to the 'class'

#### Examples

Icon Square Button:

```html
<button class="transparent square extra">
  <i>search</i>
</button>
```

Icon Circle Button:

```html
<button class="transparent circle extra">
  <i>search</i>
</button>
```

Icon Left-Top Rounded Button:

```html
<button class="transparent circle left-round top-round extra">
  <i>search</i>
</button>
```

Icon Left-Bottom Rounded Button:

```html
<button class="transparent circle left-round bottom-round extra">
  <i>search</i>
</button>
```

Icon Right-Top Rounded Button:

```html
<button class="transparent circle right-round top-round extra">
  <i>search</i>
</button>
```

Icon Right-Bottom Rounded Button:

```html
<button class="transparent circle right-round bottom-round extra">
  <i>search</i>
</button>
```

Icon Left Rounded Button:

```html
<button class="transparent circle left-round extra">
  <i>search</i>
</button>
```

Icon Right Rounded Button:

```html
<button class="transparent circle right-round extra">
  <i>search</i>
</button>
```

Icon Square Image Button:

```html
<button class="transparent square extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Icon Circle Image Button:

```html
<button class="transparent circle extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Icon Left-Top Image Rounded Button:

```html
<button class="transparent circle left-round top-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Icon Left-Bottom Image Rounded Button:

```html
<button class="transparent circle left-round bottom-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Icon Right-Top Image Rounded Button:

```html
<button class="transparent circle right-round top-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Icon Right-Bottom Image Rounded Button:

```html
<button class="transparent circle right-round bottom-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Icon Image Left Rounded Button:

```html
<button class="transparent circle left-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```

Icon Image Right Rounded Button:

```html
<button class="transparent circle right-round extra">
  <img class="responsive" src="/favicon.png">
</button>
```


### Button Groups

Style: default, primary, secondary, tertiary
Sizes: small, medium, large, extra

**Default CSS elements**
- style: default
- size: medium

Rule: The default CSS elements do not need to be added to the 'class'

#### Standard

##### Examples

```html
<nav class="group">
  <button class="left-round">Button</button>
  <button class="no-round">Button</button>
  <button class="no-round active">Button</button>
  <button class="right-round">Button</button>
</nav>
```

```html
<nav class="group">
  <button class="left-round">
    <i>mic</i>
  </button>
  <button class="no-round">
    <i>videocam</i>
  </button>
  <button class="no-round active">
    <i>mood</i>
  </button>
  <button class="right-round">
    <i>front_hand</i>
  </button>
</nav>
```

```html
<nav class="group">
  <button class="left-round">
    <i>mic</i>
    <span>Button</span>
  </button>
  <button class="no-round">
    <i>videocam</i>
    <span>Button</span>
  </button>
  <button class="no-round active">
    <i>mood</i>
    <span>Button</span>
  </button>
  <button class="right-round">
    <i>front_hand</i>
    <span>Button</span>
  </button>
</nav>
```


#### Connected

##### Examples

```html
<nav class="group connected">
  <button class="left-round">Button</button>
  <button class="no-round">Button</button>
  <button class="no-round active">Button</button>
  <button class="right-round">Button</button>
</nav>
```

```html
<nav class="group connected">
  <button class="left-round">
    <i>mic</i>
  </button>
  <button class="no-round">
    <i>videocam</i>
  </button>
  <button class="no-round active">
    <i>mood</i>
  </button>
  <button class="right-round">
    <i>front_hand</i>
  </button>
</nav>
```

```html
<nav class="group connected">
  <button class="left-round">
    <i>mic</i>
    <span>Button</span>
  </button>
  <button class="no-round">
    <i>videocam</i>
    <span>Button</span>
  </button>
  <button class="no-round active">
    <i>mood</i>
    <span>Button</span>
  </button>
  <button class="right-round">
    <i>front_hand</i>
    <span>Button</span>
  </button>
</nav>
```


#### Split Buttons

Sizes: small, medium, large, extra

**Default CSS elements**
- size: medium

Rule: The default CSS elements do not need to be added to the 'class'

##### Examples

```html
<nav class="group split">
  <button class="left-round">
    <i>add_circle</i>
    <span>Button</span>
  </button>
  <button class="right-round square">
    <i>keyboard_arrow_down</i>
  </button>
</nav>
```

```html
<nav class="group split secondary">
  <button class="left-round">
    <i>add_circle</i>
    <span>Button</span>
  </button>
  <button class="right-round square">
    <i>keyboard_arrow_down</i>
  </button>
</nav>
```

```html
<nav class="group split tertiary">
  <button class="left-round">
    <i>add_circle</i>
    <span>Button</span>
  </button>
  <button class="right-round square">
    <i>keyboard_arrow_down</i>
  </button>
</nav>
```

---

## Cards

Media file: images, videos, svgs
Styles: default, fill, primary, secondary, tertiary

**Default CSS elements**
- style: default

Rule: The default CSS elements do not need to be added to the 'class'

### Examples for 'default' Style

Square Card:

```html
<article>
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

Square Rounded Card:

```html
<article class="round">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

Square Border Card:

```html
<article class="border">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

Square Rounded Border Card:

```html
<article class="border round">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

#### Examples of cards with multiple internal elements

Square Card Example with other elements:

```html
<article>
  <div class="row">
    <img class="circle large" src="/beer-and-woman.svg">
    <div class="max">
      <h5>Title</h5>
      <div>Some text here</div>
    </div>
  </div>
  <nav>
    <button>Button</button>
  </nav>
</article>
```

Square Rounded Card Example with other elements:

```html
<article class="round">
  <div class="row">
    <img class="circle large" src="/beer-and-woman.svg">
    <div class="max">
      <h5>Title</h5>
      <div>Some text here</div>
    </div>
  </div>
  <nav>
    <button>Button</button>
  </nav>
</article>
```

Square Border Card Example with other elements:

```html
<article class="border">
  <div class="row">
    <img class="circle large" src="/beer-and-woman.svg">
    <div class="max">
      <h5>Title</h5>
      <div>Some text here</div>
    </div>
  </div>
  <nav>
    <button>Button</button>
  </nav>
</article>
```

Square Rounded Border Card Example with other elements:

```html
<article class="border round">
  <div class="row">
    <img class="circle large" src="/beer-and-woman.svg">
    <div class="max">
      <h5>Title</h5>
      <div>Some text here</div>
    </div>
  </div>
  <nav>
    <button>Button</button>
  </nav>
</article>
```

#### Examples of cards with multiple internal elements and full-bleed header image

Square Card Example with other elements and full-bleed header image:

```html
<article class="no-padding">
  <img class="responsive small" src="/beer-and-woman.svg">
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button>Button</button>
    </nav>
  </div>
</article>
```

Square Rounded Card Example with other elements and full-bleed header image:

```html
<article class="no-padding round">
  <img class="responsive small top-round" src="/beer-and-woman.svg">
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button>Button</button>
    </nav>
  </div>
</article>
```

Square Border Card Example with other elements and full-bleed header image:

```html
<article class="no-padding border">
  <img class="responsive small" src="/beer-and-woman.svg">
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button>Button</button>
    </nav>
  </div>
</article>
```

Square Rounded Border Card Example with other elements and full-bleed header image:

```html
<article class="no-padding border round">
  <img class="responsive small top-round" src="/beer-and-woman.svg">
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button>Button</button>
    </nav>
  </div>
</article>
```

#### Examples of cards with multiple internal elements and image overlay

Square Card Example with other elements and image overlay:

```html
<article class="no-padding">
  <img class="responsive medium" src="/beer-and-woman.svg">
  <div class="row absolute bottom left right padding bottom-shadow white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

Square Rounded Card Example with other elements and image overlay:

```html
<article class="no-padding round">
  <img class="responsive medium" src="/beer-and-woman.svg">
  <div class="row absolute bottom left right padding bottom-shadow bottom-round white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

Square Border Card Example with other elements and image overlay:

```html
<article class="no-padding border">
  <img class="responsive medium" src="/beer-and-woman.svg">
  <div class="row absolute bottom left right padding bottom-shadow white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

Square Rounded Border Card Example with other elements and image overlay:

```html
<article class="no-padding border round">
  <img class="responsive medium" src="/beer-and-woman.svg">
  <div class="row absolute bottom left right padding bottom-shadow bottom-round white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

#### Examples of cards with multiple internal elements and side media

Square Card Example with other elements and side media:

```html
<article class="no-padding">
  <div class="grid no-space">
    <div class="s6">
      <img class="responsive" src="/beer-and-woman.svg">
    </div>
    <div class="s6">
      <div class="padding">
        <h5>Title</h5>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        <nav>
          <button class="border round">Button</button>
        </nav>
      </div>
    </div>
  </div>
</article>
```

Square Card Example with other elements and side media:
Aditional css

```html
<article class="no-padding">
  <div class="grid no-space">
    <div class="s6">
      <img class="responsive" src="/beer-and-woman.svg">
      <div class="absolute top left right padding top-shadow white-text">
        <h5>Title</h5>
        <p>Some text here</p>
      </div>
    </div>
    <div class="s6">
      <div class="padding">
        <h5>Title</h5>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        <nav>
          <button class="border round">Button</button>
        </nav>
      </div>
    </div>
  </div>
</article>
```

### Examples for 'primary', 'secondary' or 'tertiary' Style

Warning: If you use the 'fill' style, do not add the '-container' suffix or anything else. Only use 'fill' within the 'class' element.

Square Card:

```html
<article class="primary-container">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

Square Rounded Card:

```html
<article class="round primary-container">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

Square Border Card:

```html
<article class="border primary-container">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

Square Rounded Border Card:

```html
<article class="border round primary-container">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

#### Examples of cards with multiple internal elements

Square Card Example with other elements:

```html
<article class="primary-container">
  <div class="row">
    <img class="circle large" src="/beer-and-woman.svg">
    <div class="max">
      <h5>Title</h5>
      <div>Some text here</div>
    </div>
  </div>
  <nav>
    <button class="primary">Button</button>
  </nav>
</article>
```

Square Rounded Card Example with other elements:

```html
<article class="round primary-container">
  <div class="row">
    <img class="circle large" src="/beer-and-woman.svg">
    <div class="max">
      <h5>Title</h5>
      <div>Some text here</div>
    </div>
  </div>
  <nav>
    <button class="primary">Button</button>
  </nav>
</article>
```

Square Border Card Example with other elements:

```html
<article class="border primary-container">
  <div class="row">
    <img class="circle large" src="/beer-and-woman.svg">
    <div class="max">
      <h5>Title</h5>
      <div>Some text here</div>
    </div>
  </div>
  <nav>
    <button class="primary">Button</button>
  </nav>
</article>
```

Square Rounded Border Card Example with other elements:

```html
<article class="border round primary-container">
  <div class="row">
    <img class="circle large" src="/beer-and-woman.svg">
    <div class="max">
      <h5>Title</h5>
      <div>Some text here</div>
    </div>
  </div>
  <nav>
    <button class="primary">Button</button>
  </nav>
</article>
```

#### Examples of cards with multiple internal elements and full-bleed header image

Square Card Example with other elements and full-bleed header image:

```html
<article class="no-padding primary-container">
  <img class="responsive small" src="/beer-and-woman.svg">
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button class="primary">Button</button>
    </nav>
  </div>
</article>
```

Square Rounded Card Example with other elements and full-bleed header image:

```html
<article class="no-padding round primary-container">
  <img class="responsive small top-round" src="/beer-and-woman.svg">
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button class="primary">Button</button>
    </nav>
  </div>
</article>
```

Square Border Card Example with other elements and full-bleed header image:

```html
<article class="no-padding border primary-container">
  <img class="responsive small" src="/beer-and-woman.svg">
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button class="primary">Button</button>
    </nav>
  </div>
</article>
```

Square Rounded Border Card Example with other elements and full-bleed header image:

```html
<article class="no-padding border round primary-container">
  <img class="responsive small top-round" src="/beer-and-woman.svg">
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button class="primary">Button</button>
    </nav>
  </div>
</article>
```

#### Examples of cards with multiple internal elements and image overlay

Square Card Example with other elements and image overlay:

```html
<article class="no-padding primary-container">
  <img class="responsive medium" src="/beer-and-woman.svg">
  <div class="row absolute bottom left right padding bottom-shadow white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

Square Rounded Card Example with other elements and image overlay:

```html
<article class="no-padding round primary-container">
  <img class="responsive medium" src="/beer-and-woman.svg">
  <div class="row absolute bottom left right padding bottom-shadow bottom-round white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

Square Border Card Example with other elements and image overlay:

```html
<article class="no-padding border primary-container">
  <img class="responsive medium" src="/beer-and-woman.svg">
  <div class="row absolute bottom left right padding bottom-shadow white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

Square Rounded Border Card Example with other elements and image overlay:

```html
<article class="no-padding border round primary-container">
  <img class="responsive medium" src="/beer-and-woman.svg">
  <div class="row absolute bottom left right padding bottom-shadow bottom-round white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

#### Examples of cards with multiple internal elements and side media

Square Card Example with other elements and side media:

```html
<article class="no-padding primary-container">
  <div class="grid no-space">
    <div class="s6">
      <img class="responsive" src="/beer-and-woman.svg">
    </div>
    <div class="s6">
      <div class="padding">
        <h5>Title</h5>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        <nav>
          <button class="border round">Button</button>
        </nav>
      </div>
    </div>
  </div>
</article>
```

Square Card Example with other elements and side media:
Aditional css

```html
<article class="no-padding primary-container">
  <div class="grid no-space">
    <div class="s6">
      <img class="responsive" src="/beer-and-woman.svg">
      <div class="absolute top left right padding top-shadow white-text">
        <h5>Title</h5>
        <p>Some text here</p>
      </div>
    </div>
    <div class="s6">
      <div class="padding">
        <h5>Title</h5>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        <nav>
          <button class="border round">Button</button>
        </nav>
      </div>
    </div>
  </div>
</article>
```

---

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

---

## Chips (falta detallar)

Sizes: small, medium, large
Elevate: no-elevate, small-elevate, medium-elevate, large-elevate
Orientation: horizontal, vertical

**Default CSS elements**
- size: small
- elevate: no-elevate
- orientation: horizontal

Rule: The default CSS elements do not need to be added to the 'class'

### Chips Only Border:

### Shape Square Examples:

```html
<button class="chip">Suggestion</button>
```

```html
<button class="chip">
  <span>Input</span>
  <i>close</i>
</button>
```

```html
<button class="chip">
  <i>done</i>
  <span>Filter</span>
</button>
```

```html
<button class="chip">
  <i class="primary-text">today</i>
  <span>Assist</span>
</button>
```

```html
<button class="chip">
  <img src="favicon.png">
  <span>Image</span>
</button>
```

```html
<button class="chip">
  <img class="responsive" src="favicon.png">
  <span>Responsive</span>
</button>
```


### Shape Square Rounded Examples:

```html
<button class="chip round">Suggestion</button>
```

```html
<button class="chip round">
  <span>Input</span>
  <i>close</i>
</button>
```

```html

<button class="chip round">
  <i>done</i>
  <span>Filter</span>
</button>
```

```html
<button class="chip round">
  <i class="primary-text">today</i>
  <span>Assist</span>
</button>
```

```html
<button class="chip round">
  <img src="favicon.png">
  <span>Image</span>
</button>
```

```html
<button class="chip round">
  <img class="responsive" src="favicon.png">
  <span>Responsive</span>
</button>
```

### Chips Fill:

### Shape Square Examples:

```html
<button class="chip fill">Suggestion</button>
```

```html
<button class="chip fill">
  <span>Input</span>
  <i>close</i>
</button>
```

```html
<button class="chip fill">
  <i>done</i>
  <span>Filter</span>
</button>
```

```html
<button class="chip fill">
  <i class="primary-text">today</i>
  <span>Assist</span>
</button>
```

```html
<button class="chip fill">
  <img src="favicon.png">
  <span>Image</span>
</button>
```

```html
<button class="chip fill">
  <img class="responsive" src="favicon.png">
  <span>Responsive</span>
</button>
```


### Shape Square Rounded Examples:

```html
<button class="chip fill round">Suggestion</button>
```

```html
<button class="chip fill round">
  <span>Input</span>
  <i>close</i>
</button>
```

```html
<button class="chip fill round">
  <i>done</i>
  <span>Filter</span>
</button>
```

```html
<button class="chip fill round">
  <i class="primary-text">today</i>
  <span>Assist</span>
</button>
```

```html
<button class="chip fill round">
  <img src="favicon.png">
  <span>Image</span>
</button>
```

```html
<button class="chip fill round">
  <img class="responsive" src="favicon.png">
  <span>Responsive</span>
</button>
```

---

## Colors

Rule: Use only these colors for all elements of the project; do not alter, customize, edit, or do anything that involves changing these colors.

### Light Mode

```css
--primary:#4355b9;
--on-primary:#ffffff;
--primary-container:#dee0ff;
--on-primary-container:#00105c;
--secondary:#5b5d72;
--on-secondary:#ffffff;
--secondary-container:#e0e1f9;
--on-secondary-container:#181a2c;
--tertiary:#77536d;
--on-tertiary:#ffffff;
--tertiary-container:#ffd7f1;
--on-tertiary-container:#2d1228;
--error:#ba1a1a;
--on-error:#ffffff;
--error-container:#ffdad6;
--on-error-container:#410002;
--background:#fefbff;
--on-background:#1b1b1f;
--surface:#fbf8fd;
--on-surface:#1b1b1f;
--surface-variant:#e3e1ec;
--on-surface-variant:#46464f;
--outline:#767680;
--outline-variant:#c7c5d0;
--shadow:#000000;
--scrim:#000000;
--inverse-surface:#303034;
--inverse-on-surface:#f3f0f4;
--inverse-primary:#bac3ff;
--surface-dim:#dcd9de;
--surface-bright:#fbf8fd;
--surface-container-lowest:#ffffff;
--surface-container-low:#f6f2f7;
--surface-container:#f0edf1;
--surface-container-high:#eae7ec;
--surface-container-highest:#e4e1e6;
```

### Dark Mode

```css
--primary:#bac3ff;
--on-primary:#08218a;
--primary-container:#293ca0;
--on-primary-container:#dee0ff;
--secondary:#c3c5dd;
--on-secondary:#2d2f42;
--secondary-container:#434659;
--on-secondary-container:#e0e1f9;
--tertiary:#e6bad7;
--on-tertiary:#44263d;
--tertiary-container:#5d3c55;
--on-tertiary-container:#ffd7f1;
--error:#ffb4ab;
--on-error:#690005;
--error-container:#93000a;
--on-error-container:#ffb4ab;
--background:#1b1b1f;
--on-background:#e4e1e6;
--surface:#131316;
--on-surface:#e4e1e6;
--surface-variant:#46464f;
--on-surface-variant:#c7c5d0;
--outline:#90909a;
--outline-variant:#46464f;
--shadow:#000000;
--scrim:#000000;
--inverse-surface:#e4e1e6;
--inverse-on-surface:#303034;
--inverse-primary:#4355b9;
--surface-dim:#131316;
--surface-bright:#39393c;
--surface-container-lowest:#0e0e11;
--surface-container-low:#1b1b1f;
--surface-container:#1f1f23;
--surface-container-high:#2a2a2d;
--surface-container-highest:#353438;
```

---

## Container

Rule: This property defines whether or not a container will have built-in responsiveness.

### Main Content

Default:

```html
<main></main>
```

Responsive:

```html
<main class="responsive"></main>
```

### Side Content

Rule: This property allows us to place side content, either on the left or right side of an HTML container.

```html
<div>
  <aside class="right small-width small-height padding">
    <img class="responsive" src="/beer-and-woman.jpg">
  </aside>
  <h5>Title</h5>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
</div>
```

```html
<div>
  <aside class="left small-width small-height padding">
    <img class="responsive" src="/beer-and-woman.jpg">
  </aside>
  <h5>Title</h5>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
</div>
```

---

## Dialogs (falta detallar)

### Examples

```html
<dialog>
  <h5>Default</h5>
  <div>Some text here</div>
  <nav class="right-align no-space">
    <button class="transparent link">Cancel</button>
    <button class="transparent link">Confirm</button>
  </nav>
</dialog>
```

```html
<dialog class="modal">
  <h5>Modal</h5>
  <div>Some text here</div>
  <nav class="right-align no-space">
    <button class="transparent link">Cancel</button>
    <button class="transparent link">Confirm</button>
  </nav>
</dialog>
```

```html
<div class="overlay blur"></div>
<dialog>
  <h5>Custom overlay</h5>
  <div>Some text here</div>
  <nav class="right-align no-space">
    <button class="transparent link">Cancel</button>
    <button class="transparent link">Confirm</button>
  </nav>
</dialog>
```

```html
<dialog class="left">
  <h5>Left</h5>
  <div>Some text here</div>
  <nav class="right-align">
    <button class="border">Cancel</button>
    <button>Confirm</button>
  </nav>
</dialog>
```

```html
<dialog class="right">
  <h5>Right</h5>
  <div>Some text here</div>
  <nav class="right-align">
    <button class="border">Cancel</button>
    <button>Confirm</button>
  </nav>
</dialog>
```

```html
<dialog class="top">
  <h5>Top</h5>
  <div>Some text here</div>
  <nav class="right-align">
    <button class="border">Cancel</button>
    <button>Confirm</button>
  </nav>
</dialog>
```

```html
<dialog class="bottom">
  <h5>Bottom</h5>
  <div>Some text here</div>
  <nav class="right-align">
    <button class="border">Cancel</button>
    <button>Confirm</button>
  </nav>
</dialog>
```

```html
<dialog class="max">
  <h5>Fullscreen</h5>
  <div>Some text here</div>
  <nav class="right-align">
    <button class="border">Cancel</button>
    <button>Confirm</button>
  </nav>
</dialog>
```

```html
<dialog class="left">
  <header>
    <nav>
      <img class="circle large" src="/favicon.png">
      <h6 class="max">Title</h6>
      <button class="transparent circle large">
        <i>close</i>
      </button>
    </nav>
  </header>
  <div class="space"></div>
  <ul class="list">
    <li class="wave round">
      <i>inbox</i>
      <span class="max">Inbox</span>
      <b>24</b>
    </li>
    <li class="wave round">
      <i>send</i>
      <span>Outbox</span>
    </li>
    <li class="wave round">
      <i>favorite</i>
      <span>favorities</span>
    </li>
    <li class="wave round">
      <i>delete</i>
      <span>Trash</span>
    </li>
    <li class="wave round">
      <i>fiber_manual_record</i>
      <span>Label</span>
    </li>
    <li class="wave round">
      <i>change_history</i>
      <span>Label</span>
    </li>
    <li class="wave round">
      <i>stop</i>
      <span>Label</span>
    </li>
  </ul>
</dialog>
```

---

## Directions (falta completar)

Orientation: horizontal, vertical

**Default CSS elements**
- orientation: horizontal

Rule: The default CSS elements do not need to be added to the 'class'

### Examples

```html
<button>
  <i>home</i>
  <span>Button</span>
</button>
```

```html
<button class="chip">
  <i>home</i>
  <span>Chip</span>
</button>
```

```html
<nav class="group connected">
  <button class="border left-round">
    <i>home</i>
    <span>Button</span>
  </button>
  <button class="border no-round">
    <i>home</i>
    <span>Button</span>
  </button>
  <button class="border right-round">
    <i>home</i>
    <span>Button</span>
  </button>
</nav>
```

```html
<div class="tabs">
  <a class="active">
    <i>home</i>
    <span>Tab 1</span>
  </a>
  <a>
    <i>home</i>
    <span>Tab 2</span>
  </a>
  <a>
    <i>home</i>
    <span>Tab 3</span>
  </a>
</div>
```

---

## Dividers

Size: default, small, medium, large

**Default CSS elements**
- size: default

Rule: The default CSS elements do not need to be added to the 'class'

### Examples

Default Divider:

```html
<div>
  <div>Some text here</div>
  <hr>
  <div>Some text here</div>
  <hr>
  <div>Some text here</div>
</div>
```

Small/Medium/Large Divider:

```html
<div>
  <div>Some text here</div>
  <hr class="small">
  <div>Some text here</div>
  <hr class="small">
  <div>Some text here</div>
</div>
```

---

## Expansions

Default Expansion:

```html
<details>
  <summary>Default</summary>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
</details>
```

Multiple Levels Expansion:

```html
<details>
  <summary>Multiple levels</summary>
  <details>
    <summary>First</summary>
    <details>
      <summary>Second</summary>
      <details>
        <summary>Third</summary>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
      </details>
    </details>
  </details>
</details>
```

Custom Expansion:

```html
<details>
  <summary>
    <button>
      <span>Button</span>
      <i>expand_more</i>
    </button>
  </summary>
  <article>
    <h6>Title </h6>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
  </article>
  <article>
    <h6>Title</h6>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
  </article>
</details>
```

---

REVISAR ESTE APARTADO, HAY PUNTOS POR COMPLETAR

---

## Inputs (falta completar)

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

---

## Layout (falta detallar)

Layouts are containers that you can place in any position. You can control the positioning of elements using absolute/fixed classes or control the alignment of children using alignment helpers.

### Helpers

#### **Positions** (Applied to the element itself)

Horizontal axis:

`left`, `center`, `right`

Vertical axis:

`top`, `middle`, `bottom`

#### **Alignments** (Applied to the parent container)

Horizontal axis:

`left-align`, `center-align`, `right-align`

Vertical axis:

`top-align`, `middle-align`, `bottom-align`

### Position examples

**Left and Middle**
```html
<article class="small-round padding border medium no-padding">
  <div class="padding primary absolute middle left">
    <h5>Position</h5>
    <div>Left Middle</div>
  </div>
</article>

```

**Center and Middle**

```html
<article class="small-round padding border medium no-padding">
  <div class="padding primary absolute middle center">
    <h5>Position</h5>
    <div>Center Middle</div>
  </div>
</article>

```

**Right and Top**

```html
<article class="small-round padding border medium no-padding">
  <div class="padding primary absolute top right">
    <h5>Position</h5>
    <div>Top Right</div>
  </div>
</article>

```

### Alignments Examples

**Center and Middle Align**

```html
<article class="border medium no-padding middle-align center-align">
  <div class="padding">
    <h5>Alignment</h5>
    <div>Centered content</div>
  </div>
</article>

```

**Left and Top Align**

```html
<article class="border medium no-padding left-align top-align">
  <div class="padding">
    <h5>Alignment</h5>
    <div>Top Left content</div>
  </div>
</article>

```

**Right and Bottom Align**

```html
<article class="border medium no-padding right-align bottom-align">
  <div class="padding">
    <h5>Alignment</h5>
    <div>Bottom Right content</div>
  </div>
</article>
```

### Headers and Footers

Fixed header example:

```html
<article class="small scroll">
  <header class="fixed">
    <h5 class="no-margin">Fixed header</h5>
  </header>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupILayoutt non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupILayoutt non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
</article>
```

Fixed footer example:

```html
<article class="small scroll">
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupILayoutt non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupILayoutt non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  <footer class="fixed">
    <h5 class="no-margin">Fixed footer</h5>
  </footer>
</article>
```

### Empty States

#### Examples

```html
<article class="medium middle-align center-align">
  <div>
    <i class="extra">mail</i>
    <h5>You have no new messages</h5>
    <p>Click the button to start a conversation</p>
    <div class="space"></div>
    <nav class="center-align">
      <button>Send a message</button>
    </nav>
  </div>
</article>
```

```html
<article class="medium middle-align center-align">
  <div>
    <i class="extra">mail</i>
    <h5>You've successfully signed up</h5>
    <p>Click the button to invite your friends</p>
    <div class="space"></div>
    <nav class="center-align">
      <button class="border round">Skip</button>
      <button>Invite your friends</button>
    </nav>
  </div>
</article>
```

```html
<article class="medium middle-align center-align">
  <div>
    <i class="extra">person</i>
    <h5>You are not following anyone</h5>
    <p>Start to meet new friends</p>
    <div class="space"></div>
    <nav class="no-space">
      <div class="max field border left-round">
        <input>
      </div>
      <button class="large right-round">Search</button>
    </nav>
  </div>
</article>
```

### Blurred Elements

App bar example:

```html
<header class="blur">
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <h5 class="max">App bar</h5>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
</header>
```

Card example:

```html
<article class="blur">
  <h5>Card</h5>
  <p>Some text here</p>
  <nav class="right-align">
    <button>Button</button>
  </nav>
</article>
```

Button example:

```html
<button class="blur">Button</button>
```

Chip example:

```html
<button class="chip blur">Chip</button>
```


### Shadowed Elements

App bar example:

```html
<header class="white-text left-shadow">
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <h5 class="max">App bar</h5>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
</header>
```

Card example:

```html
<article class="white-text left-shadow">
  <h5>Card</h5>
  <p>Some text here</p>
  <nav class="right-align">
    <button>Button</button>
  </nav>
</article>
```

Button example:

```html
<button class="white-text left-shadow">Button</button>
```

Chip example:

```html
<button class="chip white-text left-shadow">Chip</button>
```

---

## Lists (falta detallar)

Default example:

```html
<ul class="list border">
  <li>Item</li>
  <li>Item</li>
  <li>Item</li>
  <li>Item</li>
</ul>
```

Link example:

```html
<ul class="list border">
  <li>
    <a>Item</a>
  </li>
  <li>
    <a>Item</a>
  </li>
  <li>
    <a>Item</a>
  </li>
  <li>
    <a>Item</a>
  </li>
</ul>
```

Nested example:

```html
<ul class="list border">
  <li>Item</li>
  <li>Item</li>
  <li>
    <ul class="list border">
      <li>Item</li>
      <li>Item</li>
    </ul>
  </li>
</ul>
```

Expansion example:

```html
<ul class="list border">
  <li>Item</li>
  <li>Item</li>
  <li>
    <details>
      <summary>Header Item</summary>
      <ul class="list border">
        <li>Item</li>
        <li>Item</li>
      </ul>
    </details>
  </li>
</ul>
```

Headline and supporting text example:

```html
<ul class="list border">
  <li>
    <button class="circle">A</button>
    <div class="max">
      <h6 class="small">Headline</h6>
      <div>Supporting text</div>
    </div>
    <label>+15 min</label>
  </li>
  <li>
    <button class="circle">A</button>
    <div class="max">
      <h6 class="small">Headline</h6>
      <div>Supporting text</div>
    </div>
    <label>+15 min</label>
  </li>
</ul>
```

Icons example:

```html
<ul class="list border">
  <li>
    <i>home</i>
    <div class="max">
      <h6 class="small">Headline</h6>
      <div>Supporting text</div>
    </div>
    <label>+15 min</label>
  </li>
  <li>
    <i>home</i>
    <div class="max">
      <h6 class="small">Headline</h6>
      <div>Supporting text</div>
    </div>
    <label>+15 min</label>
  </li>
</ul>
```

Leading media or avatar example:

```html
<ul class="list border">
  <li>
    <img class="round" src="/beer-and-woman.svg">
    <div class="max">
      <h6 class="small">Headline</h6>
      <div>Supporting text</div>
    </div>
    <label>+15 min</label>
  </li>
  <li>
    <img class="round" src="/beer-and-woman.svg">
    <div class="max">
      <h6 class="small">Headline</h6>
      <div>Supporting text</div>
    </div>
    <label>+15 min</label>
  </li>
</ul>
```

Link and buttons example:

```html
<ul class="list border">
  <li>
    <div class="max">
      <h6 class="small">Headline</h6>
      <div>Supporting text</div>
    </div>
    <a>Link</a>
    <button>Button</button>
  </li>
  <li>
    <div class="max">
      <h6 class="small">Headline</h6>
      <div>Supporting text</div>
    </div>
    <a>Link</a>
    <button>Button</button>
  </li>
</ul>
```

---

## Menus (falta detallar)

Examples:

```html
<div>
  <button>
    <span>Default</span>
    <i>arrow_drop_down</i>
  </button>
  <menu>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </menu>
</div>
```

```html
<div>
  <button>
    <span>Border</span>
    <i>arrow_drop_down</i>
  </button>
  <menu class="border">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </menu>
</div>
```

```html
<div>
  <button>
    <span>No-wrap</span>
    <i>arrow_drop_down</i>
  </button>
  <menu class="no-wrap">
    <li>Lorem ipsum dolor sit amet</li>
    <li>Lorem ipsum dolor sit amet</li>
    <li>Lorem ipsum dolor sit amet</li>
  </menu>
</div>
```

```html
<div>
  <button class="circle">
    <i>arrow_back</i>
  </button>
  <menu class="left no-wrap">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </menu>
</div>
```

```html
<div>
  <button class="circle">
    <i>arrow_forward</i>
  </button>
  <menu class="right no-wrap">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </menu>
</div>
```

```html
<div>
  <button>
    <span>Top</span>
    <i>arrow_drop_up</i>
  </button>
  <menu class="top">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </menu>
</div>
```

```html
<div>
  <button>
    <span>Links</span>
    <i>arrow_drop_down</i>
  </button>
  <menu>
    <li>
      <a>Item 1</a>
    </li>
    <li>
      <a>Item 2</a>
    </li>
    <li>
      <a>Item 3</a>
    </li>
  </menu>
</div>
```

```html
<div>
  <button>
    <span>Images and icons</span>
  </button>
  <menu class="no-wrap">
    <li>Title</li>
    <li>
      <div>Title</div>
      <label>Some text here</label>
    </li>
    <li>
      <i>home</i>
      <span>Title</span>
    </li>
    <li>
      <i>home</i>
      <div class="max">
        <div>Title</div>
        <label>Some text here</label>
      </div>
    </li>
    <li>
      <img class="circle tiny" src="/beer-and-woman.svg">
      <span>Title</span>
    </li>
    <li>
      <img class="circle tiny" src="/beer-and-woman.svg">
      <div class="max">
        <div>Title</div>
        <label>Some text here</label>
      </div>
    </li>
  </menu>
</div>
```

```html
<div>
  <button>
    <span>Video</span>
  </button>
  <menu class="no-wrap no-padding">
    <li class="no-padding">
      <video class="small-width">
        <source src="/dance.mp4" type="video/mp4">
      </video>
    </li>
  </menu>
</div>
```

```html
<div>
  <button>
    <span>Docked</span>
  </button>
  <menu class="min">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </menu>
</div>
```

```html
<div>
  <button>
    <span>Fullscreen</span>
  </button>
  <menu class="max">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </menu>
</div>
```

```html
<div>
  <button>
    <span>Multi level</span>
    <i>arrow_drop_down</i>
  </button>
  <menu>
    <li>Item</li>
    <li>Item</li>
    <li>More items
      <menu>
        <li>Item</li>
        <li>Item</li>
        <li>More items
          <menu>
            <li>Item</li>
            <li>Item</li>
            <li>item</li>
          </menu>
        </li>
      </menu>
    </li>
  </menu>
</div>
```

---

## Navigations (falta detallar)

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

---

## Pages (falta detallar)

Examples:

```html
<div class="page active">
  <h5>Default</h5>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum elementum ante sit amet risus accumsan, id luctus massa gravida. Morbi fermentum vehicula leo sed rhoncus. Donec sapien lacus, rhoncus ut turpis at, elementum laoreet est. Sed ut diam eget tellus dictum varius eget vel mi. Morbi mattis posuere turpis viverra pulvinar. Sed purus nibh, tempus et sem vel, egestas consectetur eros. Sed tempus neque est. Etiam vitae eros vitae risus suscipit accumsan sed sit amet ex. Quisque eget sodales augue. Nullam eget viverra nunc. In interdum aliquam egestas. Suspendisse ultricies ante euismod, aliquam nisl eu, sagittis libero. Quisque vel condimentum ligula.</p>
</div>
```

```html
<div class="page left">
  <h5>Left</h5>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum elementum ante sit amet risus accumsan, id luctus massa gravida. Morbi fermentum vehicula leo sed rhoncus. Donec sapien lacus, rhoncus ut turpis at, elementum laoreet est. Sed ut diam eget tellus dictum varius eget vel mi. Morbi mattis posuere turpis viverra pulvinar. Sed purus nibh, tempus et sem vel, egestas consectetur eros. Sed tempus neque est. Etiam vitae eros vitae risus suscipit accumsan sed sit amet ex. Quisque eget sodales augue. Nullam eget viverra nunc. In interdum aliquam egestas. Suspendisse ultricies ante euismod, aliquam nisl eu, sagittis libero. Quisque vel condimentum ligula.</p>
</div>
```

```html
<div class="page top">
  <h5>Top</h5>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum elementum ante sit amet risus accumsan, id luctus massa gravida. Morbi fermentum vehicula leo sed rhoncus. Donec sapien lacus, rhoncus ut turpis at, elementum laoreet est. Sed ut diam eget tellus dictum varius eget vel mi. Morbi mattis posuere turpis viverra pulvinar. Sed purus nibh, tempus et sem vel, egestas consectetur eros. Sed tempus neque est. Etiam vitae eros vitae risus suscipit accumsan sed sit amet ex. Quisque eget sodales augue. Nullam eget viverra nunc. In interdum aliquam egestas. Suspendisse ultricies ante euismod, aliquam nisl eu, sagittis libero. Quisque vel condimentum ligula.</p>
</div>
```

```html
<div class="page bottom">
  <h5>Bottom</h5>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum elementum ante sit amet risus accumsan, id luctus massa gravida. Morbi fermentum vehicula leo sed rhoncus. Donec sapien lacus, rhoncus ut turpis at, elementum laoreet est. Sed ut diam eget tellus dictum varius eget vel mi. Morbi mattis posuere turpis viverra pulvinar. Sed purus nibh, tempus et sem vel, egestas consectetur eros. Sed tempus neque est. Etiam vitae eros vitae risus suscipit accumsan sed sit amet ex. Quisque eget sodales augue. Nullam eget viverra nunc. In interdum aliquam egestas. Suspendisse ultricies ante euismod, aliquam nisl eu, sagittis libero. Quisque vel condimentum ligula.</p>
</div>
```

```html
<div class="page right">
  <h5>Right</h5>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum elementum ante sit amet risus accumsan, id luctus massa gravida. Morbi fermentum vehicula leo sed rhoncus. Donec sapien lacus, rhoncus ut turpis at, elementum laoreet est. Sed ut diam eget tellus dictum varius eget vel mi. Morbi mattis posuere turpis viverra pulvinar. Sed purus nibh, tempus et sem vel, egestas consectetur eros. Sed tempus neque est. Etiam vitae eros vitae risus suscipit accumsan sed sit amet ex. Quisque eget sodales augue. Nullam eget viverra nunc. In interdum aliquam egestas. Suspendisse ultricies ante euismod, aliquam nisl eu, sagittis libero. Quisque vel condimentum ligula.</p>
</div>
```

---

## Progress (falta detallar)

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

---

## Radios (falta detallar)

### Default Radio examples

```html
<label class="radio">
  <input type="radio" name="radio1_">
  <span></span>
</label>
```

```html
<label class="radio">
  <input type="radio" name="radio1_">
  <span>Enabled</span>
</label>
```

```html
<label class="radio">
  <input type="radio" name="radio2_" disabled>
  <span>Disabled</span>
</label>
```

```html
<label class="radio">
  <input type="radio" name="radio2_" checked disabled>
  <span>Disabled</span>
</label>
```

```html
<label class="radio small">
  <input type="radio" name="radio3_">
  <span></span>
</label>
```

```html
<label class="radio">
  <input type="radio" name="radio3_">
  <span></span>
</label>
```

```html
<label class="radio large">
  <input type="radio" name="radio3_">
  <span></span>
</label>
```

```html
<label class="radio extra">
  <input type="radio" name="radio3_">
  <span></span>
</label>
```

### Radio with icons examples

```html
<label class="radio icon">
  <input type="radio" name="radio3_">
  <span>
    <i>close</i>
    <i>done</i>
  </span>
</label>
```

```html
<label class="radio icon">
  <input type="radio" name="radio3_">
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

```html
<label class="radio icon">
  <input type="radio" name="radio3_">
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

### Radio in field elements examples

```html
<div class="field middle-align">
  <nav>
    <label class="radio">
      <input type="radio" name="radio4_">
      <span>Item 1</span>
    </label>
    <label class="radio">
      <input type="radio" name="radio4_">
      <span>Item 2</span>
    </label>
    <label class="radio">
      <input type="radio" name="radio4_">
      <span>Item 3</span>
    </label>
  </nav>
</div>
```

```html
<div class="field middle-align">
  <nav>
    <label class="radio">
      <input type="radio" name="radio5_">
      <span>Item 1</span>
    </label>
    <label class="radio">
      <input type="radio" name="radio5_">
      <span>Item 2</span>
    </label>
    <label class="radio">
      <input type="radio" name="radio5_">
      <span>Item 3</span>
    </label>
  </nav>
  <output>Helper text</output>
</div>
```

```html
<div class="field middle-align invalid">
  <nav>
    <label class="radio">
      <input type="radio" name="radio6_">
      <span>Item 1</span>
    </label>
    <label class="radio">
      <input type="radio" name="radio6_">
      <span>Item 2</span>
    </label>
    <label class="radio">
      <input type="radio" name="radio6_">
      <span>Item 3</span>
    </label>
  </nav>
  <output class="invalid">Error text</output>
</div>
```

---

## Responsive (falta detallar)

Example:

```html
<nav>
  <button class="s circle extra">
    <i>phone_android</i>
  </button>
  <button class="m l border circle extra">
    <i>phone_android</i>
  </button>
  <button class="m circle extra">
    <i>tablet_android</i>
  </button>
  <button class="s l border circle extra">
    <i>tablet_android</i>
  </button>
  <button class="l circle extra">
    <i>laptop_windows</i>
  </button>
  <button class="s m border circle extra">
    <i>laptop_windows</i>
  </button>
</nav>
```

---

## Scrolls

horizontal scroll

### Horizontal Scroll in Chips

```html
<nav class="scroll">
  <button class="chip">Suggestion</button>
  <button class="chip">Suggestion</button>
  <button class="chip fill">Selected</button>
  <button class="chip fill">Selected</button>
  <button class="chip">Suggestion</button>
  <button class="chip fill">Selected</button>
  <button class="chip">Suggestion</button>
  <button class="chip">Suggestion</button>
  <button class="chip">Suggestion</button>
  <button class="chip">Suggestion</button>
  <button class="chip">Suggestion</button>
  <button class="chip">Suggestion</button>
</nav>
```

### Horizontal Scroll in Images

```html
<div class="row scroll">
  <img class="small-width small-height" src="/favicon.png">
  <img class="small-width small-height" src="/favicon.png">
  <img class="small-width small-height" src="/favicon.png">
  <img class="small-width small-height" src="/favicon.png">
  <img class="small-width small-height" src="/favicon.png">
  <img class="small-width small-height" src="/favicon.png">
  <img class="small-width small-height" src="/favicon.png">
  <img class="small-width small-height" src="/favicon.png">
  <img class="small-width small-height" src="/favicon.png">
  <img class="small-width small-height" src="/favicon.png">
</div>
```

### Horizontal Scroll in Cards

```html
<div class="row scroll">
  <article class="small-width border">
    <h5>Title </h5>
    <p>Some text here</p>
    <div class="space"></div>
    <nav>
      <button>Button</button>
    </nav>
  </article>
  <article class="small-width border">
    <h5>Title </h5>
    <p>Some text here</p>
    <div class="space"></div>
    <nav>
      <button>Button</button>
    </nav>
  </article>
  <article class="small-width border">
    <h5>Title </h5>
    <p>Some text here</p>
    <div class="space"></div>
    <nav>
      <button>Button</button>
    </nav>
  </article>
  <article class="small-width border">
    <h5>Title </h5>
    <p>Some text here</p>
    <div class="space"></div>
    <nav>
      <button>Button</button>
    </nav>
  </article>
  <article class="small-width border">
    <h5>Title </h5>
    <p>Some text here</p>
    <div class="space"></div>
    <nav>
      <button>Button</button>
    </nav>
  </article>
  <article class="small-width border">
    <h5>Title </h5>
    <p>Some text here</p>
    <div class="space"></div>
    <nav>
      <button>Button</button>
    </nav>
  </article>
  <article class="small-width border">
    <h5>Title </h5>
    <p>Some text here</p>
    <div class="space"></div>
    <nav>
      <button>Button</button>
    </nav>
  </article>
  <article class="small-width border">
    <h5>Title </h5>
    <p>Some text here</p>
    <div class="space"></div>
    <nav>
      <button>Button</button>
    </nav>
  </article>
  <article class="small-width border">
    <h5>Title </h5>
    <p>Some text here</p>
    <div class="space"></div>
    <nav>
      <button>Button</button>
    </nav>
  </article>
  <article class="small-width border">
    <h5>Title </h5>
    <p>Some text here</p>
    <div class="space"></div>
    <nav>
      <button>Button</button>
    </nav>
  </article>
</div>
```

---

## Search (falta detallar)

### Docked

Model 1:

```html
<div class="field large prefix round fill active">
  <i class="front">search</i>
  <input>
  <menu class="min">
    <li>
      <div class="field large prefix">
        <i class="front">arrow_back</i>
        <input>
      </div>
    </li>
    <li>
      <i>history</i>
      <div>Item 1</div>
    </li>
    <li>
      <i>history</i>
      <div>Item 2</div>
    </li>
    <li>
      <i>history</i>
      <div>Item 3</div>
    </li>
  </menu>
</div>
```

Model 2:

```html
<div class="active">
  <button class="extra circle fill">
    <i>search</i>
  </button>
  <menu class="no-wrap left min">
    <li>
      <div class="field large prefix">
        <i class="front">arrow_back</i>
        <input>
      </div>
    </li>
    <li>
      <i>history</i>
      <div>Item 1</div>
    </li>
    <li>
      <i>history</i>
      <div>Item 2</div>
    </li>
    <li>
      <i>history</i>
      <div>Item 3</div>
    </li>
  </menu>
</div>
```

### Fullscreen

Model 1:

```html
<div class="field large prefix round fill active">
  <i class="front">search</i>
  <input>
  <menu class="max">
    <li>
      <div class="field large prefix">
        <i class="front">arrow_back</i>
        <input>
      </div>
    </li>
    <li>
      <i>history</i>
      <div>Item 1</div>
    </li>
    <li>
      <i>history</i>
      <div>Item 2</div>
    </li>
    <li>
      <i>history</i>
      <div>Item 3</div>
    </li>
  </menu>
</div>
```

Model 2:

```html
<div>
  <button class="extra circle fill">
    <i>search</i>
  </button>
  <menu class="max">
    <li>
      <div class="field large prefix">
        <i class="front">arrow_back</i>
        <input>
      </div>
    </li>
    <li>
      <i>history</i>
      <div>Item 1</div>
    </li>
    <li>
      <i>history</i>
      <div>Item 2</div>
    </li>
    <li>
      <i>history</i>
      <div>Item 3</div>
    </li>
  </menu>
</div>
```

---

## Selects (falta detallar)

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

---

## Shapes (falta detallar)

Shapes: 'loading-indicator', 'boom', 'burst', 'clamshell', 'diamond', 'flower', 'puffy', 'sided-cookie6', 'sided-cookie7', 'sided-cookie9', 'sided-cookie12', 'soft-boom', 'soft-burst', 'sunny', 'very-sunny'

type data: none, image, video, button

### Default Examples

```html
<div class="shape sided-cookie7 small">
  <img class="responsive" src="/favicon.png">
</div>
```

```html
<div class="shape sided-cookie7 medium">
  <img class="responsive" src="/favicon.png">
</div>
```

```html
<div class="shape sided-cookie7 large">
  <img class="responsive" src="/favicon.png">
</div>
```

```html
<div class="shape sided-cookie7 extra">
  <img class="responsive" src="/favicon.png">
</div>
```

```html
<div class="shape sided-cookie7 small-width small-height rotate">
  <img class="responsive" src="/favicon.png">
</div>
```

### Custom Shapes Examples

```html
<button class="circle extra transparent">
  <span class="shape sided-cookie7 max medium-space"></span>
</button>
```

```html
<button class="circle extra fill">
  <span class="shape sided-cookie7 max medium-space"></span>
</button>
```

```html
<div class="shape sided-cookie7 transparent rotate">
  <button class="responsive">
    <i>search</i>
  </button>
</div>
```

```html
<button class="extra fill">
  <i>
    <span class="shape sided-cookie7 max"></span>
  </i>
  <span>Button</span>
</button>
```

```html
<div class="field border prefix">
  <i>
    <span class="shape sided-cookie7 max"></span>
  </i>
  <input>
</div>
```

---

## Sliders (falta detallar)

---

## Snackbards (falta detallar)

Modes: bottom, top

### Bottom Examples (default)

```html
<div class="snackbar">Some text here</div>
```

```html
<div class="snackbar error">Some text here</div>
```

```html
<div class="snackbar primary">Some text here</div>
```

```html
<div class="snackbar secondary">Some text here</div>
```

```html
<div class="snackbar tertiary">Some text here</div>
```

```html
<div class="snackbar">
  <div class="max">Some text here</div>
  <a class="inverse-primary-text">Action</a>
</div>
```

### Top Examples

```html
<div class="snackbar top">Some text here</div>
```

```html
<div class="snackbar error top">Some text here</div>
```

```html
<div class="snackbar primary top">Some text here</div>
```

```html
<div class="snackbar secondary top">Some text here</div>
```

```html
<div class="snackbar tertiary top">Some text here</div>
```

```html
<div class="snackbar top">
  <div class="max">Some text here</div>
  <a class="inverse-primary-text">Action</a>
</div>
```

---

## Spaces

space type: 'small-space', 'medium-space', 'large-space'

Default css:
space type: 'small-space'

### Example 'small-space'

```html
<div>
  <div>Some text here</div>
  <div class="space"></div>
  <div>Some text here</div>
  <div class="space"></div>
  <div>Some text here</div>
</div>
```

### Example 'medium-space', 'large-space'

```html
<div>
  <div>Some text here</div>
  <div class="medium-space"></div>
  <div>Some text here</div>
  <div class="medium-space"></div>
  <div>Some text here</div>
</div>
```

---

## Steppers (no documentado)

---

## Switches (falta detallar)

### Default Switch

```html
<label class="switch">
  <input type="checkbox">
  <span></span>
</label>
```

```html
<label class="switch">
  <input type="checkbox">
  <span></span>
</label>
```

```html
<label class="switch">
  <input type="checkbox" disabled>
  <span></span>
</label>
```

### Switch with icons

```html
<label class="switch">
  <input type="checkbox" checked disabled>
  <span></span>
</label>
```

```html
<label class="switch icon">
  <input type="checkbox">
  <span>
    <i>wifi</i>
  </span>
</label>
```

```html
<label class="switch icon">
  <input type="checkbox">
  <span>
    <i>bluetooth</i>
  </span>
</label>
```

```html
<label class="switch icon">
  <input type="checkbox">
  <span>
    <i>dark_mode</i>
  </span>
</label>
```

```html
<label class="switch icon">
  <input type="checkbox">
  <span>
    <i>close</i>
    <i>done</i>
  </span>
</label>
```

### Switch in field elements

```html
<div class="field middle-align">
  <nav>
    <div class="max">
      <h6>Title</h6>
      <div>Some text here</div>
    </div>
    <label class="switch">
      <input type="checkbox">
      <span></span>
    </label>
  </nav>
</div>
```

```html
<div class="field middle-align">
  <nav>
    <div class="max">
      <h6>Title</h6>
      <div>Some text here</div>
    </div>
    <label class="switch">
      <input type="checkbox">
      <span></span>
    </label>
  </nav>
  <output>Helper text</output>
</div>
```

```html
<div class="field middle-align invalid">
  <nav>
    <div class="max">
      <h6>Title</h6>
      <div>Some text here</div>
    </div>
    <label class="switch">
      <input type="checkbox">
      <span></span>
    </label>
  </nav>
  <output class="invalid">Error text</output>
</div>
```

---

## Tables (falta detallar)

---

## Tabs (falta detallar)

---

## Textareas (falta detallar)

---

## Toolbars (falta detallar)

---

## Tooltip (falta detallar)

---

## Typography (falta detallar)

---

## Waves and ripples (falta detallar)

### Examples

```html
<button class="wave">Wave</button>
```

```html
<button class="ripple">Ripple</button>
```

```html
<button class="slow-ripple">Slow ripple</button>
```

```html
<button class="fast-ripple">Fast ripple</button>
```

```html
<button class="chip wave">Wave</button>
```

```html
<button class="chip ripple">Ripple</button>
```

```html
<button class="chip slow-ripple">Slow ripple</button>
```

```html
<button class="chip fast-ripple">Fast ripple</button>
```
