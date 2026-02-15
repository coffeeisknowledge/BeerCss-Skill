---
name: beercss
description: >
  BeerCSS Material Design 3 expert. Creates components using ONLY documented 
  patterns from beercss.com. Prevents hallucinations by verifying every class 
  and component against official documentation.
version: "2.0.0"
scope: [root, src, components, pages, views, app, public, static, assets]
auto_invoke: "Creating BeerCSS components or Material Design UI"
---

# 🍺 BeerCSS Material Design 3 SuperSkill

Expert in creating Material Design 3 interfaces with BeerCSS framework.

## Critical Rules (ALWAYS LOADED)

@./rules/no-hallucination.md

@./rules/color-system.md

@./rules/decision-protocol.md

---

## Quick Reference

### Most Common Components

**Button:**
```html
<button class="fill">Primary</button>
```
Full docs: @./components/buttons.md

**Input:**
```html
<div class="field label border">
  <input type="text">
  <label>Label</label>
</div>
```
Full docs: @./components/inputs.md

**Card:**
```html
<article class="card padding">
  <h6>Title</h6>
  <p>Content</p>
</article>
```
Full docs: @./components/cards.md

---

## Decision Trees

### Which Component for User Input?

Single-line text → @./components/inputs.md
Multi-line text → @./components/textareas.md
Pick from list → @./components/selects.md
Yes/No toggle → @./components/switches.md
Multiple options → @./components/checkboxes.md
Single option → @./components/radios.md
Range selection → @./components/sliders.md

### Which Navigation?

Desktop sidebar → @./components/navigation.md
Mobile bottom bar → @./components/navigation.md
Temporary menu → @./components/menus.md
Switch views → @./components/tabs.md

### Which Container?

Content area → @./components/containers.md
Card-based → @./components/cards.md
Responsive grid → @./components/grid.md
Full page → @./components/pages.md

### Which Feedback?

User action needed → @./components/dialogs.md
Brief notification → @./components/snackbars.md
Contextual info → @./components/tooltips.md
Loading → @./components/progress.md

---

## Component Index

### Form Controls
@./components/buttons.md
@./components/inputs.md
@./components/textareas.md
@./components/selects.md
@./components/checkboxes.md
@./components/radios.md
@./components/switches.md
@./components/sliders.md

### Navigation
@./components/navigation.md
@./components/menus.md
@./components/tabs.md
@./components/app-bars.md
@./components/toolbars.md

### Content Display
@./components/cards.md
@./components/lists.md
@./components/tables.md
@./components/grid.md
@./components/typography.md

### Feedback & Actions
@./components/dialogs.md
@./components/snackbars.md
@./components/tooltips.md
@./components/progress.md
@./components/badges.md
@./components/chips.md

### Layout
@./components/containers.md
@./components/pages.md
@./components/layouts.md
@./components/spaces.md

---

## Helpers Reference

### Core Helpers
@./helpers/spacing.md
@./helpers/colors.md
@./helpers/responsive.md
@./helpers/sizing.md

### Visual Helpers
@./helpers/elevation.md
@./helpers/shapes.md
@./helpers/opacity.md

### Layout Helpers
@./helpers/alignment.md
@./helpers/positioning.md

### Interactive Helpers
@./helpers/utilities.md

---

## Templates (Real-World Examples)

@./templates/gmail-inbox.md
@./templates/youtube-home.md
@./templates/netflix-browse.md
@./templates/reddit-feed.md
@./templates/uber-ride.md
@./templates/music-player.md
@./templates/material-design-3.md
@./templates/dynamic-colors.md

---

## Verification Protocol

Before generating ANY code:

1. **Check component exists:**
   ```
   Is component in @./components/?
   → YES: Load it
   → NO: ASK USER
   ```

2. **Check class documented:**
   ```
   Is class in component docs?
   → YES: Use it
   → NO: ASK USER
   ```

3. **Check color in theme:**
   ```
   Color in @./rules/color-system.md?
   → YES: Use it
   → NO: ASK USER
   ```

When uncertain → Follow @./rules/decision-protocol.md

---

## Usage Examples

### Creating a Button
```
User: "Create a primary button"

Gemini:
1. Loads @./components/buttons.md
2. Finds "fill" class for primary
3. Generates: <button class="fill">Primary</button>
```

### Preventing Hallucination
```
User: "Create a fancy-card component"

Gemini:
1. Checks @./components/ for "fancy-card"
2. Not found
3. Follows @./rules/no-hallucination.md
4. Asks: "Did you mean 'card' component?"
```

### Respecting Color System
```
User: "Make button bright red"

Gemini:
1. Checks @./rules/color-system.md
2. Finds theme uses blue primary
3. Follows @./rules/decision-protocol.md
4. Asks: "Should I use:
   1) BeerCSS 'red' helper?
   2) Theme primary color?
   3) Add custom red to styles.css?"
```

---

## Resources

**Official Documentation:**
- BeerCSS: https://www.beercss.com
- Material Design 3: https://m3.material.io
- Material Icons: https://fonts.google.com/icons

**Gemini CLI:**
- Skills Docs: https://geminicli.com/docs/core/memport/
- Agent Skills: https://geminicli.com/docs/core/skills/

---

**Version:** 2.0.0
**Last Updated:** 2026-02-15
**Maintainer:** Claude
