# Layout

Layouts are containers that you can place in any position. You can control the positioning of elements using absolute/fixed classes or control the alignment of children using alignment helpers.

## Helpers

**Positions** (Applied to the element itself)
`left`, `center`, `right`, `top`, `middle`, `bottom`

**Alignments** (Applied to the parent container)
`left-align`, `center-align`, `right-align`, `top-align`, `middle-align`, `bottom-align`

## Position examples

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

## Alignments Examples

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

---

## Structural Examples

### Header and Footer

Headers and footers act as `position: sticky` when combined with `fixed`, allowing content to scroll underneath them.

```html
<article class="medium-width medium-height scroll border">
  <header class="fixed bold primary-container">Fixed header</header>
  <div class="padding">
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
    </p>
    <p>
      Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
    </p>
  </div>
  <footer class="fixed bold primary-container">Fixed footer</footer>
</article>

```

### Top App Bar

Standard navigation pattern for mobile and desktop headers.

```html
<header>
  <nav>
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    <h5 class="max">Title</h5>
    <button class="circle transparent">
      <i>attach_file</i>
    </button>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </nav>
</header>

```

### Bottom App Bar

Common pattern for mobile navigation and actions.

```html
<footer>
  <nav>
    <button class="circle transparent">
      <i>check_box</i>
    </button>
    <button class="circle transparent">
      <i>brush</i>
    </button>
    <div class="max"></div> <button class="circle transparent">
      <i>mic</i>
    </button>
    <button class="square round extra primary">
      <i>add</i>
    </button>
  </nav>
</footer>

```

### Empty State

A layout pattern used when there is no data to display.

```html
<div class="medium-height middle-align center-align border">
  <div class="center-align">
    <i class="extra">mail</i>
    <h5>You have no new messages</h5>
    <p>Click the button to start a conversation</p>
    <div class="space"></div>
    <nav class="center-align">
      <button class="round">Send a message</button>
    </nav>
  </div>
</div>

```

## Go to

[Begin](https://www.google.com/search?q=INDEX.md), [Elements](https://www.google.com/search?q=ELEMENTS.md), [Helpers](https://www.google.com/search?q=HELPERS.md), [Settings](https://www.google.com/search?q=SETTINGS.md), [Summary](SUMMARY.md), [Javascript](JAVASCRIPT.md), [beercss.com](https://www.beercss.com)

[Badge](https://www.google.com/search?q=BADGE.md), [Button](https://www.google.com/search?q=BUTTON.md), [Card](https://www.google.com/search?q=CARD.md), [Checkbox](https://www.google.com/search?q=CHECKBOX.md), [Chip](https://www.google.com/search?q=CHIP.md), [Container](CONTAINER.md), [Dialog](DIALOG.md), [Divider](https://www.google.com/search?q=DIVIDER.md), [Expansion](https://www.google.com/search?q=EXPANSION.md), [Grid](GRID.md), [Icon](ICON.md), [Input](https://www.google.com/search?q=INPUT.md), [Layout](https://www.google.com/search?q=LAYOUT.md), [List](LIST.md), [Main layout](https://www.google.com/search?q=MAIN_LAYOUT.md), [Media](https://www.google.com/search?q=MEDIA.md), [Menu](https://www.google.com/search?q=MENU.md), [Navigation](NAVIGATION.md), [Overlay](https://www.google.com/search?q=OVERLAY.md), [Page](https://www.google.com/search?q=PAGE.md), [Progress](PROGRESS.md), [Radio](RADIO.md), [Select](SELECT.md), [Shape](https://www.google.com/search?q=SHAPE.md), [Slider](https://www.google.com/search?q=SLIDER.md), [Snackbar](https://www.google.com/search?q=SNACKBAR.md), [Switch](https://www.google.com/search?q=SWITCH.md), [Table](TABLE.md), [Tabs](https://www.google.com/search?q=TABS.md), [Textarea](https://www.google.com/search?q=TEXTAREA.md), [Tooltip](https://www.google.com/search?q=TOOLTIP.md), [Typography](https://www.google.com/search?q=TYPOGRAPHY.md), [Toolbar](https://www.google.com/search?q=extras/toolbar/TOOLBAR.md)

```


## Go to

[Begin](INDEX.md), [Elements](ELEMENTS.md), [Helpers](HELPERS.md), [Settings](SETTINGS.md), [Summary](SUMMARY.md), [Javascript](JAVASCRIPT.md), [beercss.com](https://www.beercss.com)

[Badge](BADGE.md), [Button](BUTTON.md), [Card](CARD.md), [Checkbox](CHECKBOX.md), [Chip](CHIP.md), [Container](CONTAINER.md), [Dialog](DIALOG.md), [Divider](DIVIDER.md), [Expansion](EXPANSION.md), [Grid](GRID.md), [Icon](ICON.md), [Input](INPUT.md), [Layout](LAYOUT.md), [List](LIST.md), [Main layout](MAIN_LAYOUT.md), [Media](MEDIA.md), [Menu](MENU.md), [Navigation](NAVIGATION.md), [Overlay](OVERLAY.md), [Page](PAGE.md), [Progress](PROGRESS.md), [Radio](RADIO.md), [Select](SELECT.md), [Shape](SHAPE.md), [Slider](SLIDER.md), [Snackbar](SNACKBAR.md), [Switch](SWITCH.md), [Table](TABLE.md), [Tabs](TABS.md), [Textarea](TEXTAREA.md), [Tooltip](TOOLTIP.md), [Typography](TYPOGRAPHY.md), [Toolbar](extras/toolbar/TOOLBAR.md)





