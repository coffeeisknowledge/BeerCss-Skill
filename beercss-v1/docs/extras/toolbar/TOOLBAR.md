# Toolbars Examples

Toolbars group and organize a set of related actions and controls into a single horizontal container.
They provide quick access to primary actions, indicate the current state or active action, and help users interact efficiently with the current context.
Toolbars are commonly used for navigation, media controls, and contextual actions, using icons or icon-based buttons to keep the interface compact and focused.

## Element

```html
<nav class="toolbar">...</nav>
```

## Most used helpers

Modes/Variants:

Default, Floating, Docked

Elevations:

no-elevate, small-elevate, medium-elevate, large-elevate

Orientation:

horizontal, vertical

Styles:

default, fill, primary, secondary, tertiary

## Examples for Default Mode

keys: default & no-elevate & horizontal

```html
<nav class="toolbar">
  <a>
    <i>videocam_off</i>
  </a>
  <a>
    <i>mic</i>
  </a>
  <a class="active">
    <i>front_hand</i>
  </a>
  <a>
    <i>more_vert</i>
  </a>
</nav>
```

```html
<nav class="toolbar">
  <a>
    <i>videocam_off</i>
    <div>Video</div>
  </a>
  <a>
    <i>mic</i>
    <span>Speech</span>
  </a>
  <a class="active">
    <i>front_hand</i>
    <span>Attention</span>
  </a>
  <a>
    <i>more_vert</i>
    <span>More</span>
  </a>
</nav>
```


keys: fill & no-elevate & horizontal

```html
<nav class="toolbar fill">
  <a>
    <i>videocam_off</i>
  </a>
  <a>
    <i>mic</i>
  </a>
  <a class="active">
    <i>front_hand</i>
  </a>
  <a>
    <i>more_vert</i>
  </a>
</nav>
```

```html
<nav class="toolbar fill">
  <a>
    <i>videocam_off</i>
    <div>Video</div>
  </a>
  <a>
    <i>mic</i>
    <span>Speech</span>
  </a>
  <a class="active">
    <i>front_hand</i>
    <span>Attention</span>
  </a>
  <a>
    <i>more_vert</i>
    <span>More</span>
  </a>
</nav>
```


keys: primary & no-elevate & horizontal

```html
<nav class="toolbar primary-container">
  <a>
    <i>videocam_off</i>
  </a>
  <a>
    <i>mic</i>
  </a>
  <a class="active">
    <i>front_hand</i>
  </a>
  <a>
    <i>more_vert</i>
  </a>
</nav>
```

```html
<nav class="toolbar primary-container">
  <a>
    <i>videocam_off</i>
    <div>Video</div>
  </a>
  <a>
    <i>mic</i>
    <span>Speech</span>
  </a>
  <a class="active">
    <i>front_hand</i>
    <span>Attention</span>
  </a>
  <a>
    <i>more_vert</i>
    <span>More</span>
  </a>
</nav>
```


keys: secondary & no-elevate & horizontal

```html
<nav class="toolbar secondary-container">
  <a>
    <i>videocam_off</i>
  </a>
  <a>
    <i>mic</i>
  </a>
  <a class="active">
    <i>front_hand</i>
  </a>
  <a>
    <i>more_vert</i>
  </a>
</nav>
```

```html
<nav class="toolbar secondary-container">
  <a>
    <i>videocam_off</i>
    <div>Video</div>
  </a>
  <a>
    <i>mic</i>
    <span>Speech</span>
  </a>
  <a class="active">
    <i>front_hand</i>
    <span>Attention</span>
  </a>
  <a>
    <i>more_vert</i>
    <span>More</span>
  </a>
</nav>
```


keys: tertiary & no-elevate & horizontal

```html
<nav class="toolbar tertiary-container">
  <a>
    <i>videocam_off</i>
  </a>
  <a>
    <i>mic</i>
  </a>
  <a class="active">
    <i>front_hand</i>
  </a>
  <a>
    <i>more_vert</i>
  </a>
</nav>
```

```html
<nav class="toolbar tertiary-container">
  <a>
    <i>videocam_off</i>
    <div>Video</div>
  </a>
  <a>
    <i>mic</i>
    <span>Speech</span>
  </a>
  <a class="active">
    <i>front_hand</i>
    <span>Attention</span>
  </a>
  <a>
    <i>more_vert</i>
    <span>More</span>
  </a>
</nav>
```


keys: default & small-elevate & horizontal

```html
<nav class="toolbar small-elevate">
  <a>
    <i>videocam_off</i>
  </a>
  <a>
    <i>mic</i>
  </a>
  <a class="active">
    <i>front_hand</i>
  </a>
  <a>
    <i>more_vert</i>
  </a>
</nav>
```

```html
<nav class="toolbar small-elevate">
  <a>
    <i>videocam_off</i>
    <div>Video</div>
  </a>
  <a>
    <i>mic</i>
    <span>Speech</span>
  </a>
  <a class="active">
    <i>front_hand</i>
    <span>Attention</span>
  </a>
  <a>
    <i>more_vert</i>
    <span>More</span>
  </a>
</nav>
```

keys: fill & small-elevate & horizontal

```html
<nav class="toolbar fill small-elevate">
  <a>
    <i>videocam_off</i>
  </a>
  <a>
    <i>mic</i>
  </a>
  <a class="active">
    <i>front_hand</i>
  </a>
  <a>
    <i>more_vert</i>
  </a>
</nav>
```

```html
<nav class="toolbar fill small-elevate">
  <a>
    <i>videocam_off</i>
    <div>Video</div>
  </a>
  <a>
    <i>mic</i>
    <span>Speech</span>
  </a>
  <a class="active">
    <i>front_hand</i>
    <span>Attention</span>
  </a>
  <a>
    <i>more_vert</i>
    <span>More</span>
  </a>
</nav>
```


keys: primary & large-elevate & vertical

```html
<nav class="toolbar primary-container large-elevate vertical">
  <a>
    <i>videocam_off</i>
  </a>
  <a>
    <i>mic</i>
  </a>
  <a class="active">
    <i>front_hand</i>
  </a>
  <a>
    <i>more_vert</i>
  </a>
</nav>
```

```html
<nav class="toolbar primary-container large-elevate vertical">
  <a>
    <i>videocam_off</i>
    <div>Video</div>
  </a>
  <a>
    <i>mic</i>
    <span>Speech</span>
  </a>
  <a class="active">
    <i>front_hand</i>
    <span>Attention</span>
  </a>
  <a>
    <i>more_vert</i>
    <span>More</span>
  </a>
</nav>
```


## Examples for Floating Mode

```html
<nav class="center-align tiny-space">
  <nav class="toolbar">
    <a>
      <i>videocam_off</i>
    </a>
    <a>
      <i>mic</i>
    </a>
    <a class="active">
      <i>front_hand</i>
    </a>
    <a>
      <i>more_vert</i>
    </a>
  </nav>
  <button class="extra round circle error">
    <i>call_end</i>
  </button>
</nav>
```

```html
<nav class="center-align tiny-space m l">
  <nav class="toolbar">
    <a>
      <i>videocam_off</i>
      <div>Video</div>
    </a>
    <a>
      <i>mic</i>
      <span>Mic</span>
    </a>
    <a class="active">
      <i>front_hand</i>
      <span>Attention</span>
    </a>
    <a>
      <i>more_vert</i>
      <span>More</span>
    </a>
  </nav>
  <button class="extra round circle error">
    <i>call_end</i>
  </button>
</nav>
```


## Examples for Docked Mode

```html
<nav class="toolbar max">
  <a>
    <i>videocam_off</i>
  </a>
  <a>
    <i>mic</i>
  </a>
  <a class="active">
    <i>front_hand</i>
  </a>
  <a>
    <i>more_vert</i>
  </a>
</nav>
```

```html
<nav class="toolbar max m l">
  <a>
    <i>videocam_off</i>
    <span>Video</span>
  </a>
  <a>
    <i>mic</i>
    <span>Mic</span>
  </a>
  <a class="active">
    <i>front_hand</i>
    <span>Attention</span>
  </a>
  <a>
    <i>more_vert</i>
    <span>More</span>
  </a>
</nav>
```

