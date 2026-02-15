# SKILL.md Estructura Correcta para Gemini CLI

Basado en: https://geminicli.com/docs/core/memport/

---

## Estructura Oficial de Agent Skills en Gemini CLI

### 1. Archivo Principal: SKILL.md

```markdown
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
**Maintainer:** [Your name]
```

---

## 2. Reglas (Siempre Cargadas)

### rules/no-hallucination.md

```markdown
# No Hallucination Rule

## CRITICAL: Verification Protocol

Before generating ANY BeerCSS code, verify:

### Step 1: Component Exists?

```
Is component in ../components/?
├─ YES → Load with @../components/[name].md
└─ NO  → STOP and ASK USER
```

**Example:**
```
User: "Create fancy-slider"

Check: Does ../components/fancy-slider.md exist?
→ NO

Response: "I don't see 'fancy-slider' in BeerCSS documentation.
Did you mean:
1. 'slider' (standard slider component)?
2. Something custom?

Available: @../components/sliders.md"
```

### Step 2: Class Documented?

```
Is class name in component docs?
├─ YES → Use it
└─ NO  → STOP and ASK USER
```

**Example:**
```
User: "Add class='product-card'"

Check: Is 'product-card' in @../components/cards.md?
→ NO (only 'card' exists)

Response: "'product-card' isn't a BeerCSS class.
Should I use 'card' instead?

See: @../components/cards.md"
```

### Step 3: Pattern Matches Examples?

```
Does pattern match examples in docs?
├─ YES → Proceed
├─ SIMILAR → Verify with user first
└─ NO  → ASK USER
```

---

## What to Do When Uncertain

### Scenario A: Component Not Found

```markdown
"I don't see [component-name] in BeerCSS docs.

Similar components:
- [option 1]: @../components/[name].md
- [option 2]: @../components/[name].md

Which should I use, or do you need something custom?"
```

### Scenario B: Class Not Documented

```markdown
"[class-name] isn't in BeerCSS documentation.

From @../components/[component].md, available classes are:
- [list documented classes]

Should I use one of these instead?"
```

### Scenario C: Pattern Unclear

```markdown
"I found [component] in @../components/[name].md

There are multiple patterns. Should I use:
1. [Pattern A with brief description]
2. [Pattern B with brief description]"
```

---

## Never Assume

❌ DON'T create custom classes without asking
❌ DON'T invent component names
❌ DON'T combine components without documentation
❌ DON'T use patterns not in examples

✅ DO verify against @../components/
✅ DO ask when uncertain
✅ DO suggest documented alternatives
✅ DO explain what exists vs what doesn't

---

## Confidence Levels

**High (95-100%):** Component + class in docs → Proceed
**Medium (70-95%):** Similar pattern exists → Verify first
**Low (<70%):** Not in docs → Ask before proceeding

---

## Summary

```
Every component → Check @../components/
Every class → Verify in component docs
Every pattern → Match with examples
When uncertain → ASK, never hallucinate
```
```

### rules/color-system.md

```markdown
# Color System Rule

## Source of Truth

**User's Theme:** styles.css (your custom theme)

**CRITICAL:** Every color decision MUST reference:
1. styles.css CSS variables
2. BeerCSS helpers from @../helpers/colors.md

---

## Allowed Colors

### From styles.css

```css
/* Your theme (example structure) */
:root, .light {
  --primary: #your-color;
  --secondary: #your-color;
  --surface: #your-color;
  --background: #your-color;
}

.dark {
  --primary: #your-dark-color;
  --secondary: #your-dark-color;
  /* ... */
}
```

### From BeerCSS Helpers

See full palette: @../helpers/colors.md

**Semantic colors:**
- primary, secondary, tertiary
- error, surface, background
- primary-text, error-text, etc.

**Named colors:**
- red, blue, green, etc. (with shades 1-10)
- red-text, blue-border, etc.

---

## Verification Protocol

Before using ANY color:

### Step 1: Is it a semantic color?

```
primary, secondary, error, surface?
├─ YES → Check if matches theme intent
│         ├─ YES → Use it
│         └─ NO  → Ask if intentional
└─ NO  → Go to Step 2
```

### Step 2: Is it a BeerCSS named color?

```
red, blue, green, etc. from @../helpers/colors.md?
├─ YES → Check if theme allows
│         ├─ YES → Use it
│         └─ NO  → Ask about theme consistency
└─ NO  → Go to Step 3
```

### Step 3: Is it a CSS variable from styles.css?

```
--custom-color in styles.css?
├─ YES → Use with style="color: var(--custom-color)"
└─ NO  → STOP and ASK USER
```

---

## When to Ask User

### Scenario A: Color Not in Theme

```
User: "Make button neon green"

Check:
1. "neon green" semantic? → NO
2. "green" in BeerCSS? → YES (but is it "neon"?)
3. In styles.css? → NO

Response: "I can use BeerCSS 'green' helper, but it may not be 'neon'.
Should I:
1. Use BeerCSS 'green' helper?
2. Use 'light-green' helper (lighter shade)?
3. Add custom neon green to styles.css?

Your theme: @../rules/color-system.md"
```

### Scenario B: Conflicts with Theme

```
User: "Use red for primary button"

Check:
1. styles.css primary = blue
2. User requests red

Response: "Your theme uses blue for primary (see styles.css).
Should I:
1. Use theme primary (blue)?
2. Use BeerCSS 'red' helper (off-theme)?
3. Update primary in styles.css to red?

Current theme: @../rules/color-system.md"
```

---

## Rules

### ✅ ALLOWED

1. **BeerCSS semantic colors that match theme:**
   ```html
   <button class="fill">Uses theme primary</button>
   <div class="surface">Uses theme surface</div>
   ```

2. **BeerCSS named colors (with caution):**
   ```html
   <span class="error-text">Error message</span>
   <div class="red padding">Red background</div>
   ```

3. **CSS variables from styles.css:**
   ```html
   <div style="background: var(--custom-accent)">...</div>
   ```

### ❌ FORBIDDEN

1. **Random hex colors:**
   ```html
   ❌ <div style="background: #ff5722">...</div>
   ```

2. **Colors not in system:**
   ```html
   ❌ <div class="neon-green">...</div>
   ```

3. **Overriding theme:**
   ```html
   ❌ <button class="primary" style="background: red">...</button>
   ```

---

## Examples

### ✅ CORRECT

```html
<!-- Using theme semantic colors -->
<button class="fill">Primary action</button>
<div class="surface padding">Content area</div>
<span class="error-text">Error message</span>

<!-- Using BeerCSS helpers -->
<div class="blue padding">Blue section</div>
<span class="red-text">Red text</span>

<!-- Using CSS variables -->
<div style="color: var(--custom-accent)">Accent text</div>
```

### ❌ INCORRECT

```html
<!-- Random colors -->
<div style="background: #3f51b5">...</div>

<!-- Non-existent classes -->
<div class="custom-blue">...</div>

<!-- Breaking theme -->
<button class="primary" style="background: green">...</button>
```

---

## Summary

```
Color requested?
├─ In semantic colors? → Check theme match
├─ In BeerCSS colors? → Check theme allows
├─ In styles.css? → Use CSS variable
└─ None of above? → ASK USER

When in doubt → Check @../helpers/colors.md and ASK
```

See: @../helpers/colors.md for complete color reference
```

### rules/decision-protocol.md

```markdown
# Decision Protocol

## When to Ask vs When to Proceed

### Decision Matrix

```
Request Type          | Action        | Why
---------------------|---------------|------------------------
Standard component   | PROCEED       | Exact match in docs
Multiple valid ways  | VERIFY        | Need clarification
Component not found  | ASK           | Might be custom
Custom class         | ASK           | Not in BeerCSS
Custom color         | ASK           | Not in theme
Complex layout       | VERIFY/ASK    | Need specification
```

---

## Level 1: PROCEED (No Questions)

**Criteria:** ALL of these true:
- Component in @../components/
- Pattern exact match in examples
- Uses theme colors from @../rules/color-system.md
- Single clear approach

**Examples:**

```
✅ "Create a primary button"
→ @../components/buttons.md has clear pattern
→ <button class="fill">Primary</button>

✅ "Add padding to card"
→ @../components/cards.md + @../helpers/spacing.md
→ <article class="card padding">...</article>

✅ "Make text red"
→ @../helpers/colors.md has red-text
→ <span class="red-text">...</span>
```

---

## Level 2: VERIFY (Quick Clarification)

**Criteria:** ONE of these true:
- Multiple valid approaches
- Combining 2-3 components
- Responsive considerations
- Layout decisions

**Protocol:**
1. Present 2-3 options
2. Wait for choice
3. Proceed with selected option

**Examples:**

```
⚠️ "Create a login form"

Multiple approaches exist.

Response: "Should the login form include:
1. Username + password + submit?
2. Username + password + remember me + submit?
3. Email + password + forgot password + submit?

I'll use components from:
- @../components/inputs.md
- @../components/buttons.md
- @../components/checkboxes.md (if option 2)"

[Wait for response, then proceed]
```

```
⚠️ "Add navigation"

Multiple patterns exist.

Response: "Which navigation pattern:
1. Desktop sidebar (@../components/navigation.md - left rail)
2. Mobile bottom bar (@../components/navigation.md - bottom)
3. Both responsive (sidebar on desktop, bottom on mobile)?

See options: @../components/navigation.md"

[Wait for choice]
```

---

## Level 3: ASK (Must Get Approval)

**Criteria:** ANY of these true:
- Component not in @../components/
- Class not documented
- Color not in theme (@../rules/color-system.md)
- Pattern very different from examples
- Would need custom CSS

**Protocol:**
1. Identify the issue
2. Explain what exists vs what doesn't
3. Suggest alternatives from docs
4. Wait for decision
5. Proceed ONLY after approval

**Examples:**

```
🛑 "Create fancy-slider component"

Component not found.

Response: "I don't see 'fancy-slider' in BeerCSS docs.

From @../components/, available:
- sliders.md - Standard slider component
- No 'fancy' variant documented

Should I:
1. Use standard slider from @../components/sliders.md?
2. Create custom with additional styling (requires custom CSS)?
3. Something else?

Please specify."

[STOP - wait for decision]
```

```
🛑 "Use class='product-card'"

Class not documented.

Response: "'product-card' isn't a BeerCSS class.

From @../components/cards.md, available:
- card (standard card element)
- Helpers from @../helpers/

This would be a custom class requiring custom CSS.

Should I:
1. Use BeerCSS 'card' class instead?
2. Create 'product-card' as custom class (you'll need to style it)?

Please confirm."

[STOP - wait for confirmation]
```

```
🛑 "Make it neon green"

Color not in theme.

Response: "Neon green isn't in your theme.

From @../rules/color-system.md, available:
- BeerCSS 'green' helper (standard green)
- BeerCSS 'light-green' helper (lighter)
- Theme colors (primary, secondary, etc.)

Should I:
1. Use BeerCSS 'green' helper?
2. Use 'light-green' helper?
3. Add neon green to styles.css first?

See colors: @../helpers/colors.md"

[STOP - wait for decision]
```

---

## Question Format

### ✅ GOOD (Specific + References)

```
"[Issue identified]

From @../[relevant-doc], available options:
- [Option A with description]
- [Option B with description]

Should I use [A] or [B]?"
```

### ❌ BAD (Vague)

```
"Is this okay?"
"What do you want?"
"Should I continue?"
```

---

## Confidence Thresholds

```
95-100% confidence  → PROCEED
70-95% confidence   → VERIFY first
<70% confidence     → ASK before proceeding
```

### Confidence Factors

**Increases confidence:**
- Exact component match in @../components/
- Pattern in examples
- Used frequently in @../templates/

**Decreases confidence:**
- Not in documentation
- Multiple interpretations
- Requires custom code

---

## Escalation Path

```
1. Try exact match in @../components/
   ↓ (no match)
2. Try similar component
   ↓ (no similar)
3. Check if combination works
   ↓ (too complex)
4. ASK USER for clarification
   ↓ (user confirms custom)
5. Explain custom CSS needed
   ↓ (user approves)
6. Create with documentation
```

---

## Summary

```
Standard pattern?
  → PROCEED with @../components/[name].md

Multiple options?
  → VERIFY which approach

Not in docs?
  → ASK before proceeding

Custom needed?
  → ASK for approval + explain implications

When uncertain?
  → Better to ASK than assume wrong
```

**Reference docs as proof:**
- "@../components/ doesn't have X"
- "See @../components/[name].md for available patterns"
- "From @../helpers/colors.md, available colors are..."
```

---

## Uso en SKILL.md

```markdown
# SKILL.md

---
name: beercss
# ...
---

## Critical Rules

@./rules/no-hallucination.md
@./rules/color-system.md
@./rules/decision-protocol.md

## Components

@./components/buttons.md
@./components/cards.md
# etc...

## Helpers

@./helpers/colors.md
@./helpers/spacing.md
# etc...
```

---

## Resumen

**Gemini CLI carga:**

1. **SKILL.md** (siempre)
2. **@./rules/** (siempre - via imports o inline @)
3. **@./components/** (bajo demanda cuando se menciona)
4. **@./helpers/** (bajo demanda cuando se necesita)
5. **@./templates/** (bajo demanda cuando se solicita)

**Ventaja:** Solo carga lo necesario, no todo el skill
