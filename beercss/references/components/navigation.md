# Navigation & Layout Reference

Detailed reference for navigation patterns and structural containers.

## Navigation Rail (Left/Right)

### Purpose
Vertical side navigation, typically for desktop.

### Basic Pattern
```html
<nav class="left">
  <a>
    <i>home</i>
    <span>Home</span>
  </a>
</nav>
```

### Variations
- **Left rail:** `class="left"`
- **Right rail:** `class="right"`
- **Full width:** `class="max"`

---

## Navigation Bar (Top/Bottom)

### Purpose
Horizontal navigation, typically for mobile or top headers.

### Basic Pattern
```html
<nav class="bottom">
  <a>
    <i>home</i>
    <span>Home</span>
  </a>
</nav>
```

---

## Tabs

### Purpose
Switching between peer views.

### Basic Pattern
```html
<nav class="tabbed">
  <a class="active">Tab 1</a>
  <a>Tab 2</a>
</nav>
```

---

## Menu

### Purpose
Displays choices on temporary surfaces.

### Basic Pattern
```html
<div class="relative">
  <button>Open Menu</button>
  <menu id="menu-id">
    <li><a>Item 1</a></li>
    <li><a>Item 2</a></li>
  </menu>
</div>
```

### Variations
- **Positioning:** `top`, `bottom`, `left`, `right`.

---

## Toolbar

### Purpose
Groups related actions and controls into a compact container. Ideal for media controls or contextual actions.

### Basic Pattern
```html
<nav class="toolbar">
  <a><i>mic</i></a>
  <a><i>videocam</i></a>
  <a class="active"><i>front_hand</i></a>
</nav>
```

### Variations
- **Modes:** 
  - Default: `class="toolbar"`
  - Docked: `class="toolbar max"` (Full width)
  - Floating: Wrapped in a centered `nav` or `div`.
- **Orientation:**
  - Horizontal (Default)
  - Vertical: `class="toolbar vertical"`
- **Elevations:** `no-elevate`, `small-elevate`, `medium-elevate`, `large-elevate`.
- **Labels:** Icons can be accompanied by `<span>` or `<div>` labels.

---

## Layout Containers

### Main Layout
The standard high-level structure.
```html
<nav class="left l">...</nav>
<nav class="bottom s">...</nav>
<main class="responsive">...</main>
```

### Page
Used for full-width sections or screen animations.
```html
<div class="page active">...</div>
```

### Container
Standard content width wrapper.
```html
<div class="container">...</div>
```
