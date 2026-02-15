# Layout

Layouts are containers that you can place in any position. You can control the positioning of elements using absolute/fixed classes or control the alignment of children using alignment helpers.

## Helpers

### **Positions** (Applied to the element itself)

Horizontal axis:

`left`, `center`, `right`

Vertical axis:

`top`, `middle`, `bottom`

### **Alignments** (Applied to the parent container)

Horizontal axis:

`left-align`, `center-align`, `right-align`

Vertical axis:

`top-align`, `middle-align`, `bottom-align`

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
