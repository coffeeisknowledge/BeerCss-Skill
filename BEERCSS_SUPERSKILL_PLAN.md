# 🍺 BeerCSS SuperSkill - Plan Maestro de Desarrollo

**Ingeniero Senior a Cargo:** Claude  
**Developer:** Tu  
**Objetivo:** Crear una super skill robusta que convierta a Gemini CLI en un experto en BeerCSS

---

## 📊 Análisis de la Documentación

### Estructura de BeerCSS (lo que descubrí)

```
BeerCSS Philosophy: "Beer Purity Law" - 3 ingredientes
├── SETTINGS (Temas, colores, configuración global)
├── ELEMENTS (28 componentes - Badge, Button, Card, etc.)
└── HELPERS (Utilities - margins, padding, colors, responsive, etc.)

Total: 38 archivos MD, ~4000 líneas de documentación
```

### Categorías Identificadas

1. **Core Concepts** (3 archivos)
   - INDEX.md (263 líneas) - Filosofía, setup, DO/DON'T
   - ELEMENTS.md (135 líneas) - Catálogo de componentes
   - HELPERS.md (144 líneas) - Utilities system

2. **Form Controls** (8 componentes)
   - INPUT, TEXTAREA, SELECT, CHECKBOX, RADIO, SWITCH, SLIDER

3. **Navigation & Layout** (7 componentes)
   - NAVIGATION, MENU, TABS, LAYOUT, MAIN_LAYOUT, PAGE, CONTAINER

4. **Content Display** (8 componentes)
   - CARD, LIST, TABLE, MEDIA, TYPOGRAPHY, ICON, GRID

5. **Feedback & Actions** (8 componentes)
   - BUTTON, DIALOG, SNACKBAR, TOOLTIP, PROGRESS, OVERLAY, BADGE, CHIP

6. **Utilities & Config** (4 archivos)
   - SETTINGS, JAVASCRIPT, SUMMARY, SHAPE, DIVIDER, EXPANSION

---

## 🎯 Decisión Arquitectónica: UNA SuperSkill Modular

### ✅ Opción Elegida: Una SuperSkill con Módulos

**Estructura:**
```
beercss/                           # Skill principal
├── SKILL.md                       # Orquestador maestro (3000-4000 líneas)
├── assets/
│   ├── setup_patterns.html        # Setup completo
│   ├── form_controls_examples.html
│   ├── navigation_examples.html
│   ├── content_display_examples.html
│   └── feedback_examples.html
└── references/
    ├── file-locations.md
    ├── components/                # Módulo de componentes
    │   ├── form-controls.md       # Todos los forms
    │   ├── navigation.md          # Nav, Menu, Tabs
    │   ├── content-display.md     # Card, List, Table
    │   └── feedback-actions.md    # Dialogs, Snackbar, etc.
    ├── helpers-guide.md           # Guía completa de helpers
    ├── settings-themes.md         # Temas y configuración
    └── best-practices.md          # DO/DON'T + patterns
```

### ❌ Por qué NO 28 skills separadas

1. **Fragmentación:** Usuario tendría que saber qué skill activar
2. **Redundancia:** Helpers y Settings se repiten en cada skill
3. **Mantenimiento:** Actualizar 28 skills vs 1
4. **Contexto perdido:** Material Design funciona como sistema, no piezas aisladas
5. **Confusión de activación:** ¿Qué skill para un botón con badge y tooltip?

### ✅ Por qué SÍ una skill modular

1. **Progressive Disclosure:** SKILL.md carga lo básico, referencias bajo demanda
2. **Sistema cohesivo:** BeerCSS es un sistema, la skill refleja eso
3. **Decision Trees:** "¿Qué componente usar?" en un solo lugar
4. **Helpers unificados:** margin, padding, colors aplicables a TODO
5. **Fácil de mantener:** Un solo punto de verdad
6. **Gemini entenderá el contexto completo:** Material Design como sistema

---

## 📋 Plan de Trabajo (5 Fases)

### FASE 1: Preparación y Estructura Base (2-3 horas)

#### Tarea 1.1: Crear Estructura de Directorios
```bash
mkdir -p ~/.gemini/skills/beercss/{assets,references/components}
cd ~/.gemini/skills/beercss
```

**Deliverable:**
```
beercss/
├── SKILL.md (vacío, listo para llenar)
├── assets/
└── references/
    └── components/
```

#### Tarea 1.2: Analizar y Categorizar Componentes

**Input:** Todos los .md de docs/
**Output:** Spreadsheet o documento con:

| Component | Category | Complexity | Priority | Dependencies |
|-----------|----------|------------|----------|--------------|
| Button | Feedback | Low | High | None |
| Dialog | Feedback | Medium | High | Overlay |
| Navigation | Navigation | High | High | Layout |
| ... | ... | ... | ... | ... |

**Prioridades:**
- **P0 (Must have):** Button, Input, Card, Grid, Navigation (básicos)
- **P1 (Important):** Dialog, Menu, Tabs, List, Table
- **P2 (Nice to have):** Badge, Chip, Tooltip, Progress
- **P3 (Advanced):** Expansion, Overlay, Page, Shape

#### Tarea 1.3: Identificar Patrones Comunes

**Output:** Documento listando:
- Patrones de clase común: `.class helper helper`
- Convenciones de naming
- Estructura HTML típica
- JavaScript patterns (si aplica)
- DO/DON'T patterns

---

### FASE 2: SKILL.md - Sección Core (4-6 horas)

#### Tarea 2.1: Metadata y Setup

```yaml
---
name: beercss
description: >
  BeerCSS Material Design implementation: components, helpers, responsive layouts.
  Trigger: When creating UI with BeerCSS, Material Design components, or responsive layouts.
version: "1.0.0"
scope: [root, src, components, pages, views, public, static]
auto_invoke: "Creating BeerCSS components or Material Design UI"
---
```

**Estimado:** 30 min

#### Tarea 2.2: When to Use + Critical Rules

**Contenido:**
```markdown
## When to Use

Use this skill for:
- Material Design 3 implementations with BeerCSS
- Responsive layouts following Material guidelines
- Form controls with Material styling
- Navigation patterns (rail, bar, drawer)
- Component composition with helpers

For pure CSS frameworks without Material Design, use `tailwind` or `bootstrap` skills.

## Critical Rules

### ✅ ALWAYS Rules
- ALWAYS use ONE element class per tag (no multiple elements)
- ALWAYS combine elements with helpers: `<div class="element helper helper">`
- ALWAYS include beer.min.css before custom CSS
- ALWAYS use Material Icons with `<i>` tags
- ALWAYS apply theme class to `<body>`: `class="dark"` or `class="light"`
- ALWAYS use responsive helpers for mobile-first design
- ALWAYS follow the 1 main element per document rule

### ❌ NEVER Rules
- NEVER use multiple element classes on same tag: `class="card button"`
- NEVER create element dependencies (e.g., .card-header, .card-body)
- NEVER nest block elements in inline elements
- NEVER write CSS selectors like `.element .helper` (use `.element > .helper`)
- NEVER use more than one `<main>` per document
- NEVER forget to include material-dynamic-colors.min.js for theming

> **Note**: BeerCSS follows "Beer Purity Law" - 3 ingredients only: Settings, Elements, Helpers
```

**Estimado:** 1.5 horas

#### Tarea 2.3: Architecture Overview

**Contenido:**
- 3-ingredient philosophy diagram
- Element + Helper composition model
- Theme system (light/dark)
- Responsive breakpoints
- File structure recommendations

**Estimado:** 1 hour

#### Tarea 2.4: Decision Trees (Crítico)

**Contenido:**
```markdown
## Decision Trees

### Which Component for User Input?

```
Single-line text        → Input (with label, icon)
Multi-line text         → Textarea
Pick from list          → Select
Yes/No toggle           → Switch
Multiple options        → Checkbox
Single option from set  → Radio
Range selection         → Slider
```

### Which Navigation Pattern?

```
Desktop + always visible       → Navigation Rail (left)
Mobile + bottom                → Navigation Bar (bottom)
Temporary menu                 → Menu (dropdown)
Switch between views           → Tabs
Hierarchical menu              → Expansion panels
```

### Which Layout Container?

```
Main content area              → Container
Full-width sections            → Page
Responsive grid                → Grid (s12 m6 l4 pattern)
Absolute positioning           → Layout (left, right, top, bottom)
Card-based content             → Card
```

### Which Feedback Component?

```
User action needed             → Dialog
Brief notification             → Snackbar (top/bottom)
Contextual info on hover       → Tooltip
Loading state                  → Progress (circular/linear)
Blocking wait                  → Overlay + Progress
Emphasize element              → Badge
Compact tag/filter             → Chip
```

### Which Helper for Spacing?

```
External space                 → margin (tiny, small, medium, large)
Internal space                 → padding (tiny, small, medium, large)
Responsive spacing             → Use with breakpoints (s, m, l)
Remove default spacing         → no-margin, no-padding
```
```

**Estimado:** 2 hours

#### Tarea 2.5: Setup and Installation Patterns

**Contenido:**
- CDN setup (default, scoped, custom element)
- NPM installation
- HTML boilerplate
- Vite configuration
- Theme setup

**Estimado:** 1 hour

---

### FASE 3: Code Patterns - Components (6-8 horas)

#### Tarea 3.1: Form Controls Patterns

**Para cada componente (Input, Textarea, Select, Checkbox, Radio, Switch, Slider):**

```markdown
## Input Pattern

### Basic Input (Filled)

```html
<div class="field label border">
  <input type="text" id="username">
  <label for="username">Username</label>
</div>
```

**Variations:**
- Filled: `class="field label border"`
- Outlined: `class="field label outline"`
- With prefix icon: Add `<i>person</i>` before input
- With suffix icon: Add `<i>visibility</i>` after input
- Invalid state: Add `class="invalid"` to field
- Helper text: Add `<span class="helper">Helper text</span>`

### Input with Icon

```html
<div class="field label prefix border">
  <i>search</i>
  <input type="text" id="search">
  <label for="search">Search</label>
</div>
```

### Input States

```html
<!-- Disabled -->
<div class="field label border">
  <input type="text" disabled>
  <label>Disabled</label>
</div>

<!-- Invalid -->
<div class="field label border invalid">
  <input type="text">
  <label>Error</label>
  <span class="helper error">This field is required</span>
</div>

<!-- Success -->
<div class="field label border">
  <input type="text">
  <label>Valid</label>
  <span class="helper">Looks good!</span>
</div>
```

**Key Points:**
- Always wrap input in `div class="field"`
- Label goes AFTER input for proper styling
- Use `for` attribute linking label to input id
- Icons use Material Icons font
- Helper text with `span class="helper"`
```

**Estimado por componente:** 30-45 min  
**Total:** 3-4 hours para 8 form controls

#### Tarea 3.2: Navigation Patterns

**Componentes:** Navigation, Menu, Tabs

```markdown
## Navigation Rail Pattern (Desktop Sidebar)

### Basic Left Navigation

```html
<nav class="left max l">
  <header>
    <img src="logo.png" class="circle">
    <h6>App Name</h6>
  </header>
  
  <a class="active">
    <i>home</i>
    <span>Home</span>
  </a>
  
  <a>
    <i>search</i>
    <span>Search</span>
  </a>
  
  <div class="divider"></div>
  
  <a>
    <i>settings</i>
    <span>Settings</span>
  </a>
</nav>
```

**Variations:**
- Left rail: `class="left"`
- Right rail: `class="right"`
- With labels: Include `<span>` text
- Icon-only (collapsed): Remove `<span>` or use `class="m"` for medium
- Responsive: `class="left max l"` (max width on large screens)

### Bottom Navigation Bar (Mobile)

```html
<nav class="bottom s">
  <a class="active">
    <i>home</i>
    <span>Home</span>
  </a>
  <a>
    <i>search</i>
    <span>Search</span>
  </a>
  <a>
    <i>notifications</i>
    <span>Alerts</span>
  </a>
  <a>
    <i>person</i>
    <span>Profile</span>
  </a>
</nav>
```

**Key Points:**
- `class="s"` shows only on small screens
- `class="m"` shows only on medium screens  
- `class="l"` shows only on large screens
- Active state: `class="active"` on `<a>`
- Can include badge: `<i>notifications<sup>3</sup></i>`
```

**Estimado:** 2 hours

#### Tarea 3.3: Content Display Patterns

**Componentes:** Card, List, Table, Grid

```markdown
## Card Pattern

### Basic Card

```html
<article class="card">
  <img src="image.jpg" class="responsive">
  <div class="padding">
    <h6>Card Title</h6>
    <p>Card description text goes here. Can be multiple lines.</p>
    <nav class="right-align">
      <button>Cancel</button>
      <button class="fill">Action</button>
    </nav>
  </div>
</article>
```

**Variations:**
- With elevation: Add `class="elevate"`
- With border: Add `class="border"`
- Full-width image: Use `class="responsive"` on img
- Fixed height: Add `class="medium-height"` to card
- Rounded corners: Add `class="round"` to card

### Card with Actions

```html
<article class="card">
  <div class="padding">
    <h6>Title</h6>
    <p>Content</p>
  </div>
  <nav class="right-align">
    <button class="border">Learn More</button>
    <button class="fill">Get Started</button>
  </nav>
</article>
```

## Grid Pattern

### Responsive Grid

```html
<div class="grid">
  <div class="s12 m6 l4">
    <article class="card">Column 1</article>
  </div>
  <div class="s12 m6 l4">
    <article class="card">Column 2</article>
  </div>
  <div class="s12 m6 l4">
    <article class="card">Column 3</article>
  </div>
</div>
```

**Grid Classes:**
- Small (mobile): `s1` to `s12`
- Medium (tablet): `m1` to `m12`
- Large (desktop): `l1` to `l12`
- Total columns: Always add up to 12

**Common Patterns:**
```
Full width all screens:    s12
Half on mobile, full rest: s12 m6
Thirds on desktop:         s12 m6 l4
Quarters on desktop:       s12 m6 l3
```
```

**Estimado:** 2 hours

#### Tarea 3.4: Feedback & Actions Patterns

**Componentes:** Button, Dialog, Snackbar, Tooltip, Progress

```markdown
## Button Pattern

### Button Variants

```html
<!-- Filled (primary) -->
<button class="fill">Primary</button>

<!-- Outlined -->
<button class="border">Secondary</button>

<!-- Text (tertiary) -->
<button>Tertiary</button>

<!-- With icon -->
<button class="fill">
  <i>send</i>
  <span>Send</span>
</button>

<!-- Icon only -->
<button class="circle">
  <i>favorite</i>
</button>

<!-- FAB (Floating Action Button) -->
<button class="circle extra large-elevate fixed bottom right">
  <i>add</i>
</button>
```

**Sizes:**
- Default: No class needed
- Small: `class="small"`
- Large: `class="large"`
- Extra: `class="extra"`

**States:**
- Disabled: `disabled` attribute
- Loading: Add progress inside button

## Dialog Pattern

### Basic Dialog

```html
<dialog class="modal">
  <h5>Dialog Title</h5>
  <div>Dialog content goes here.</div>
  <nav class="right-align">
    <button class="border" onclick="ui('dialog-id')">Cancel</button>
    <button class="fill" onclick="ui('dialog-id')">Confirm</button>
  </nav>
</dialog>
```

**Show/Hide:**
```html
<!-- Trigger -->
<button onclick="ui('dialog-id')">Open Dialog</button>

<!-- Dialog with id -->
<dialog id="dialog-id">...</dialog>
```

**Variations:**
- Modal (blocks background): `class="modal"`
- Right side: `class="right"`
- Left side: `class="left"`
- Bottom sheet: `class="bottom"`
- Fullscreen: `class="fill"`

## Snackbar Pattern

```html
<div class="snackbar bottom">
  <i>check_circle</i>
  <span>Action completed successfully</span>
  <button class="transparent circle" onclick="ui('snackbar-id')">
    <i>close</i>
  </button>
</div>
```

**Show snackbar:**
```javascript
ui('#snackbar-id');
```

**Positions:**
- Bottom: `class="snackbar bottom"`
- Top: `class="snackbar top"`

## Progress Pattern

### Linear Progress

```html
<!-- Indeterminate -->
<progress class="linear"></progress>

<!-- Determinate -->
<progress class="linear" value="75" max="100"></progress>
```

### Circular Progress

```html
<!-- Indeterminate -->
<progress class="circle"></progress>

<!-- Determinate -->
<progress class="circle" value="75" max="100"></progress>
```
```

**Estimado:** 2 hours

---

### FASE 4: Referencias Modulares (4-6 horas)

#### Tarea 4.1: references/components/*.md

Crear 4 archivos de referencia detallados:

**1. form-controls.md** (extraer de 8 archivos .md)
- Input, Textarea, Select
- Checkbox, Radio, Switch, Slider
- Todos los patrones, variaciones, estados

**2. navigation.md** (extraer de 4 archivos .md)
- Navigation (rail, bar)
- Menu, Tabs
- Layout patterns

**3. content-display.md** (extraer de 8 archivos .md)
- Card, List, Table
- Grid, Media, Typography, Icon

**4. feedback-actions.md** (extraer de 8 archivos .md)
- Button, Dialog, Snackbar
- Tooltip, Progress, Overlay, Badge, Chip

**Formato de cada archivo:**
```markdown
# [Category Name]

## Component Name

### Purpose
[When to use]

### Basic Pattern
[Code example]

### Variations
[All variations with code]

### States
[States and their code]

### Accessibility
[A11y considerations]

### Common Pitfalls
[DO/DON'T]

---

[Repeat for each component]
```

**Estimado:** 1 hour per file = 4 hours

#### Tarea 4.2: helpers-guide.md

**Contenido completo de HELPERS.md organizado:**

```markdown
# BeerCSS Helpers Guide

Complete reference for all utility classes.

## Philosophy

Helpers make elements scalable and customizable. Apply multiple helpers to one element:
```html
<div class="element helper1 helper2 helper3">...</div>
```

## Spacing System

### Margins
[Lista completa con ejemplos]

### Paddings
[Lista completa con ejemplos]

### Responsive Spacing
[Combinaciones con breakpoints]

## Color System

### Background Colors
[Todos los colores con tonos 1-10]

### Text Colors
[*-text classes]

### Border Colors
[*-border classes]

## Layout Helpers

### Alignment
[left-align, center-align, etc.]

### Positioning
[left, right, center, top, bottom, middle]

### Responsive Display
[s, m, l classes]

## Visual Helpers

### Elevation
[elevate, small-elevate, etc.]

### Shapes
[circle, square, round, etc.]

### Opacity
[opacity, small-opacity, etc.]

## Responsive Breakpoints

| Breakpoint | Screen Size | Class Prefix |
|------------|-------------|--------------|
| Small | 0-600px | s |
| Medium | 601-1240px | m |
| Large | 1241px+ | l |

### Examples
```html
<!-- Show only on small screens -->
<div class="s">Mobile only</div>

<!-- Hide on small screens -->
<div class="m l">Tablet and desktop</div>

<!-- Different grid on each breakpoint -->
<div class="s12 m6 l4">Responsive column</div>
```
```

**Estimado:** 2 hours

#### Tarea 4.3: settings-themes.md

**Contenido de SETTINGS.md + theme customization:**

```markdown
# Settings & Theming

## Theme Setup

### Light/Dark Mode

```html
<!-- Light theme -->
<body class="light">...</body>

<!-- Dark theme -->
<body class="dark">...</body>
```

### Dynamic Theme Switching

```javascript
// Toggle theme
document.body.classList.toggle('dark');
document.body.classList.toggle('light');
```

## Color Customization

[Extract from SETTINGS.md]

## Typography Settings

[Typography configuration]

## Custom CSS Variables

[List of all CSS variables for customization]
```

**Estimado:** 1.5 hours

#### Tarea 4.4: best-practices.md

```markdown
# BeerCSS Best Practices

## DO ✅

### 1. Single Element per Tag
```html
✅ GOOD
<div class="card elevate round">...</div>

❌ BAD
<div class="card button">...</div>
```

### 2. Element + Helpers Pattern
```html
✅ GOOD
<button class="fill circle large">...</button>

❌ BAD  
<button class="button fill">...</button>
```

### 3. Proper Nesting
```html
✅ GOOD
<div class="card">
  <div class="padding">...</div>
</div>

❌ BAD
<div class="card">
  <div class="card-body">...</div>
</div>
```

## DON'T ❌

[All the DON'T patterns from INDEX.md]

## Common Patterns

### Responsive Layout
[Examples]

### Form Validation
[Examples]

### Modal Dialogs
[Examples]

## Performance Tips

1. Use CDN for faster loading
2. For Vite: Set `assetsInlineLimit: 0`
3. Minimize custom CSS - use helpers first
4. Use scoped version if needed

## Accessibility

- Always use label with form controls
- Provide alt text for images
- Use semantic HTML
- Test keyboard navigation
- Include ARIA labels where needed
```

**Estimado:** 1.5 hours

---

### FASE 5: Assets y Finalización (3-4 horas)

#### Tarea 5.1: assets/setup_patterns.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>BeerCSS Setup Examples</title>
  <link href="https://cdn.jsdelivr.net/npm/beercss@4.0.2/dist/cdn/beer.min.css" rel="stylesheet">
  <script type="module" src="https://cdn.jsdelivr.net/npm/beercss@4.0.2/dist/cdn/beer.min.js"></script>
  <script type="module" src="https://cdn.jsdelivr.net/npm/material-dynamic-colors@1.1.4/dist/cdn/material-dynamic-colors.min.js"></script>
</head>
<body class="dark">

<!-- EXAMPLE 1: Basic Setup -->
<section class="padding">
  <h3>1. Basic Page Structure</h3>
  [Complete example]
</section>

<!-- EXAMPLE 2: With Navigation -->
[...]

<!-- EXAMPLE 3: Form Layout -->
[...]

<!-- EXAMPLE 4: Responsive Grid -->
[...]

</body>
</html>
```

**Estimado:** 1.5 hours

#### Tarea 5.2: assets/*.html (otros ejemplos)

Crear archivos HTML con ejemplos ejecutables de:
- form_controls_examples.html
- navigation_examples.html
- content_display_examples.html
- feedback_examples.html

**Estimado:** 1.5 hours

#### Tarea 5.3: Revisión Final y Testing

**Checklist:**
- [ ] Todos los placeholders reemplazados
- [ ] Code examples son válidos HTML
- [ ] Referencias cruzadas funcionan
- [ ] Triggers apropiados en metadata
- [ ] Scope cubre todos los directorios comunes
- [ ] Decision trees son completos
- [ ] Assets son ejecutables
- [ ] Referencias no tienen enlaces rotos

**Testing:**
```bash
cd ~/.gemini/skills/beercss
gemini

# Test prompts:
"Create a navigation rail with BeerCSS"
"Build a form with BeerCSS inputs"
"Create a card grid with BeerCSS"
"Add a dialog to my BeerCSS app"
```

**Estimado:** 1 hour

---

## 📊 Resumen del Plan

### Tiempo Total Estimado: 19-27 horas

| Fase | Tareas | Tiempo | Prioridad |
|------|--------|--------|-----------|
| FASE 1: Preparación | 3 tareas | 2-3h | P0 |
| FASE 2: SKILL.md Core | 5 tareas | 4-6h | P0 |
| FASE 3: Code Patterns | 4 tareas | 6-8h | P0 |
| FASE 4: Referencias | 4 tareas | 4-6h | P1 |
| FASE 5: Assets | 3 tareas | 3-4h | P1 |

### Approach Recomendado

**Semana 1 (MVP - 10-12 horas):**
- FASE 1 completa
- FASE 2 completa
- FASE 3: Solo P0 components (Button, Input, Card, Grid, Navigation)
- Testing básico

**Semana 2 (Complete - 9-15 horas):**
- FASE 3: Completar P1 y P2 components
- FASE 4 completa
- FASE 5 completa
- Testing exhaustivo

---

## 🎯 Entregables por Fase

### FASE 1 ✅
- [ ] Estructura de directorios creada
- [ ] Componentes categorizados (spreadsheet)
- [ ] Patrones comunes identificados

### FASE 2 ✅
- [ ] Metadata completo
- [ ] When to Use + Critical Rules
- [ ] Architecture Overview
- [ ] Decision Trees (5+ trees)
- [ ] Setup patterns

### FASE 3 ✅
- [ ] 8 Form controls con ejemplos
- [ ] 3 Navigation patterns con ejemplos
- [ ] 4 Content display patterns con ejemplos
- [ ] 5 Feedback patterns con ejemplos

### FASE 4 ✅
- [ ] 4 archivos de referencias detallados
- [ ] helpers-guide.md completo
- [ ] settings-themes.md completo
- [ ] best-practices.md completo

### FASE 5 ✅
- [ ] setup_patterns.html funcional
- [ ] 4 archivos de ejemplos HTML
- [ ] Testing completo
- [ ] Documentación de uso

---

## 📐 Estructura Final de la Skill

```
beercss/
├── SKILL.md (3500-4500 líneas)
│   ├── Metadata
│   ├── When to Use
│   ├── Critical Rules (ALWAYS/NEVER)
│   ├── Architecture Overview
│   ├── Decision Trees (5-7 trees)
│   ├── Setup & Installation
│   ├── Form Controls Patterns (8 components)
│   ├── Navigation Patterns (3 components)
│   ├── Content Display Patterns (4 components)
│   ├── Feedback Patterns (5 components)
│   ├── Helper System Overview
│   ├── Theming & Settings
│   ├── Common Pitfalls
│   ├── Production Checklist
│   └── Resources
│
├── assets/ (2000-3000 líneas HTML)
│   ├── setup_patterns.html
│   ├── form_controls_examples.html
│   ├── navigation_examples.html
│   ├── content_display_examples.html
│   └── feedback_examples.html
│
└── references/ (3000-4000 líneas)
    ├── components/
    │   ├── form-controls.md (800-1000 líneas)
    │   ├── navigation.md (600-800 líneas)
    │   ├── content-display.md (800-1000 líneas)
    │   └── feedback-actions.md (800-1000 líneas)
    ├── helpers-guide.md (600-800 líneas)
    ├── settings-themes.md (400-600 líneas)
    ├── best-practices.md (400-600 líneas)
    └── file-locations.md (200-300 líneas)

TOTAL: ~9,000-12,000 líneas
```

---

## 🎓 Consejos del Ingeniero Senior

### 1. **Empieza por Decision Trees**

Los decision trees son lo MÁS IMPORTANTE. Si Gemini sabe cuándo usar qué componente, todo lo demás fluye naturalmente.

**Invierte tiempo aquí primero:**
- Which component for X?
- Which helper for Y?
- Which pattern for Z?

### 2. **Progressive Disclosure es Clave**

No metas TODO en SKILL.md. La estructura debe ser:

```
SKILL.md → Overview + Patterns comunes (70% de uso)
           ↓
references/ → Deep dive en cada categoría (30% de uso)
           ↓
assets/ → Ejemplos ejecutables (cuando necesitas copiar/pegar)
```

### 3. **Prioriza P0 Components Primero**

MVP viable con:
- Button, Input, Card, Grid, Navigation
- Helpers básicos (margin, padding, colors)
- Light/Dark theme

Esto ya te da 80% de valor.

### 4. **Code Debe Ser Copy-Paste Ready**

```html
<!-- ✅ GOOD - Completo y funcional -->
<div class="field label border">
  <input type="text" id="username">
  <label for="username">Username</label>
</div>

<!-- ❌ BAD - Incompleto -->
<div class="field">
  <input>
  ...
</div>
```

### 5. **Testea con Prompts Reales**

Después de cada fase, testea con Gemini:
```
"Create a login form with BeerCSS"
"Build a dashboard with navigation and cards"
"Add a snackbar notification"
```

Si Gemini no genera código correcto, tu skill necesita más ejemplos.

### 6. **Documenta DO/DON'T Exhaustivamente**

BeerCSS tiene reglas específicas (no multiple elements, etc.). Documenta CADA regla con ejemplo visual:

```markdown
❌ BAD
<div class="card button">...</div>

✅ GOOD
<div class="card">...</div>
```

### 7. **Mantén Consistencia con Material Design**

BeerCSS sigue Material Design 3. Tus decision trees y ejemplos deben reflejar esa filosofía:
- Mobile-first
- Elevation system
- Color theming
- Responsive breakpoints

---

## 🚀 Siguiente Paso Inmediato

### Acción 1: Crear Estructura Base

```bash
# En tu terminal
mkdir -p ~/.gemini/skills/beercss/{assets,references/components}
cd ~/.gemini/skills/beercss

# Crear archivos vacíos
touch SKILL.md
touch assets/{setup_patterns,form_controls_examples,navigation_examples,content_display_examples,feedback_examples}.html
touch references/{helpers-guide,settings-themes,best-practices,file-locations}.md
touch references/components/{form-controls,navigation,content-display,feedback-actions}.md
```

### Acción 2: Copiar Template Base

```bash
# Copiar el template del kit
cp ~/superskill-creator-kit/skill-template/SKILL.md ~/.gemini/skills/beercss/SKILL.md
```

### Acción 3: Empezar con Metadata

Abre `SKILL.md` y empieza llenando:
1. Metadata (name, description, etc.)
2. When to Use
3. Critical Rules

---

## 📞 Checkpoint System

Después de cada fase, reporta:

1. **¿Qué completaste?**
2. **¿Qué fue difícil?**
3. **¿Qué dudas tienes?**
4. **¿Necesitas ajustar el plan?**

**Yo te ayudaré con:**
- Revisar tu trabajo
- Ajustar decision trees
- Mejorar examples
- Optimizar la estructura

---

## 🎯 Objetivo Final

Al terminar, tendrás una super skill que:

✅ Gemini CLI activa automáticamente al trabajar con BeerCSS  
✅ Genera código Material Design perfecto  
✅ Conoce todos los 28 componentes  
✅ Usa helpers correctamente  
✅ Sigue las reglas DO/DON'T  
✅ Implementa responsive design  
✅ Maneja temas light/dark  
✅ Es más experto en BeerCSS que tú mismo  

---

**¿Listo para empezar? Comencemos por FASE 1! 🍺**

¿Qué fase quieres atacar primero? ¿Necesitas que te ayude con alguna tarea específica?
