# Cards Examples

Cards group related information and actions into a single, flexible container.
They present content in a clear and structured way, helping users quickly understand, compare, and interact with key information.
Cards are commonly used to display summaries, previews, or actionable content, combining text, media, and controls while keeping the interface organized and visually balanced.

## Element

```html
<article>...</article>
```

## Most used helpers

Media file:

images, videos, svgs

Styles:

default, fill, primary, secondary, tertiary

## Examples for 'default' Style

```html
<article>
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

```html
<article class="round">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

```html
<article class="border">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

```html
<article class="border round">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

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


## Examples for 'primary' Style

```html
<article class="primary-container">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

```html
<article class="round primary-container">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

```html
<article class="border primary-container">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

```html
<article class="border round primary-container">
  <h5>Title</h5>
  <p>Some text here</p>
</article>
```

```html
<article class="primary-container">
  <div class="row">
    <video class="circle large">
      <source src="/dance.mp4" type="video/mp4">
    </video>
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

```html
<article class="round primary-container">
  <div class="row">
    <video class="circle large">
      <source src="/dance.mp4" type="video/mp4">
    </video>
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

```html
<article class="border primary-container">
  <div class="row">
    <video class="circle large">
      <source src="/dance.mp4" type="video/mp4">
    </video>
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

```html
<article class="border round primary-container">
  <div class="row">
    <video class="circle large">
      <source src="/dance.mp4" type="video/mp4">
    </video>
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

```html
<article class="no-padding primary-container">
  <video class="responsive small">
    <source src="/dance.mp4" type="video/mp4">
  </video>
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button class="primary">Button</button>
    </nav>
  </div>
</article>
```

```html
<article class="no-padding round primary-container">
  <video class="responsive small top-round">
    <source src="/dance.mp4" type="video/mp4">
  </video>
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button class="primary">Button</button>
    </nav>
  </div>
</article>
```

```html
<article class="no-padding border primary-container">
  <video class="responsive small">
    <source src="/dance.mp4" type="video/mp4">
  </video>
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button class="primary">Button</button>
    </nav>
  </div>
</article>
```

```html
<article class="no-padding border round primary-container">
  <video class="responsive small top-round">
    <source src="/dance.mp4" type="video/mp4">
  </video>
  <div class="padding">
    <h5>Title</h5>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <nav>
      <button class="primary">Button</button>
    </nav>
  </div>
</article>
```

```html
<article class="no-padding primary-container">
  <video class="responsive medium">
    <source src="/dance.mp4" type="video/mp4">
  </video>
  <div class="row absolute bottom left right padding bottom-shadow white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

```html
<article class="no-padding round primary-container">
  <video class="responsive medium">
    <source src="/dance.mp4" type="video/mp4">
  </video>
  <div class="row absolute bottom left right padding bottom-shadow bottom-round white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

```html
<article class="no-padding border primary-container">
  <video class="responsive medium">
    <source src="/dance.mp4" type="video/mp4">
  </video>
  <div class="row absolute bottom left right padding bottom-shadow white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

```html
<article class="no-padding border round primary-container">
  <video class="responsive medium">
    <source src="/dance.mp4" type="video/mp4">
  </video>
  <div class="row absolute bottom left right padding bottom-shadow bottom-round white-text">
    <h5>Title</h5>
    <div class="max"></div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </div>
</article>
```

```html
<article class="no-padding primary-container">
  <div class="grid no-space">
    <div class="s6">
      <video class="responsive">
        <source src="/dance.mp4" type="video/mp4">
      </video>
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

```html
<article class="no-padding primary-container">
  <div class="grid no-space">
    <div class="s6">
      <video class="responsive">
        <source src="/dance.mp4" type="video/mp4">
      </video>
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
