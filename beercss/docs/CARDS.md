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
