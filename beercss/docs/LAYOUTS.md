## Layout

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
