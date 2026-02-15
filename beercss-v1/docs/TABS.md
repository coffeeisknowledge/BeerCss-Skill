# Tabs

align: 'default', 'left-align', 'center-align', 'right-align'
page transition: 'page default', 'page left', 'page right'
orientation: 'horizontal', 'vertical'
indicator size: 'min', 'max'

**Default CSS elements**
align: 'left-align'
page transition: 'page default'
orientation: 'horizontal'
indicator: 'max'

Rule: The default CSS elements do not need to be added to the 'class'

### Default Examples

```html
<div>
  <div class="tabs">
    <a class="active">Tab 1</a>
    <a>Tab 2</a>
    <a>Tab 3</a>
  </div>
  <div class="page padding active">
    <h5>Tab 1</h5>
  </div>
  <div class="page padding">
    <h5>Tab 2</h5>
  </div>
  <div class="page padding">
    <h5>Tab 3</h5>
  </div>
</div>
```

```html
<div>
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
  <div class="page padding active">
    <h5>Tab 1</h5>
  </div>
  <div class="page padding">
    <h5>Tab 2</h5>
  </div>
  <div class="page padding">
    <h5>Tab 3</h5>
  </div>
</div>
```

```html
<div>
  <div class="tabs">
    <a class="active">
      <img class="circle" src="/favicon.png">
      <span>Tab 1</span>
    </a>
    <a>
      <img class="circle" src="/favicon.png">
      <span>Tab 2</span>
    </a>
    <a>
      <img class="circle" src="/favicon.png">
      <span>Tab 3</span>
    </a>
  </div>
  <div class="page padding active">
    <h5>Tab 1</h5>
  </div>
  <div class="page padding">
    <h5>Tab 2</h5>
  </div>
  <div class="page padding">
    <h5>Tab 3</h5>
  </div>
</div>
```

### Custom Examples

Can use for align:
- 'center-align'
- 'right-align'
- 'left-align'

Can use for page transition:
- 'page left'
- 'page right'

Can use for orientation:
- 'vertical'

Can use for tab indicator:
- 'min'


```html
<div>
  <div class="tabs min center-align">
    <a class="vertical active">Tab 1</a>
    <a class="vertical">Tab 2</a>
    <a class="vertical">Tab 3</a>
  </div>
  <div class="page padding left active">
    <h5>Tab 1</h5>
  </div>
  <div class="page padding left">
    <h5>Tab 2</h5>
  </div>
  <div class="page padding left">
    <h5>Tab 3</h5>
  </div>
</div>
```

```html
<div>
  <div class="tabs min center-align">
    <a class="active vertical">
      <i>home</i>
      <span>Tab 1</span>
    </a>
    <a class="vertical">
      <i>home</i>
      <span>Tab 2</span>
    </a>
    <a class="vertical">
      <i>home</i>
      <span>Tab 3</span>
    </a>
  </div>
  <div class="page padding active left">
    <h5>Tab 1</h5>
  </div>
  <div class="page padding left">
    <h5>Tab 2</h5>
  </div>
  <div class="page padding left">
    <h5>Tab 3</h5>
  </div>
</div>
```

```html
<div>
  <div class="tabs min center-align">
    <a class="active vertical">
      <img class="circle" src="/favicon.png">
      <span>Tab 1</span>
    </a>
    <a class="vertical">
      <img class="circle" src="/favicon.png">
      <span>Tab 2</span>
    </a>
    <a class="vertical">
      <img class="circle" src="/favicon.png">
      <span>Tab 3</span>
    </a>
  </div>
  <div class="page padding active left">
    <h5>Tab 1</h5>
  </div>
  <div class="page padding left">
    <h5>Tab 2</h5>
  </div>
  <div class="page padding left">
    <h5>Tab 3</h5>
  </div>
</div>
```
