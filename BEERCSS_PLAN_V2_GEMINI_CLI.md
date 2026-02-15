# 🍺 BeerCSS SuperSkill v2.0 - Plan Maestro para Gemini CLI

**Ingeniero Senior:** Claude  
**Developer:** Tu  
**Objetivo:** Crear una Agent Skill optimizada para Gemini CLI usando `@` references y documentación actualizada de beercss.com

---

## 📊 Análisis de Material Actualizado

### Lo que Tienes Ahora (EXCELENTE)

```
beercss/
├── docs/ (7,702 líneas - ACTUALIZADO desde web)
│   ├── BUTTONS.md (1,381 líneas - más grande)
│   ├── CARDS.md (573 líneas)
│   ├── BADGES.md (448 líneas)
│   ├── TOOLBARS.md (450 líneas)
│   ├── APP-BARS.md (360 líneas)
│   ├── TABLES.md (345 líneas)
│   ├── NAVIGATIONS.md (313 líneas)
│   ├── LAYOUTS.md (260 líneas)
│   ├── INDEX.md (254 líneas)
│   └── [...27 componentes más]
│
└── templates/ (8 ejemplos reales)
    ├── gmail/ (inbox pattern)
    ├── youtube/ (video app)
    ├── netflix/ (streaming UI)
    ├── reddit/ (social feed)
    ├── uber/ (ride app)
    ├── musicPlayer/
    ├── materialDesign3/
    └── dynamicColors/
```

**Total:** ~8,000+ líneas de documentación oficial actualizada + ejemplos reales

---

## 🎯 Decisión Arquitectónica v2.0

### Nueva Estructura Optimizada para Gemini CLI

```
~/.gemini/skills/beercss/
├── SKILL.md (500-700 líneas - ORQUESTADOR)
│   ├── Metadata
│   ├── Critical Rules
│   ├── Decision Trees
│   ├── Quick Reference
│   └── @./components/[...].md ← Referencias a componentes
│
├── components/ (documentación completa)
│   ├── buttons.md @← docs/BUTTONS.md procesado
│   ├── cards.md @← docs/CARDS.md procesado
│   ├── inputs.md @← docs/INPUTS.md procesado
│   ├── navigation.md @← docs/NAVIGATIONS.md procesado
│   └── [...20+ componentes]
│
├── templates/ (ejemplos reales)
│   ├── gmail-inbox.md
│   ├── youtube-home.md
│   ├── netflix-browse.md
│   └── [...]
│
├── helpers/ (utilities system)
│   ├── spacing.md
│   ├── colors.md
│   ├── typography.md
│   └── responsive.md
│
└── rules/ (reglas de proyecto)
    ├── no-hallucination.md ⭐ NUEVO
    ├── color-system.md ⭐ NUEVO (tu styles.css)
    └── decision-protocol.md ⭐ NUEVO
```

**Innovación clave:** Usar `@` references de Gemini CLI para cargar componentes bajo demanda

---

## 🚀 Capacidades de Gemini CLI que Usaremos

### 1. **@ References** (Progressive Loading)

```markdown
# SKILL.md

## Components

@./components/buttons.md
@./components/cards.md
@./components/inputs.md

## Templates

@./templates/gmail-inbox.md

## Rules

@./rules/no-hallucination.md
@./rules/color-system.md
```

**Ventaja:** Gemini CLI carga solo lo necesario, no todo el skill

### 2. **Inline References** (Contexto Específico)

```markdown
# SKILL.md

When creating buttons:

@./components/buttons.md

Use these patterns, NO custom classes.
```

### 3. **Conditional Loading** (Basado en Prompt)

```markdown
# SKILL.md

## Form Controls

For inputs: @./components/inputs.md
For selects: @./components/selects.md
For checkboxes: @./components/checkboxes.md
```

### 4. **Multi-Reference** (Combinar Múltiples Fuentes)

```markdown
# Creating a login form

@./components/inputs.md
@./components/buttons.md
@./rules/no-hallucination.md
@./rules/color-system.md
```

---

## 📋 Plan de Trabajo (6 Fases)

### FASE 1: Procesar Documentación (3-4 horas)

#### Tarea 1.1: Convertir docs/ a components/

**Objetivo:** Transformar docs raw en archivos optimizados para Gemini CLI

**Input:** `docs/BUTTONS.md` (1,381 líneas)

**Output:** `components/buttons.md` (optimizado)

**Estructura de cada archivo:**

```markdown
# Buttons

Source: https://www.beercss.com/documentation/buttons
Last Updated: [fecha]

## Quick Reference

### Common Patterns

**Default Button:**
```html
<button>Button</button>
```

**Primary (Filled):**
```html
<button class="fill">Primary</button>
```

**Secondary (Border):**
```html
<button class="border">Secondary</button>
```

**Tertiary (Text):**
```html
<button>Tertiary</button>
```

---

## Styles

default, fill, primary, secondary, tertiary

## Sizes

small, medium (default), large, extra

## Elevations

no-elevate (default), small-elevate, medium-elevate, large-elevate

## Orientations

horizontal (default), vertical

---

## Complete Examples

[Todo el contenido de docs/BUTTONS.md]

---

## Rules from Source

1. Default CSS elements don't need class
2. Medium size is default (no class needed)
3. Use `fill` for primary actions
4. Use `border` for secondary actions
5. Use plain `<button>` for tertiary

---

## Common Pitfalls

❌ DON'T:
```html
<button class="button primary">...</button>
```

✅ DO:
```html
<button class="fill">...</button>
```
```

**Acción:**
```bash
# Para cada componente
cp docs/BUTTONS.md components/buttons.md
# Agregar header + Quick Reference + Rules
```

**Componentes a procesar (orden de prioridad):**

**P0 (Must have - 6 componentes):**
1. buttons.md (BUTTONS.md)
2. inputs.md (INPUTS.md)
3. cards.md (CARDS.md)
4. navigation.md (NAVIGATIONS.md)
5. dialogs.md (DIALOGS.md)
6. grid.md (GRID.md)

**P1 (Important - 8 componentes):**
7. selects.md (SELECTS.md)
8. checkboxes.md (CHECKBOXES.md)
9. radios.md (RADIOS.md)
10. switches.md (SWITCHES.md)
11. textareas.md (TEXTAREAS.md)
12. tabs.md (TABS.md)
13. lists.md (LISTS.md)
14. tables.md (TABLES.md)

**P2 (Nice to have - resto):**
15-38. Resto de componentes

**Estimado:** 20 min por componente × 38 = ~13 horas TOTAL  
**MVP (P0):** 2 horas  
**P0+P1:** 4.5 horas

---

#### Tarea 1.2: Crear helpers/ modulares

**Objetivo:** Dividir HELPERS.md en archivos específicos

**Output:**

```
helpers/
├── spacing.md (margin, padding, gap)
├── colors.md (paleta completa)
├── typography.md (text sizes, weights)
├── responsive.md (breakpoints s/m/l)
├── elevation.md (shadows)
├── shapes.md (border-radius)
└── utilities.md (misc helpers)
```

**Contenido de cada archivo:**

```markdown
# Spacing Helpers

Source: https://www.beercss.com/documentation/helpers#spacing

## Margin

- `margin` - Default margin
- `no-margin` - Remove margin
- `tiny-margin` - 4px
- `small-margin` - 8px
- `medium-margin` - 16px
- `large-margin` - 24px

### Directional
- `left-margin`, `right-margin`
- `top-margin`, `bottom-margin`
- `horizontal-margin`, `vertical-margin`

## Padding

[Similar structure]

## Gap (Grid/Flex)

[Gap utilities]

---

## Examples

```html
<!-- Card with padding -->
<article class="card padding">...</article>

<!-- Section with vertical spacing -->
<section class="vertical-margin">...</section>
```

---

## Rules

1. Use semantic helpers before custom CSS
2. Combine multiple spacing classes
3. Responsive spacing: `<div class="small-padding m large-padding l">`
```

**Estimado:** 2 horas

---

#### Tarea 1.3: Procesar templates/

**Objetivo:** Convertir ejemplos Vue a documentación markdown

**Input:** `templates/gmail/home.vue`

**Output:** `templates/gmail-inbox.md`

```markdown
# Gmail Inbox Template

Source: BeerCSS Templates - Gmail
Pattern: Email List with Actions

## Preview

![Gmail Inbox Pattern]

## Structure

```
page
├── toolbar (actions row)
│   ├── checkbox (select all)
│   ├── refresh button
│   ├── more button
│   └── pagination
└── email list
    ├── email row
    │   ├── checkbox
    │   ├── star button
    │   ├── avatar
    │   ├── content (truncated)
    │   └── timestamp
    └── divider
```

## Complete HTML (BeerCSS)

```html
<div class="page right active">
  <!-- Toolbar -->
  <div class="row m l">
    <label class="checkbox">
      <input type="checkbox" aria-label="select all emails">
      <span></span>
    </label>
    
    <button class="circle transparent">
      <i>refresh</i>
    </button>
    
    <button class="circle transparent">
      <i>more_vert</i>
    </button>
    
    <div class="max"></div>
    
    <label>from 1 to 50</label>
    
    <button class="circle transparent">
      <i>arrow_back</i>
    </button>
    
    <button class="circle transparent">
      <i>arrow_forward</i>
    </button>
  </div>
  
  <div class="space m l"></div>
  
  <!-- Email List -->
  <div class="row">
    <label class="checkbox m l">
      <input type="checkbox" aria-label="select email">
      <span></span>
    </label>
    
    <button class="circle transparent m l">
      <i>star_outline</i>
    </button>
    
    <button class="small circle s">A</button>
    
    <a class="max truncate left-align">
      <b>From - </b>
      <b>Subject - </b>
      <span>Preview text...</span>
    </a>
    
    <label>12:03</label>
  </div>
  
  <hr class="m l">
  <hr class="small s">
  
  <!-- Repeat for each email -->
</div>
```

## Key Patterns Used

1. **Page Layout:** `class="page right active"`
2. **Toolbar:** `class="row m l"` (show on medium/large)
3. **Checkbox:** Standard BeerCSS pattern
4. **Icon Buttons:** `class="circle transparent"`
5. **Spacer:** `class="max"` for flex spacing
6. **Truncation:** `class="truncate"` for long text
7. **Responsive Dividers:** Different for mobile/desktop

## Components Referenced

@./components/buttons.md
@./components/checkboxes.md
@./helpers/responsive.md

## Use Case

Perfect for:
- Email clients
- Message lists
- Notification feeds
- Any list with selection + actions
```

**Templates a procesar:**
1. gmail-inbox.md (email list)
2. youtube-home.md (video grid)
3. netflix-browse.md (media cards)
4. reddit-feed.md (social posts)
5. uber-ride.md (map + actions)
6. music-player.md (player controls)
7. material-design-3.md (showcase)
8. dynamic-colors.md (theming)

**Estimado:** 1 hora por template × 8 = 8 horas (opcional para v1.0)

---

### FASE 2: Crear SKILL.md Orquestador (3-4 horas)

#### Tarea 2.1: Metadata con @ references

```yaml
---
name: beercss
description: >
  BeerCSS Material Design 3 expert with hallucination prevention.
  Uses ONLY documented components from official beercss.com.
  Trigger: When creating UI with BeerCSS or Material Design components.
version: "2.0.0"
scope: [root, src, components, pages, views, app, public, static, assets]
auto_invoke: "Creating BeerCSS components or Material Design UI"
imports:
  - ./rules/no-hallucination.md
  - ./rules/color-system.md
  - ./rules/decision-protocol.md
---
```

**CRITICAL:** `imports` carga reglas SIEMPRE, antes de cualquier generación

#### Tarea 2.2: Critical Rules con @ references

```markdown
# 🍺 BeerCSS SuperSkill v2.0

## ⚠️ CRITICAL RULES

@./rules/no-hallucination.md

@./rules/color-system.md

@./rules/decision-protocol.md

### ✅ ALWAYS Rules

1. **ONLY use components from documentation**
   - Every class must exist in @./components/
   - If unsure → Ask user before inventing

2. **Follow color system**
   - Use ONLY colors from @./rules/color-system.md
   - NO custom colors without user approval

3. **One element class per tag**
   - ❌ NO `class="button card"`
   - ✅ YES `class="button"` + helpers

4. **Verify before generating**
   - Check component exists in @./components/
   - Check pattern in documentation
   - If not found → Ask user

### ❌ NEVER Rules

1. **NEVER hallucinate components**
   - NO `class="fancy-button"` unless in docs
   - NO `class="product-card"` unless documented
   
2. **NEVER ignore color system**
   - Colors are in @./rules/color-system.md
   - Light mode and dark mode defined there
   
3. **NEVER assume features exist**
   - If component not in @./components/ → Ask
   - If pattern uncertain → Reference docs
```

#### Tarea 2.3: Decision Trees con @ references

```markdown
## 🛤️ Decision Trees

### Which Component for User Input?

@./components/inputs.md

Single-line text        → Input (see above)
Multi-line text         → @./components/textareas.md
Pick from list          → @./components/selects.md
Yes/No toggle           → @./components/switches.md
Multiple options        → @./components/checkboxes.md
Single option from set  → @./components/radios.md
Range selection         → @./components/sliders.md

### Which Navigation Pattern?

@./components/navigation.md

Desktop sidebar         → Navigation rail (see above)
Mobile bottom          → Bottom navigation bar
Temporary menu         → @./components/menus.md
Switch between views   → @./components/tabs.md

### Which Container?

Main content           → @./components/containers.md
Card-based content     → @./components/cards.md
Responsive grid        → @./components/grid.md
Full-page section      → @./components/pages.md

### Which Feedback?

User action needed     → @./components/dialogs.md
Brief notification     → @./components/snackbars.md
Contextual info        → @./components/tooltips.md
Loading state          → @./components/progress.md
```

#### Tarea 2.4: Quick Reference

```markdown
## 🚀 Quick Reference

### Most Common Patterns

**Button (Primary):**
```html
<button class="fill">Action</button>
```
Full docs: @./components/buttons.md

**Input (Filled):**
```html
<div class="field label border">
  <input type="text">
  <label>Label</label>
</div>
```
Full docs: @./components/inputs.md

**Card (Basic):**
```html
<article class="card">
  <div class="padding">Content</div>
</article>
```
Full docs: @./components/cards.md

**Grid (Responsive):**
```html
<div class="grid">
  <div class="s12 m6 l4">Column</div>
</div>
```
Full docs: @./components/grid.md

**Navigation (Desktop):**
```html
<nav class="left l">
  <a><i>home</i><span>Home</span></a>
</nav>
```
Full docs: @./components/navigation.md
```

#### Tarea 2.5: Component Index con @ references

```markdown
## 📚 Component Index

### Form Controls
- Buttons: @./components/buttons.md
- Inputs: @./components/inputs.md
- Textareas: @./components/textareas.md
- Selects: @./components/selects.md
- Checkboxes: @./components/checkboxes.md
- Radios: @./components/radios.md
- Switches: @./components/switches.md
- Sliders: @./components/sliders.md

### Navigation
- Navigation: @./components/navigation.md
- Menus: @./components/menus.md
- Tabs: @./components/tabs.md
- App Bars: @./components/app-bars.md
- Toolbars: @./components/toolbars.md

### Content Display
- Cards: @./components/cards.md
- Lists: @./components/lists.md
- Tables: @./components/tables.md
- Grid: @./components/grid.md
- Typography: @./components/typography.md

### Feedback
- Dialogs: @./components/dialogs.md
- Snackbars: @./components/snackbars.md
- Tooltips: @./components/tooltips.md
- Progress: @./components/progress.md
- Badges: @./components/badges.md
- Chips: @./components/chips.md

### Layout
- Containers: @./components/containers.md
- Pages: @./components/pages.md
- Layouts: @./components/layouts.md
- Spaces: @./components/spaces.md

### Helpers
- Spacing: @./helpers/spacing.md
- Colors: @./helpers/colors.md
- Typography: @./helpers/typography.md
- Responsive: @./helpers/responsive.md
- Elevation: @./helpers/elevation.md
- Shapes: @./helpers/shapes.md

### Templates (Real Examples)
- Gmail Inbox: @./templates/gmail-inbox.md
- YouTube Home: @./templates/youtube-home.md
- Netflix Browse: @./templates/netflix-browse.md
```

**Estimado Fase 2:** 3-4 horas

---

### FASE 3: Crear Reglas de Proyecto (2 horas) ⭐ NUEVO

#### Tarea 3.1: no-hallucination.md

```markdown
# No Hallucination Rule

## CRITICAL PRINCIPLE

**NEVER create components, classes, or patterns that don't exist in the official documentation.**

---

## Verification Protocol

Before generating ANY BeerCSS code:

1. **Check component exists**
   ```
   Is [component-name].md in @./components/?
   └─ YES → Proceed
   └─ NO  → ASK USER
   ```

2. **Check class exists in component**
   ```
   Does class exist in component docs?
   └─ YES → Use it
   └─ NO  → ASK USER
   ```

3. **Check pattern is documented**
   ```
   Is this exact pattern in examples?
   └─ YES → Use it
   └─ NO  → Find closest match or ASK USER
   ```

---

## When to Ask User

### Scenario 1: Component Not Found

**Example:**
```
User: "Create a fancy-card component"

Gemini Check:
- fancy-card.md in components/? → NO
- Similar in documentation? → card.md exists

Response:
"I found 'card' component in BeerCSS documentation, but not 'fancy-card'. 
Did you mean the standard card component? Or do you want me to use card 
with custom styling (which would require custom CSS)?"
```

### Scenario 2: Class Not Documented

**Example:**
```
User: "Add class='product-card' to the div"

Gemini Check:
- 'product-card' in BeerCSS docs? → NO
- Custom class detected → HALT

Response:
"'product-card' is not a BeerCSS class. This would be a custom class.
Should I:
1. Use BeerCSS 'card' class instead?
2. Create this as a custom class (requires custom CSS)?
Please confirm."
```

### Scenario 3: Pattern Uncertain

**Example:**
```
User: "Create a button with a gradient background"

Gemini Check:
- Button component exists → YES
- Gradient pattern in docs? → NO (only solid colors)

Response:
"BeerCSS buttons support solid colors (fill, primary, secondary).
Gradients would require custom CSS. Should I:
1. Use a solid color button (fill)?
2. Add custom gradient CSS?
Please specify."
```

---

## Allowed Assumptions

You MAY assume standard HTML/BeerCSS patterns:

✅ Combining helpers: `class="button fill small-round"`
✅ Responsive classes: `class="s12 m6 l4"`
✅ Standard HTML attributes: `type`, `id`, `name`, etc.
✅ Documented variations in component docs

You MAY NOT assume:

❌ Custom component names
❌ Undocumented classes
❌ Patterns not in examples
❌ Features from other frameworks

---

## Error Recovery

If you realize you've hallucinated:

1. **Stop generation**
2. **Admit error:** "I apologize, [class/component] is not in BeerCSS docs"
3. **Suggest alternative:** "The correct approach is [documented pattern]"
4. **Regenerate** with correct pattern

---

## Examples

### ❌ WRONG (Hallucination)

```html
<!-- Invented classes -->
<div class="product-card elevated fancy-border">
  <div class="card-header">Title</div>
  <div class="card-body">Content</div>
</div>
```

**Problems:**
- `product-card` - Not documented
- `elevated` - Wrong (should be `elevate` or `small-elevate`)
- `fancy-border` - Not documented
- `card-header`, `card-body` - Not BeerCSS pattern

### ✅ CORRECT (Documented)

```html
<!-- From @./components/cards.md -->
<article class="card small-elevate">
  <div class="padding">
    <h6>Title</h6>
    <p>Content</p>
  </div>
</article>
```

**Why correct:**
- `card` - Documented in cards.md
- `small-elevate` - Documented elevation helper
- `padding` - Documented spacing helper
- `<h6>`, `<p>` - Standard HTML

---

## Confidence Levels

### High Confidence (Generate Immediately)

- Component in @./components/
- Exact pattern in examples
- Standard BeerCSS helper

### Medium Confidence (Verify First)

- Similar pattern exists
- Combining multiple components
- Complex layout

### Low Confidence (Ask User)

- Component not found
- Pattern very different from docs
- Requires custom CSS

---

## Summary

```
Documentation exists? 
  → YES → Use it
  → NO  → ASK USER

Pattern uncertain?
  → ASK USER

Custom class requested?
  → WARN USER + ask confirmation
```

**Golden Rule:** When in doubt, ASK. Never hallucinate.
```

#### Tarea 3.2: color-system.md

```markdown
# Color System Rule

## Source of Truth

**File:** `styles.css` (user's custom theme)

**CRITICAL:** All color decisions MUST reference this file.

---

## Theme Structure

### Light Mode

```css
/* From styles.css */
:root, .light {
  --primary: #your-primary-color;
  --secondary: #your-secondary-color;
  --surface: #your-surface-color;
  --background: #your-bg-color;
  --on-primary: #your-on-primary;
  /* ... more variables ... */
}
```

### Dark Mode

```css
/* From styles.css */
.dark {
  --primary: #your-dark-primary;
  --secondary: #your-dark-secondary;
  --surface: #your-dark-surface;
  --background: #your-dark-bg;
  /* ... more variables ... */
}
```

---

## Rules

### ✅ ALLOWED

1. **Use BeerCSS color helpers**
   ```html
   <div class="primary">...</div>
   <button class="surface">...</button>
   <span class="error-text">...</span>
   ```

2. **Use CSS variables from styles.css**
   ```html
   <div style="background: var(--primary)">...</div>
   ```

3. **Use BeerCSS semantic colors**
   ```html
   <button class="fill">Primary action</button>
   <button class="border">Secondary action</button>
   ```

### ❌ FORBIDDEN

1. **NO custom colors not in styles.css**
   ```html
   ❌ <div style="background: #ff5722">...</div>
   ❌ <button style="color: blue">...</button>
   ```

2. **NO overriding theme colors**
   ```html
   ❌ <div class="primary" style="background: red">...</div>
   ```

3. **NO assuming colors**
   ```html
   ❌ class="pink-background"  (unless in styles.css)
   ❌ class="custom-blue"      (unless in styles.css)
   ```

---

## When User Requests Custom Color

### Scenario: User asks for specific color

```
User: "Make the button red"

Gemini Check:
1. Is "red" a BeerCSS color? → YES (red is a helper)
2. Is it in styles.css theme? → CHECK styles.css
3. Does it match theme? → If NO → ASK

Response options:
A) If "red" fits theme:
   "<button class="red">...</button>"

B) If "red" conflicts with theme:
   "I see you want a red button, but your theme uses [primary-color] 
    for primary actions. Should I:
    1. Use BeerCSS 'red' helper (may not match theme)?
    2. Use your theme's primary color instead?
    3. Add custom red to styles.css?"
```

---

## Color Helpers Reference

From BeerCSS documentation (@./helpers/colors.md):

**Semantic:**
- `primary`, `secondary`, `tertiary`
- `surface`, `background`, `error`, `success`

**Named Colors:**
- `red`, `pink`, `purple`, `deep-purple`
- `indigo`, `blue`, `light-blue`, `cyan`
- `teal`, `green`, `light-green`, `lime`
- `yellow`, `amber`, `orange`, `deep-orange`
- `brown`, `grey`, `blue-grey`

**Text Variants:**
- Add `-text` suffix: `primary-text`, `error-text`

**Border Variants:**
- Add `-border` suffix: `primary-border`

---

## Theme Switching

### Respecting Light/Dark Modes

```html
<!-- Theme applied to body -->
<body class="light">...</body>
<body class="dark">...</body>

<!-- Colors auto-adjust based on theme -->
<button class="fill">
  <!-- primary color changes based on light/dark -->
</button>
```

**Rule:** NEVER hardcode colors that should respond to theme

---

## Custom Colors Workflow

If user needs custom color not in styles.css:

1. **Inform user:**
   ```
   "This color isn't in your theme (styles.css). 
    To add it properly:
    1. Add to styles.css: --custom-color: #value
    2. Then use: style="background: var(--custom-color)"
    
    Or should I use an existing theme color instead?"
   ```

2. **Wait for confirmation**

3. **If approved:** Use inline style with CSS variable
   ```html
   <div style="background: var(--custom-accent)">...</div>
   ```

---

## Examples

### ✅ CORRECT

```html
<!-- Using theme colors -->
<button class="fill">Primary</button>
<div class="surface padding">Surface container</div>
<span class="error-text">Error message</span>

<!-- Using BeerCSS helpers that match theme -->
<article class="card primary">...</article>
```

### ❌ INCORRECT

```html
<!-- Random colors -->
<button style="background: #3f51b5">...</button>

<!-- Overriding theme -->
<div class="primary" style="background: red">...</div>

<!-- Assuming colors exist -->
<div class="my-custom-blue">...</div>
```

---

## Verification Checklist

Before using any color:

- [ ] Is it a BeerCSS semantic color? (primary, surface, etc.)
- [ ] Is it a BeerCSS named color? (red, blue, etc.)
- [ ] Is it a CSS variable in styles.css?
- [ ] Does it respect light/dark theme?

If ALL answers are YES → Use it
If ANY answer is NO → Ask user

---

## Summary

```
Color from BeerCSS helpers?
  → YES → Use it (check theme consistency)
  → NO  → Check styles.css

Color in styles.css?
  → YES → Use CSS variable
  → NO  → ASK USER before using

Custom color requested?
  → ASK: "Should I add to styles.css or use existing?"
```

**Golden Rule:** Theme consistency > individual color requests
```

#### Tarea 3.3: decision-protocol.md

```markdown
# Decision Protocol

## When to Ask vs When to Decide

**Purpose:** Guide Gemini CLI on when to proceed vs when to consult user

---

## Decision Matrix

### ✅ PROCEED WITHOUT ASKING

**Criteria:** All of these are true:
1. Component exists in documentation
2. Pattern is exact match from docs
3. Uses theme colors from styles.css
4. Follows BeerCSS conventions

**Examples:**
```
User: "Create a primary button"
→ PROCEED (standard pattern in buttons.md)

User: "Add a card with padding"
→ PROCEED (standard pattern in cards.md)

User: "Make a responsive grid"
→ PROCEED (standard pattern in grid.md)
```

---

### ⚠️ VERIFY THEN PROCEED

**Criteria:** One of these is true:
1. Combining multiple components
2. Complex layout
3. Similar pattern exists but not exact
4. Multiple valid approaches

**Examples:**
```
User: "Create a login form"
→ VERIFY: "Should I include: username, password, remember me, submit?"
→ THEN PROCEED with confirmed spec

User: "Add navigation"
→ VERIFY: "Desktop sidebar, mobile bottom bar, or both?"
→ THEN PROCEED with choice

User: "Create a dashboard"
→ VERIFY: "What sections/widgets should I include?"
→ THEN PROCEED with spec
```

**Protocol:**
1. Ask clarifying question
2. Present 2-3 options
3. Wait for response
4. Proceed with confirmed approach

---

### 🛑 ASK USER (REQUIRED)

**Criteria:** ANY of these is true:
1. Component not in documentation
2. Custom class requested
3. Color not in theme
4. Pattern significantly different from docs
5. Would require custom CSS

**Examples:**
```
User: "Create a fancy-slider component"
→ ASK: "BeerCSS has 'slider' component. Did you mean that, or something custom?"

User: "Use class='product-card'"
→ ASK: "product-card isn't a BeerCSS class. Should I use 'card' instead or create custom?"

User: "Make it neon green"
→ ASK: "Neon green isn't in your theme. Should I add it to styles.css?"

User: "Create like Twitter's layout"
→ ASK: "I can create a similar layout. Which specific features do you want?"
```

**Protocol:**
1. Identify the uncertainty
2. Explain why asking
3. Provide alternatives
4. Wait for decision
5. Proceed ONLY after confirmation

---

## Question Format

### Good Questions (Specific)

✅ "Should I use navigation rail (desktop sidebar) or bottom bar (mobile)?"
✅ "The theme uses blue primary. Should the button be blue or use error red?"
✅ "This pattern isn't in docs. Should I create with custom CSS or use closest match?"

### Bad Questions (Vague)

❌ "Is this okay?"
❌ "Should I proceed?"
❌ "What do you want?"

---

## Decision Trees

### Component Selection

```
Component exists in docs?
├─ YES → Exact pattern in examples?
│         ├─ YES → PROCEED
│         └─ NO  → VERIFY approach
└─ NO  → Similar component exists?
           ├─ YES → ASK which to use
           └─ NO  → ASK if custom needed
```

### Color Selection

```
Color requested?
├─ In BeerCSS helpers? (primary, red, etc.)
│  ├─ YES → Matches theme?
│  │         ├─ YES → PROCEED
│  │         └─ NO  → ASK if intentional
│  └─ NO  → In styles.css?
│            ├─ YES → PROCEED with CSS var
│            └─ NO  → ASK to add or use alternative
```

### Layout Creation

```
Layout request?
├─ Simple (1 component)
│  └─ PROCEED
├─ Medium (2-4 components)
│  └─ VERIFY approach
└─ Complex (5+ components or full page)
   └─ ASK for spec/wireframe
```

---

## Examples by Complexity

### Simple (Proceed)

```
User: "Create a submit button"

Decision: PROCEED
- Component: buttons.md ✓
- Pattern: fill button ✓
- Color: primary (theme) ✓

<button class="fill">Submit</button>
```

### Medium (Verify)

```
User: "Create a product card"

Decision: VERIFY
- Component: cards.md ✓
- Pattern: needs clarification
- Layout: multiple options

Response: "Should the product card include:
1. Image + title + price + button?
2. Image + title + description + actions?
3. Custom layout?

I'll use BeerCSS card component with your chosen structure."

[Wait for response]
```

### Complex (Ask)

```
User: "Create an e-commerce homepage"

Decision: ASK
- Scope: very large
- Components: many
- Layout: needs specification

Response: "I can create an e-commerce homepage with BeerCSS. 
To ensure I build what you need, please specify:

1. Header: Logo + navigation + search + cart?
2. Hero section: Carousel, static image, or video?
3. Product grid: How many columns (desktop/mobile)?
4. Featured sections: Best sellers, new arrivals, categories?
5. Footer: Links, social, newsletter signup?

Or should I create a basic layout and we refine from there?"

[Wait for response]
```

---

## Confidence Thresholds

### High Confidence (90-100%)
- Exact component from docs
- Standard helper combination
- Simple single-component request
→ **Action: PROCEED**

### Medium Confidence (60-89%)
- Component exists but multiple valid patterns
- Combining 2-3 components
- Moderate complexity
→ **Action: VERIFY approach**

### Low Confidence (< 60%)
- Component not in docs
- Significantly different from examples
- Requires custom CSS
- Complex multi-component layout
→ **Action: ASK USER**

---

## Response Templates

### When Verifying

```
"I can create [X] with BeerCSS. 
I see these options:

1. [Option A with brief description]
2. [Option B with brief description]
3. [Option C with brief description]

Which approach should I use?"
```

### When Asking About Uncertainty

```
"I notice [issue/uncertainty].

In BeerCSS documentation:
- [What exists]
- [What doesn't exist]

Should I:
1. [Suggested approach A]
2. [Suggested approach B]
3. [Custom solution]

Please advise."
```

### When Component Not Found

```
"[Component-name] isn't in BeerCSS documentation.

Similar components:
- [Similar A] - [brief description]
- [Similar B] - [brief description]

Should I use one of these, or create a custom component?"
```

---

## Escalation Path

```
1. Try to match with documented component
   ↓ (no match)
2. Try to find similar component
   ↓ (no similar)
3. Check if combination of components works
   ↓ (too complex)
4. Ask user for clarification/decision
   ↓ (user confirms custom)
5. Explain what custom CSS would be needed
   ↓ (user approves)
6. Create with custom CSS + document it
```

---

## Summary

```
Standard pattern?
  → PROCEED

Multiple valid options?
  → VERIFY with user

Not in documentation?
  → ASK before proceeding

Complex request?
  → ASK for specification

Custom CSS needed?
  → ASK for approval

When in doubt?
  → ASK, don't assume
```

**Golden Rule:** It's better to ask once than apologize twice.
```

**Estimado Fase 3:** 2 horas

---

### FASE 4: Crear Helpers Modulares (2-3 horas)

#### Tarea 4.1: Procesar HELPERS.md

**Problema:** docs/HELPERS.md está vacío/incompleto

**Solución:** Extraer de docs oficiales web

**Acción:**

1. **Ir a:** https://www.beercss.com/documentation/helpers

2. **Copiar secciones:**
   - Spacing (margin, padding, gap)
   - Colors (full palette)
   - Typography (sizes, weights)
   - Responsive (breakpoints)
   - Elevation (shadows)
   - Shapes (border-radius)
   - Utilities (misc)

3. **Crear archivos modulares:**

```bash
helpers/
├── spacing.md     # margin, padding, gap
├── colors.md      # all color helpers
├── typography.md  # text helpers
├── responsive.md  # s/m/l breakpoints
├── elevation.md   # shadow helpers
├── shapes.md      # border-radius
└── utilities.md   # opacity, cursors, etc.
```

**Contenido ejemplo (spacing.md):**

```markdown
# Spacing Helpers

Source: https://www.beercss.com/documentation/helpers

## Margin

### Sizes
- `no-margin` - Remove all margin
- `tiny-margin` - 0.25rem (4px)
- `small-margin` - 0.5rem (8px)
- `margin` - 1rem (16px) - DEFAULT
- `medium-margin` - 1.5rem (24px)
- `large-margin` - 2rem (32px)

### Directional
- `left-margin`, `right-margin`
- `top-margin`, `bottom-margin`
- `horizontal-margin` - left + right
- `vertical-margin` - top + bottom

### Examples
```html
<div class="medium-margin">Content with 24px margin all sides</div>
<div class="horizontal-margin">Content with margin left/right only</div>
<section class="top-margin bottom-margin">Top and bottom margin</section>
```

## Padding

[Similar structure to Margin]

## Gap (Flexbox/Grid)

- `no-gap` - Remove gap
- `tiny-gap` - 0.25rem
- `small-gap` - 0.5rem
- `gap` - 1rem - DEFAULT
- `medium-gap` - 1.5rem
- `large-gap` - 2rem

### Examples
```html
<div class="grid medium-gap">
  <div class="s12 m6">Column 1</div>
  <div class="s12 m6">Column 2</div>
</div>
```

## Responsive Spacing

Combine with breakpoints:

```html
<!-- Small padding on mobile, large on desktop -->
<div class="small-padding s large-padding l">...</div>

<!-- No margin on mobile, margin on desktop -->
<div class="no-margin s margin l">...</div>
```

## Common Patterns

### Card with Padding
```html
<article class="card padding">
  <h6>Title</h6>
  <p>Content with padding inside card</p>
</article>
```

### Section Spacing
```html
<section class="vertical-margin large-padding">
  Content with vertical margin and large padding
</section>
```

### Grid with Gap
```html
<div class="grid large-gap">
  <div class="s12 m6 l4">...</div>
  <div class="s12 m6 l4">...</div>
  <div class="s12 m6 l4">...</div>
</div>
```
```

**Estimado:** 30 min por archivo × 7 = 3.5 horas

**MVP (solo spacing + colors):** 1 hora

---

### FASE 5: Testing y Refinamiento (2-3 horas)

#### Tarea 5.1: Test Suite

**Crear archivo:** `tests/prompts.md`

```markdown
# Test Prompts for BeerCSS Skill

## Basic Components

### Test 1: Button
```
Prompt: "Create a primary button"
Expected: Uses fill class from buttons.md
Expected Code:
<button class="fill">Primary</button>
```

### Test 2: Input
```
Prompt: "Create a text input with label"
Expected: Uses field pattern from inputs.md
Expected Code:
<div class="field label border">
  <input type="text">
  <label>Label</label>
</div>
```

### Test 3: Card
```
Prompt: "Create a card with padding"
Expected: Uses article card with padding helper
Expected Code:
<article class="card padding">
  <h6>Title</h6>
  <p>Content</p>
</article>
```

## Hallucination Prevention

### Test 4: Fake Component
```
Prompt: "Create a fancy-slider component"
Expected: Asks user (component doesn't exist)
Expected Response: "BeerCSS has a 'slider' component. Did you mean that?"
```

### Test 5: Custom Class
```
Prompt: "Add class='product-card'"
Expected: Warns about custom class
Expected Response: "'product-card' isn't a BeerCSS class. Should I use 'card'?"
```

### Test 6: Custom Color
```
Prompt: "Make the button neon green"
Expected: Checks color-system.md
Expected Response: "Neon green isn't in your theme (styles.css). Should I..."
```

## Complex Layouts

### Test 7: Login Form
```
Prompt: "Create a login form"
Expected: Asks for clarification
Expected Response: "Should I include: username, password, remember me, submit button?"
```

### Test 8: Dashboard
```
Prompt: "Create a dashboard layout"
Expected: Asks for specification
Expected Response: "What sections should the dashboard include?"
```

## Templates

### Test 9: Gmail-like Inbox
```
Prompt: "Create an email inbox like Gmail"
Expected: Uses gmail-inbox.md template
Expected: Checkbox, star button, truncated content, timestamp
```

### Test 10: Video Grid
```
Prompt: "Create a YouTube-style video grid"
Expected: Uses youtube-home.md template
Expected: Responsive grid with cards
```

## Color System

### Test 11: Theme Color
```
Prompt: "Create button with primary color"
Expected: Uses theme primary from color-system.md
Expected Code: <button class="fill">...</button>
```

### Test 12: Non-Theme Color
```
Prompt: "Make text bright red"
Expected: Checks if intentional
Expected Response: "Should I use BeerCSS 'red' helper or error color from theme?"
```

## @ References Loading

### Test 13: Component Reference
```
Prompt: "Show me all button variations"
Expected: Loads @./components/buttons.md
Expected: Shows all styles, sizes, patterns
```

### Test 14: Helper Reference
```
Prompt: "What spacing helpers are available?"
Expected: Loads @./helpers/spacing.md
Expected: Lists margin, padding, gap with sizes
```

## Edge Cases

### Test 15: Ambiguous Request
```
Prompt: "Create a card"
Expected: Provides basic card, mentions variations available
```

### Test 16: Combining Components
```
Prompt: "Create a card with button inside"
Expected: Combines card.md + buttons.md correctly
Expected Code:
<article class="card">
  <div class="padding">
    <h6>Title</h6>
    <button class="fill">Action</button>
  </div>
</article>
```

## Success Criteria

✅ Pass if:
- Uses documented components only
- Asks before hallucinating
- Respects color system
- Loads correct @ references
- Provides clean, working code

❌ Fail if:
- Invents custom classes
- Uses undocumented patterns
- Ignores color-system.md
- Doesn't ask when uncertain
- Generates broken code
```

#### Tarea 5.2: Run Tests

```bash
# Para cada test
gemini

[paste test prompt]

# Verificar:
# 1. Código generado es correcto
# 2. Usa solo clases documentadas
# 3. Respeta color system
# 4. Pregunta cuando debe
# 5. Carga @ references apropiados
```

#### Tarea 5.3: Iterar

**Si test falla:**

1. Identificar causa
2. Actualizar SKILL.md o rules/
3. Re-test
4. Documentar fix

**Estimado:** 2-3 horas

---

### FASE 6: Documentación Final (1 hora)

#### Tarea 6.1: README.md

```markdown
# 🍺 BeerCSS SuperSkill v2.0

Material Design 3 expert for Gemini CLI with hallucination prevention.

## Features

- ✅ **38 Components** - All documented from beercss.com
- ✅ **8 Real Templates** - Gmail, YouTube, Netflix, etc.
- ✅ **Hallucination Prevention** - Only uses documented patterns
- ✅ **Color System Enforcement** - Respects your styles.css theme
- ✅ **@ References** - Progressive loading for efficiency
- ✅ **Decision Protocol** - Asks when uncertain

## Installation

```bash
# Copy to Gemini CLI skills directory
cp -r beercss ~/.gemini/skills/

# Or symlink for development
ln -s /path/to/beercss ~/.gemini/skills/beercss
```

## Quick Start

```bash
gemini

# The skill activates automatically when you work with BeerCSS
"Create a primary button"
"Create a login form with BeerCSS"
"Add a responsive card grid"
```

## Structure

```
beercss/
├── SKILL.md (Orchestrator with @ references)
├── components/ (38 components from docs)
├── helpers/ (Spacing, colors, typography, etc.)
├── templates/ (8 real-world examples)
└── rules/ (Hallucination prevention, color system)
```

## How It Works

### 1. Progressive Loading

SKILL.md uses @ references to load components on-demand:

```markdown
@./components/buttons.md
@./components/cards.md
```

Only loads what's needed for your prompt.

### 2. Hallucination Prevention

Before generating code, checks:
- Component exists in docs?
- Class is documented?
- Pattern matches examples?

If not → Asks you first.

### 3. Color System

Enforces your `styles.css` theme:
- Only uses colors from theme
- Respects light/dark modes
- Asks before adding custom colors

### 4. Decision Protocol

- Simple requests → Proceeds
- Ambiguous → Verifies approach
- Uncertain → Asks for clarification

## Examples

### Creating Components

```
You: "Create a primary button"
Gemini: [Loads @./components/buttons.md]
        <button class="fill">Primary</button>
```

### Hallucination Prevention

```
You: "Create a fancy-card component"
Gemini: "BeerCSS has 'card' component, not 'fancy-card'.
         Did you mean the standard card, or do you need
         custom styling?"
```

### Color System

```
You: "Make button bright red"
Gemini: [Checks @./rules/color-system.md]
        "Your theme uses blue primary. Should I:
         1. Use BeerCSS 'red' helper?
         2. Use theme primary color?
         3. Add custom red to styles.css?"
```

## Configuration

### Customize Color System

Edit `rules/color-system.md` to match your `styles.css`:

```markdown
### Light Mode
--primary: #your-color
--secondary: #your-color

### Dark Mode
--primary: #your-dark-color
```

### Add Custom Rules

Create new files in `rules/`:

```bash
rules/
├── no-hallucination.md
├── color-system.md
├── decision-protocol.md
└── your-custom-rule.md  ← Add here
```

Reference in SKILL.md:

```markdown
@./rules/your-custom-rule.md
```

## Testing

Run test suite:

```bash
# See tests/prompts.md for all tests
gemini < tests/prompts.md
```

## Maintenance

### Update from beercss.com

1. Download latest docs
2. Replace files in `components/`
3. Update version in SKILL.md
4. Run tests

### Add New Component

1. Copy from beercss.com documentation
2. Create `components/new-component.md`
3. Add to component index in SKILL.md
4. Test with prompts

## Troubleshooting

### Skill not activating

Check scope in SKILL.md:
```yaml
scope: [root, src, components, pages, views]
```

Add your project directories if needed.

### Generating wrong code

1. Check component docs are up-to-date
2. Verify @ references are loading
3. Run test suite
4. Check Gemini CLI version

### Hallucination still occurring

1. Strengthen no-hallucination.md
2. Add specific examples of what NOT to do
3. Update decision-protocol.md thresholds

## Version History

### v2.0.0 (Current)
- ✅ Full documentation from beercss.com
- ✅ @ references for progressive loading
- ✅ Hallucination prevention system
- ✅ Color system enforcement
- ✅ Decision protocol
- ✅ 8 real-world templates

### v1.0.0
- ❌ Based on outdated GitHub docs
- ❌ No hallucination prevention
- ❌ No @ references

## Contributing

Improvements welcome! Please:

1. Test changes with test suite
2. Update version history
3. Document breaking changes

## License

[Your license]

## Links

- **BeerCSS**: https://www.beercss.com
- **Gemini CLI**: https://geminicli.com
- **Material Design 3**: https://m3.material.io
```

#### Tarea 6.2: CHANGELOG.md

```markdown
# Changelog

## [2.0.0] - 2026-02-15

### Added
- 38 components from official beercss.com documentation
- @ references for progressive loading
- Hallucination prevention system (no-hallucination.md)
- Color system enforcement (color-system.md)
- Decision protocol (decision-protocol.md)
- 8 real-world templates (Gmail, YouTube, Netflix, etc.)
- Comprehensive test suite
- Modular helpers (spacing, colors, typography, etc.)

### Changed
- Migrated from GitHub docs to web documentation
- SKILL.md now orchestrator with @ references
- Split monolithic docs into modular components
- Updated all examples to latest BeerCSS syntax

### Removed
- Outdated GitHub docs/ references
- Monolithic SKILL.md approach

### Fixed
- Hallucination of custom components
- Inconsistent color usage
- Missing component documentation
- Incorrect class names

## [1.0.0] - 2026-02-11

### Added
- Initial BeerCSS skill
- Basic component documentation
- References structure

### Issues
- Based on outdated GitHub docs
- No hallucination prevention
- Manual component loading
```

**Estimado Fase 6:** 1 hora

---

## 📊 Resumen del Plan v2.0

### Tiempo Total Estimado: 15-20 horas

| Fase | Tareas | Tiempo | Prioridad |
|------|--------|--------|-----------|
| FASE 1: Procesar Docs | 3 tareas | 3-4h | P0 |
| FASE 2: SKILL.md | 5 tareas | 3-4h | P0 |
| FASE 3: Reglas | 3 tareas | 2h | P0 |
| FASE 4: Helpers | 1 tarea | 2-3h | P1 |
| FASE 5: Testing | 3 tareas | 2-3h | P1 |
| FASE 6: Docs | 2 tareas | 1h | P2 |

### MVP (1 Week - 10-12 horas)

**Día 1-2 (4-5 horas):**
- FASE 1: Procesar P0 components (6 componentes)
- FASE 2: SKILL.md básico con @ references

**Día 3-4 (4-5 horas):**
- FASE 3: Crear 3 reglas (no-hallucination, color-system, decision-protocol)
- FASE 4: Helpers básicos (spacing + colors)

**Día 5 (2-3 horas):**
- FASE 5: Testing básico
- Refinamiento

**Resultado:** Skill funcional con hallucination prevention

### Complete (2 Weeks - 20 horas)

**Semana 1:** MVP
**Semana 2:**
- Resto de componentes (P1 + P2)
- Templates
- Testing exhaustivo
- Documentación completa

---

## 🎯 Características Únicas de v2.0

### 1. **@ References (Gemini CLI)**

```markdown
# SKILL.md es ligero (500-700 líneas)
# Carga componentes bajo demanda

@./components/buttons.md  ← Solo cuando se necesitan botones
@./components/cards.md    ← Solo cuando se necesitan cards
```

**Beneficio:** Velocidad + eficiencia

### 2. **Hallucination Prevention**

```
Antes (v1.0):
User: "Create fancy-card"
Gemini: <div class="fancy-card">... ❌ HALLUCINATION

Después (v2.0):
User: "Create fancy-card"
Gemini: "fancy-card doesn't exist in docs. Did you mean 'card'?" ✅
```

### 3. **Color System Enforcement**

```
Antes (v1.0):
User: "Make it red"
Gemini: style="background: red" ❌ Random color

Después (v2.0):
Gemini: [Checks color-system.md]
        "Should I use: 1) BeerCSS red, 2) theme primary, 3) add to styles.css?"
```

### 4. **Decision Protocol**

```
Simple request    → Proceed
Medium complexity → Verify approach
High complexity   → Ask for spec
Uncertain         → Always ask
```

### 5. **Real Templates**

```
templates/
├── gmail-inbox.md (email list pattern)
├── youtube-home.md (video grid)
├── netflix-browse.md (media cards)
└── [...]

User: "Create Gmail-like inbox"
Gemini: [Loads @./templates/gmail-inbox.md]
        [Generates exact pattern]
```

---

## 🚀 Ventajas vs v1.0

| Aspecto | v1.0 | v2.0 |
|---------|------|------|
| **Docs Source** | GitHub (outdated) | beercss.com (current) |
| **Loading** | All at once | Progressive (@ refs) |
| **Hallucination** | Frequent | Prevented |
| **Color System** | Ignored | Enforced |
| **Decision Making** | Random | Protocol-based |
| **Templates** | None | 8 real examples |
| **File Size** | 731 lines mono | 500 lines + modules |
| **Maintenance** | Hard (monolithic) | Easy (modular) |

---

## 📐 Estructura Final Completa

```
~/.gemini/skills/beercss/
│
├── SKILL.md (500-700 líneas - Orchestrator)
│   ├── Metadata with imports
│   ├── Critical Rules with @ refs
│   ├── Decision Trees with @ refs
│   ├── Quick Reference
│   └── Component Index with @ refs
│
├── components/ (38 archivos)
│   ├── buttons.md (1,381 líneas procesadas)
│   ├── cards.md (573 líneas procesadas)
│   ├── badges.md (448 líneas procesadas)
│   ├── toolbars.md (450 líneas procesadas)
│   ├── app-bars.md (360 líneas procesadas)
│   ├── tables.md (345 líneas procesadas)
│   ├── navigations.md (313 líneas procesadas)
│   ├── layouts.md (260 líneas procesadas)
│   └── [...30 more components]
│
├── helpers/ (7 archivos)
│   ├── spacing.md (margin, padding, gap)
│   ├── colors.md (full palette + theme)
│   ├── typography.md (text helpers)
│   ├── responsive.md (breakpoints)
│   ├── elevation.md (shadows)
│   ├── shapes.md (border-radius)
│   └── utilities.md (misc)
│
├── templates/ (8 archivos)
│   ├── gmail-inbox.md
│   ├── youtube-home.md
│   ├── netflix-browse.md
│   ├── reddit-feed.md
│   ├── uber-ride.md
│   ├── music-player.md
│   ├── material-design-3.md
│   └── dynamic-colors.md
│
├── rules/ (3 archivos críticos)
│   ├── no-hallucination.md (verification protocol)
│   ├── color-system.md (enforce styles.css)
│   └── decision-protocol.md (when to ask)
│
├── tests/
│   └── prompts.md (16 test cases)
│
└── docs/ (meta)
    ├── README.md (usage guide)
    ├── CHANGELOG.md (version history)
    └── CONTRIBUTING.md (how to improve)

Total Files: ~60
Total Lines: ~10,000
But loaded progressively via @ references
```

---

## ✅ Checklist Final

### Setup Inicial
- [ ] Crear estructura de directorios
- [ ] Copiar docs actualizados
- [ ] Tener styles.css listo

### Fase 1 (MVP)
- [ ] Procesar 6 componentes P0
- [ ] Crear SKILL.md con @ references
- [ ] Crear 3 reglas críticas
- [ ] Crear helpers básicos (spacing + colors)

### Fase 2 (Complete)
- [ ] Procesar resto de componentes
- [ ] Procesar templates
- [ ] Testing exhaustivo
- [ ] Documentación completa

### Validación
- [ ] Test suite passes
- [ ] No hallucinations
- [ ] Respeta color system
- [ ] @ references cargan correctamente
- [ ] Gemini CLI activa skill automáticamente

---

## 🎓 Próximo Paso Inmediato

```bash
# 1. Crear estructura base
mkdir -p ~/.gemini/skills/beercss/{components,helpers,templates,rules,tests,docs}

# 2. Copiar docs actualizados
cp /path/to/beercss/docs/*.md ~/.gemini/skills/beercss/components/

# 3. Crear archivos de reglas
touch ~/.gemini/skills/beercss/rules/{no-hallucination,color-system,decision-protocol}.md

# 4. Empezar con SKILL.md
nano ~/.gemini/skills/beercss/SKILL.md
```

**Primera tarea:** Crear `rules/no-hallucination.md` usando el template que te di arriba.

---

**¿Listo para empezar? ¿Quieres que te ayude con alguna fase específica primero?** 🍺

Puedo ayudarte a:
1. Procesar los primeros 6 componentes P0
2. Crear los 3 archivos de reglas
3. Crear el SKILL.md con @ references
4. Lo que necesites!
