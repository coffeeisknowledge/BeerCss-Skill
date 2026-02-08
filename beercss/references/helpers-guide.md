# BeerCSS Helpers Guide

Complete reference for all BeerCSS utility classes.

## Spacing System

### Margins
- `margin`, `no-margin`, `auto-margin`.
- `tiny-margin`, `small-margin`, `medium-margin`, `large-margin`.
- Directional: `left-margin`, `right-margin`, `top-margin`, `bottom-margin`, `horizontal-margin`, `vertical-margin`.

### Paddings
- `padding`, `no-padding`.
- `tiny-padding`, `small-padding`, `medium-padding`, `large-padding`.
- Directional: `left-padding`, `right-padding`, `top-padding`, `bottom-padding`, `horizontal-padding`, `vertical-padding`.

---

## Color System

### Semantic Colors
- `primary`, `secondary`, `tertiary`, `error`.
- Containers: `primary-container`, etc.
- Text: `primary-text`, etc.
- Border: `primary-border`, etc.

### Named Colors
Available colors: `amber`, `blue`, `blue-grey`, `brown`, `cyan`, `deep-orange`, `deep-purple`, `green`, `grey`, `indigo`, `light-blue`, `light-green`, `lime`, `orange`, `pink`, `purple`, `red`, `teal`, `yellow`.
- Tones: `[color]1` to `[color]10`.
- Usage: `red`, `red-text`, `red-border`.

---

## Layout & Alignment

### Alignment
- `left-align`, `center-align`, `right-align`.
- `top-align`, `middle-align`, `bottom-align`.

### Positioning
- `left`, `right`, `top`, `bottom`, `middle`.
- `front`, `back`.

### Display & Sizes
- `wrap`, `no-wrap`.
- `min`, `max`.
- `auto-width`, `small-width`, `medium-width`, `large-width`.
- `auto-height`, `small-height`, `medium-height`, `large-height`.

---

## Visual Helpers

### Elevate
- `elevate`, `no-elevate`.
- `small-elevate`, `medium-elevate`, `large-elevate`.

### Shape
- `circle`, `square`, `round`.
- `no-round`, `small-round`, `medium-round`, `large-round`.

### Opacity & Effects
- `opacity`, `small-opacity`, `medium-opacity`, `large-opacity`.
- `ripple`, `slow-ripple`, `fast-ripple`.
- `blur`, `small-blur`, `medium-blur`, `large-blur`.

---

## Responsive Breakpoints

| Breakpoint | Range | Prefix |
|------------|-------|--------|
| Small (Mobile) | 0-600px | `s` |
| Medium (Tablet) | 601-1240px | `m` |
| Large (Desktop) | 1241px+ | `l` |

**Usage:** Prefix any spacing or grid class with the breakpoint.
- `s12 m6 l4` (Grid cells).
- `m-padding` (Padding only on medium screens and up).
