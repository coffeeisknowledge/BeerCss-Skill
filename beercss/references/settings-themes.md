# Settings & Theming Reference

Detailed guide for configuring themes, colors, and global settings.

## Default Themes

BeerCSS supports `light` and `dark` themes out of the box.

### Static Setup
Apply the class to the `<body>` tag:
```html
<body class="light">...</body>
<body class="dark">...</body>
```

---

## Dynamic Theming (JS API)

BeerCSS can generate dynamic themes using the `material-dynamic-colors` library.

### Changing the Theme
```javascript
// From a hex color
ui("theme", "#006400");

// From an image URL
ui("theme", "https://example.com/image.jpg");
```

### Changing the Mode
```javascript
// Switch to dark mode
ui("mode", "dark");

// Switch to light mode
ui("mode", "light");

// Auto mode (follows system settings)
ui("mode", "auto");
```

---

## CSS Variables Customization

You can customize the design system by overriding CSS variables in your stylesheet.

### Core Color Variables
- `--primary`, `--on-primary`, `--primary-container`.
- `--secondary`, `--on-secondary`, `--secondary-container`.
- `--tertiary`, `--on-tertiary`, `--tertiary-container`.
- `--error`, `--on-error`, `--error-container`.
- `--surface`, `--on-surface`, `--surface-variant`.
- `--background`, `--on-background`.

### Global Design Variables
- `--size`: Base sizing (default: `1rem`).
- `--font`: Custom font family.
- `--font-icon`: Icon font family.
- `--elevate1`, `--elevate2`, `--elevate3`: Shadow depths.
- `--speed1` to `--speed4`: Animation speeds.

---

## Font Configuration

```css
:root {
  --font: "Roboto Flex", sans-serif;
  --font-icon: "Material Symbols Outlined";
}
```
**Options for icons:**
- `Material Symbols Outlined` (Default)
- `Material Symbols Rounded`
- `Material Symbols Sharp`
- `Material Symbols Subset` (Minimal weight)
