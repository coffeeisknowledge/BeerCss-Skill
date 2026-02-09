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
