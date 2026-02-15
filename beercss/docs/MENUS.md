## Menus

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
