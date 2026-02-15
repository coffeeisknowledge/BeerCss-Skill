# BeerCSS Super Skill v2.0 - Test Suite

This battery of tests is designed to validate the reliability, accuracy, and strict adherence to documentation of the BeerCSS Agent.

---

## 1. Retrieval Tests (RAG Check)
**Goal:** Verify that the agent correctly accesses and retrieves definitions from the `beercss-v2/helpers/` directory.

### Test 1.1: Spacing Helpers
- **Prompt:** "What are the available helpers for margins and their specific pixel values?"
- **Expected Result:** The agent should list `tiny-margin` (4px), `small-margin` (8px), `margin` (16px), `medium-margin` (24px), and `large-margin` (32px), citing `beercss-v2/helpers/spacing.md`.

### Test 1.2: Elevation Scale
- **Prompt:** "List all available elevation levels and their corresponding Material Design DP values."
- **Expected Result:** The agent should list the scale from `no-elevate` (0dp) to `large-elevate` (16dp) using information from `beercss-v2/helpers/elevation.md`.

---

## 2. Hallucination Trap Tests
**Goal:** Verify that the agent enforces `rules/no-hallucination.md` and refuses to use non-existent classes.

### Test 2.1: Invalid Class Detection
- **Prompt:** "Create a primary button with the class `btn-mega-shadow`."
- **Expected Result:** The agent must **STOP**. It should state that `btn-mega-shadow` is not a BeerCSS class, reference `rules/no-hallucination.md`, and suggest using `fill` combined with a valid elevation helper like `large-elevate`.

### Test 2.2: Structure Correction
- **Prompt:** "Create a card using the `card-header` and `card-body` components."
- **Expected Result:** The agent should explain that BeerCSS does not use those specific classes for card sub-sections. It should provide the correct pattern using standard HTML tags (like `<h5>` for the header and a `div` for the body) inside an `<article>` tag, as documented in `beercss-v2/components/cards.md`.

---

## 3. Implementation Tests
**Goal:** Validate the agent's ability to compose complex layouts by combining multiple components and helpers.

### Test 3.1: Complex Card Layout
- **Prompt:** "Create a horizontal product card. It should have an image on the left taking up half the width on desktop, a title, a description text, and two action buttons (Cancel and Confirm) aligned to the right at the bottom. Use the grid system."
- **Expected Result:** The agent should generate code using:
  - `<article class="no-padding">`
  - `<div class="grid no-space">`
  - `<div class="s12 l6">` for the image cell.
  - `<div class="s12 l6">` for the content cell.
  - `<nav class="right-align">` for the buttons.
  - References to `grid.md`, `cards.md`, and `navigation.md`.

### Test 3.2: Mobile-First Navigation
- **Prompt:** "Implement a responsive navigation system: a bottom navigation bar for mobile and a left navigation rail for desktop."
- **Expected Result:** The agent should provide two `<nav>` elements:
  - One with classes `bottom s` for mobile.
  - One with classes `left m l` for tablet/desktop.
  - Correct internal structure (icons + labels) based on `beercss-v2/components/main-layouts.md`.

---

## 4. Color Token Tests
**Goal:** Verify that the agent correctly identifies and uses tokens defined in `rules/color-system.md`.

### Test 4.1: Custom Styling with Tokens
- **Prompt:** "I need to style a custom element using the 'primary container' color from the current theme. What CSS variable should I use?"
- **Expected Result:** The agent should identify `var(--primary-container)` and its corresponding `on-primary-container` text color, referencing `beercss-v2/rules/color-system.md`.

### Test 4.2: Dark Mode Verification
- **Prompt:** "What is the primary hex color value defined for Dark Mode in this project's design tokens?"
- **Expected Result:** The agent should correctly retrieve `#9ecaff` from the Dark Theme reference in `beercss-v2/rules/color-system.md`.
