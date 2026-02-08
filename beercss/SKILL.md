---
name: beercss
description: >
  Expert in BeerCSS Material Design implementation. Provides guidance on components, 
  helpers, responsive layouts, and Material Design 3 patterns.
  Trigger: When creating UI with BeerCSS, Material Design components, or responsive layouts.
version: "1.0.0"
scope: [root, src, components, pages, views, public, static]
auto_invoke: "Creating BeerCSS components or Material Design UI"
---

# 🍺 BeerCSS - Material Design 3 SuperSkill

This skill transforms Gemini CLI into an expert on BeerCSS, a framework that follows the **"Beer Purity Law"** (Settings, Elements, Helpers) to implement Material Design 3 with minimal effort and high performance.

## 🚀 Setup & Installation

BeerCSS can be integrated into any project via CDN or NPM.

### CDN Setup (Recommended for quick prototypes)

Include these tags in your `<head>`:

```html
<link href="https://cdn.jsdelivr.net/npm/beercss@4.0.2/dist/cdn/beer.min.css" rel="stylesheet">
<script type="module" src="https://cdn.jsdelivr.net/npm/beercss@4.0.2/dist/cdn/beer.min.js"></script>
<script type="module" src="https://cdn.jsdelivr.net/npm/material-dynamic-colors@1.1.4/dist/cdn/material-dynamic-colors.min.js"></script>
```

### NPM Installation

```bash
npm i beercss material-dynamic-colors
```

**Import in your main JS/TS file:**

```javascript
import "beercss";
import "material-dynamic-colors";
```

### Versions available
- **Default:** Global styles.
- **Scoped:** Styles applied only to children of `<* class="beer">`.
- **Custom Element:** Styles applied only inside `<beer-css>` tags.

### Basic HTML Boilerplate

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>BeerCSS App</title>
  <link href="https://cdn.jsdelivr.net/npm/beercss@4.0.2/dist/cdn/beer.min.css" rel="stylesheet">
  <script type="module" src="https://cdn.jsdelivr.net/npm/beercss@4.0.2/dist/cdn/beer.min.js"></script>
  <script type="module" src="https://cdn.jsdelivr.net/npm/material-dynamic-colors@1.1.4/dist/cdn/material-dynamic-colors.min.js"></script>
</head>
<body class="light">
  <main class="responsive">
    <!-- Your content here -->
  </main>
</body>
</html>
```

## 🎯 When to Use

Use this skill for:
- Implementing **Material Design 3** interfaces.
- Projects requiring a lightweight, high-performance CSS framework.
- Creating responsive layouts (mobile-first) with minimal code.
- Using complex components like Rails, Bottom Bars, and Modal Dialogs with standard HTML.

## ⚠️ Critical Rules

### ✅ ALWAYS Rules
- **One Element Class:** Use only ONE element class per tag (e.g., `class="button"`).
- **Composition:** Combine the element with multiple helpers (e.g., `class="button fill round extra"`).
- **Purity Law:** Follow the structure: Settings (Theme) -> Elements -> Helpers.
- **Theme on Body:** Always apply `class="light"\` or `class="dark"` to the `<body>`.
- **Responsive Helpers:** Use `s`, `m`, `l` for mobile-first responsiveness.
- **Semantic Tags:** Prefer `<nav>`, `<article>`, `<header>`, `<footer>` and `<main>`.

### ❌ NEVER Rules
- **Multiple Elements:** NEVER put two element classes on the same tag (e.g., NO `class="card button"`).
- **BEM Naming:** NEVER use dependent classes like `.card-header`. Use BeerCSS structure instead.
- **Wrong Nesting:** NEVER put block elements inside inline elements (e.g., NO `div` inside `span`).
- **Multiple Mains:** NEVER use more than one `<main>` tag per document.
- **Ignoring Documentation:** NEVER guess a class name; if it's not in `references/` or `docs/`, it doesn't exist.

## 🏗️ Architecture Overview

BeerCSS architecture is based on the **"Beer Purity Law"**, which simplifies Material Design into three core ingredients.

### 1. Settings (The Theme)
Settings affect the entire document. They are usually applied to the `<body>` tag to set the global theme and primary colors.
- **Example:** `<body class="dark">`

### 2. Elements (The Components)
Elements are the core UI components (tags, widgets, or components). Each tag should have **only one** element class.
- **Example:** `<button>`, `<article class="card">`, `<nav>`.

### 3. Helpers (The Scalability)
Helpers make elements scalable and customizable. You can apply multiple helpers to a single element to modify its appearance, size, spacing, or behavior.
- **Example:** `<button class="fill extra circle">`

### Composition Model
The standard pattern for any BeerCSS component is:
`Element` + `Helpers (Spacing, Colors, Forms, Sizes)`

```html
<!-- Example of composition -->
<article class="card padding elevate round">
  <h5>Card Title</h5>
  <p>Content goes here.</p>
</article>
```

### Responsive System
BeerCSS uses a mobile-first responsive system with three main breakpoints:
- **Small (s):** 0px - 600px
- **Medium (m):** 601px - 1240px
- **Large (l):** 1241px+

## 🛤️ Decision Trees

### Which Component for User Input?
- **Single-line text:** → `input` (within `div class="field"`)
- **Multi-line text:** → `textarea` (within `div class="field"`)
- **Pick from list:** → `select` (within `div class="field"`)
- **Yes/No toggle:** → `label class="switch"`
- **Multiple options:** → `label class="checkbox"`
- **Single option from set:** → `label class="radio"`
- **Range selection:** → `label class="slider"`

### Which Navigation Pattern?
- **Desktop (Left side):** → `nav class="left"` (Navigation Rail)
- **Mobile (Bottom):** → `nav class="bottom"` (Navigation Bar)
- **Top Bar:** → `header` or `nav class="top"`
- **Dropdown/Contextual:** → `menu`
- **Contextual actions/Media controls:** → `nav class="toolbar"`
- **Switch between views:** → `nav class="tabs"`
- **Hierarchical/Collapsible:** → `details` + `summary` (Expansion panels)

### Which Layout Container?
- **Main content area:** → `main class="responsive"`
- **Full-width section:** → `div class="page"`
- **Responsive column grid:** → `div class="grid"`
- **Absolute positioning:** → `div class="layout"`
- **Content block with elevation:** → `article class="card"`

### Which Feedback Component?
- **Critical user action:** → `dialog`
- **Brief notification:** → `div class="snackbar"`
- **Information on hover:** → `div class="tooltip"`
- **Indeterminate wait:** → `progress`
- **Blocking overlay:** → `div class="overlay"`
- **Emphasis on icon/element:** → `label class="badge"`
- **Compact tag/filter:** → `label class="chip"`

### Which Helper for Spacing?
- **External space:** → `margin` (`tiny`, `small`, `medium`, `large`)
- **Internal space:** → `padding` (`tiny`, `small`, `medium`, `large`)
- **Remove default space:** → `no-margin`, `no-padding`
- **Responsive spacing:** → Use with prefix: `s`, `m`, `l` (e.g., `m-padding`)

## 🛠️ Advanced Setup Patterns

### Vite Configuration
For Vite users, ensure your app keeps the original size of CSS files to avoid issues with some BeerCSS styles.

**vite.config.js:**
```javascript
export default {
  build: {
    assetsInlineLimit: 0
  }
}
```

### Dynamic Theme & Colors
BeerCSS supports Material You dynamic colors based on an image or a specific color code.

**Theme Switching (JS):**
```javascript
// Toggle theme
document.body.classList.toggle('dark');
document.body.classList.toggle('light');

// Dynamic Color from hex
ui("theme", "#006400"); // Dark green

// Dynamic Color from image
ui("theme", "https://example.com/image.jpg");
```

### Scoped Implementation
Use the scoped version if you want to apply BeerCSS only to a specific part of your application without affecting global styles.

```html
<link href="beercss.scoped.min.css" rel="stylesheet">
<div class="beer">
  <!-- Only elements here will have BeerCSS styles -->
  <button class="fill">Scoped Button</button>
</div>
```

## 🧩 Component Patterns: Form Controls

### 1. Input
Inputs are wrapped in a `div class="field"`. Labels must come AFTER the input.

#### Basic Patterns
```html
<!-- Filled Input (Default) -->
<div class="field label border">
  <input type="text">
  <label>Label</label>
</div>

<!-- Outlined Input -->
<div class="field label outline">
  <input type="text">
  <label>Label</label>
</div>

<!-- Rounded Input -->
<div class="field label border round">
  <input type="text">
  <label>Label</label>
</div>
```

#### Variations with Icons
```html
<!-- With Prefix Icon -->
<div class="field label prefix border">
  <i>search</i>
  <input type="text">
  <label>Search</label>
</div>

<!-- With Suffix Icon -->
<div class="field label suffix border">
  <input type="password">
  <label>Password</label>
  <i>visibility</i>
</div>
```

#### States & Validation
```html
<!-- Invalid State -->
<div class="field label border invalid">
  <input type="text">
  <label>Username</label>
  <span class="helper">This field is required</span>
</div>

<!-- Disabled State -->
<div class="field label border disabled">
  <input type="text" disabled>
  <label>Disabled Input</label>
</div>
```

**Key Rules for Inputs:**
- Always use `div class="field"` as a wrapper.
- Label goes after the input for the "Material float" effect.
- Use `placeholder=" "` for a pure CSS floating label if not using `beer.min.js`.

### 2. Textarea
Similar to Input, but for long text. It auto-resizes by default unless the `rows` attribute is specified.

#### Basic Pattern
```html
<div class="field label border">
  <textarea></textarea>
  <label>Comments</label>
</div>
```

#### Fixed Height
```html
<div class="field label border">
  <textarea rows="5"></textarea>
  <label>Fixed height</label>
</div>
```

**Key Rules for Textareas:**
- Auto-resize is enabled by default (pure CSS in Chromium, JS elsewhere).
- Same helpers as Input (`border`, `round`, `fill`, etc.) apply.

### 3. Select
Standard dropdown menus wrapped in a field.

#### Basic Pattern
```html
<div class="field label border">
  <select>
    <option disabled selected>Pick one</option>
    <option>Option 1</option>
    <option>Option 2</option>
  </select>
  <label>Category</label>
</div>
```

**Key Rules for Selects:**
- Must be wrapped in `div class="field"`.
- Uses the same helpers as Input.
- Label follows the same "float" logic.

### 4. Checkbox, Radio & Switch
These components use a `label` as a wrapper and an internal `span` for the visual element.

#### Basic Patterns
```html
<!-- Checkbox -->
<label class="checkbox">
  <input type="checkbox">
  <span>Option label</span>
</label>

<!-- Radio Button -->
<label class="radio">
  <input type="radio" name="group1">
  <span>Option 1</span>
</label>

<!-- Switch -->
<label class="switch">
  <input type="checkbox">
  <span>Enable feature</span>
</label>
```

#### Icon Variants
```html
<!-- Switch with Icons -->
<label class="switch icon">
  <input type="checkbox">
  <span>
    <i>close</i>
    <i>done</i>
  </span>
</label>
```

**Key Rules:**
- The `input` must be the first child of the `label`.
- The `span` contains the text or the icon container.
- Use `nav` to group multiple options horizontally.

### 5. Slider
Range selection components.

#### Basic Pattern
```html
<div class="slider">
  <input type="range">
  <span></span>
</div>
```

#### With Tooltip (Value indicator)
```html
<div class="slider">
  <input type="range">
  <span></span>
  <div class="tooltip"></div>
</div>
```

**Key Rules:**
- The `span` element is mandatory for the visual slider track.
- Can be placed inside a `div class="field middle-align"` for form alignment.

## 🧭 Component Patterns: Navigation

### 1. Navigation Rail (Desktop)
A vertical sidebar for desktop layouts.

#### Basic Pattern
```html
<nav class="left">
  <a>
    <i>home</i>
    <span>Home</span>
  </a>
  <a>
    <i>search</i>
    <span>Search</span>
  </a>
</nav>
```

#### Full Width (Drawer-like)
```html
<nav class="left max">
  <header>
    <img src="logo.png" class="circle">
    <h6>App Title</h6>
  </header>
  <a>
    <i>home</i>
    <span>Home</span>
  </a>
</nav>
```

### 2. Navigation Bar (Mobile)
A horizontal bar typically placed at the bottom for small screens.

#### Basic Pattern
```html
<nav class="bottom">
  <a>
    <i>home</i>
    <span>Home</span>
  </a>
  <a>
    <i>search</i>
    <span>Search</span>
  </a>
</nav>
```

### 3. Navigation Tabs
Horizontal tabs for switching views.

#### Basic Pattern
```html
<nav class="tabbed">
  <a class="active">Tab 1</a>
  <a>Tab 2</a>
  <a>Tab 3</a>
</nav>
```

**Key Rules for Navigation:**
- Use `nav class="left"` or `nav class="right"` for rails.
- Use `nav class="bottom"` or `nav class="top"` for bars.
- Use `class="active"` to highlight the current destination.
- Combine with responsive helpers: `class="left l"` (show rail only on large screens).

### 4. Menu
Dropdown menus for temporary choices.

#### Basic Pattern
```html
<div>
  <button>
    <span>Options</span>
    <i>arrow_drop_down</i>
  </button>
  <menu>
    <li><a>Action 1</a></li>
    <li><a>Action 2</a></li>
  </menu>
</div>
```

### 5. Toolbar
Compact containers for contextual actions or media controls.

#### Basic Pattern
```html
<nav class="toolbar">
  <a><i>videocam_off</i></a>
  <a><i>mic</i></a>
  <a class="active"><i>front_hand</i></a>
  <a><i>more_vert</i></a>
</nav>
```

#### Floating Toolbar
```html
<nav class="center-align tiny-space">
  <nav class="toolbar">
    <a><i>mic</i></a>
    <a><i>videocam</i></a>
  </nav>
  <button class="circle error"><i>call_end</i></button>
</nav>
```

#### Docked/Full-width
```html
<nav class="toolbar max">
  <a><i>share</i></a>
  <a><i>edit</i></a>
  <a><i>delete</i></a>
</nav>
```

**Key Rules for Toolbars:**
- Use `nav class="toolbar"`.
- Use `class="vertical"` for vertical orientation.
- Combine with `class="fill"` or `primary-container` for background styles.
- Supports `small-elevate`, `medium-elevate`, and `large-elevate`.

## 🖼️ Component Patterns: Content Display

### 1. Card
Surfaces for displaying related content and actions.

#### Basic Pattern
```html
<article>
  <h5>Card Title</h5>
  <p>Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  <nav>
    <button>Action</button>
  </nav>
</article>
```

#### Image Card
```html
<article>
  <img src="image.jpg" class="responsive">
  <div class="padding">
    <h5>Title</h5>
    <p>Content</p>
  </div>
</article>
```

**Key Rules for Cards:**
- Use the `<article>` tag.
- Use helpers like `elevate`, `border`, or `fill` to style.
- Internal content usually needs a `div class="padding"` for proper spacing.

### 2. List
Continuous vertical indexes of text and images.

#### Basic Pattern
```html
<ul class="list">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

#### Rich List (with Icons & Supporting text)
```html
<ul class="list">
  <li>
    <i>person</i>
    <div class="max">
      <h6>Headline</h6>
      <div>Supporting text</div>
    </div>
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
  </li>
</ul>
```

**Key Rules for Lists:**
- Use `ul class="list"` or `ol class="list"`.
- Use `div class="max"` to allow a content block to take the remaining width.
- Support for images/avatars and secondary actions (icons/buttons).

### 3. Table
Sets of data across rows and columns.

#### Basic Pattern
```html
<table class="border stripes">
  <thead>
    <tr>
      <th>Column 1</th>
      <th>Column 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Data 1</td>
      <td>Data 2</td>
    </tr>
  </tbody>
</table>
```

**Key Rules for Tables:**
- Use the `<table>` tag.
- Combine with helpers like `border`, `stripes`, and `min`.
- For horizontal scroll on small screens, wrap in `<div class="scroll">`.

### 4. Media & Icons
Handling images, videos, and Material Icons.

#### Responsive Media
```html
<img src="image.jpg" class="responsive round">
<video src="video.mp4" class="responsive"></video>
```

#### Icons
```html
<i>home</i> <!-- Default -->
<i class="extra large">face</i> <!-- Sized -->
```

### 5. Typography
Semantic text elements and formatting.

#### Headlines
```html
<h1>Display</h1>
<h4>Headline</h4>
<p class="bold">Important text</p>
```

### 6. Grid (Layout System)
The responsive 12-column grid system.

#### Basic Pattern
```html
<div class="grid">
  <div class="s12 m6 l4">Column 1</div>
  <div class="s12 m6 l4">Column 2</div>
  <div class="s12 m6 l4">Column 3</div>
</div>
```

**Key Rules for Grid:**
- Use `div class="grid"`.
- Immediate children MUST be cells with `s[1-12]`, `m[1-12]`, or `l[1-12]` classes.
- Use `s` for small, `m` for medium, and `l` for large screens.

## ⚡ Component Patterns: Feedback & Actions

### 1. Button
Triggers for user actions.

#### Basic Patterns
```html
<button>Tertiary</button>
<button class="border">Secondary</button>
<button class="fill">Primary</button>
```

#### FAB (Floating Action Button)
```html
<button class="circle extra"><i>add</i></button>
<button class="extend circle"><i>add</i><span>Label</span></button>
```

**Key Rules for Buttons:**
- Use `<button>` or `<a class="button">`.
- Use `class="fill"` for primary actions.
- Use `class="circle"` for icon-only buttons or FABs.
- Use `class="responsive"` to fill the container width.

### 2. Dialog
Modal windows for critical actions or info.

#### Basic Pattern
```html
<dialog id="dialog-id">
  <h5>Dialog Title</h5>
  <div>Message body</div>
  <nav class="right-align">
    <button class="border" data-ui="#dialog-id">Cancel</button>
    <button class="fill" data-ui="#dialog-id">Confirm</button>
  </nav>
</dialog>
```

**Key Rules for Dialogs:**
- Use the `<dialog>` tag.
- Open/Close with `ui("#dialog-id")` or `data-ui="#dialog-id"`.
- Position with `class="left"`, `class="right"`, `class="top"`, `class="bottom"` for drawers/sheets.
- Use `class="modal"` to block the background.

### 3. Snackbar
Brief messages at the bottom/top of the screen.

#### Basic Pattern
```html
<div class="snackbar bottom" id="snackbar-id">
  <i>info</i>
  <span>Message sent!</span>
</div>
```

**Key Rules for Snackbars:**
- Show with `ui("#snackbar-id")`.
- Default timeout is 6000ms.
- Positions: `top`, `bottom` (default).
- Do not show multiple snackbars simultaneously.

### 4. Tooltip
Contextual information on hover.

#### Basic Pattern
```html
<button>
  <span>Action</span>
  <span class="tooltip">Description of action</span>
</button>
```

**Key Rules for Tooltips:**
- Can be a child of the element or a sibling.
- Triggers automatically on hover/focus.
- Use helpers like `top`, `bottom`, `left`, `right` for positioning.

### 5. Progress
Visual indicators of process length or wait time.

#### Basic Pattern
```html
<progress></progress> <!-- Indeterminate linear -->
<progress class="circle"></progress> <!-- Indeterminate circular -->
<progress value="50" max="100"></progress> <!-- Determinate -->
```

**Key Rules for Progress:**
- Use the `<progress>` tag.
- Use `class="circle"` for circular variants.
- Combine with `class="wavy"` for a wavy animation effect.
