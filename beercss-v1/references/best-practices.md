# BeerCSS Best Practices & Guidelines

## Core Principles

### 1. The Beer Purity Law
Strictly follow the 3 ingredients: **Settings**, **Elements**, and **Helpers**. 
- Never mix two element classes on the same tag.
- Always scale elements using helpers.

### 2. Mobile-First Responsiveness
Always design for small screens (`s`) first, then layer on complexity for medium (`m`) and large (`l`) screens using responsive helpers.

---

## Technical Standards

### Compliance Checklist ✅
- [ ] Theme class applied to `<body>`.
- [ ] Only one `<main>` element in the document.
- [ ] Form controls wrapped in `div class="field"`.
- [ ] Labels placed AFTER inputs for proper Material Design floating effect.
- [ ] Semantic HTML tags used correctly (`article`, `nav`, `header`, `footer`).

### Anti-Patterns to Avoid ❌
- **No BEM:** Don't use `.card-title` or `.button-large`. Use BeerCSS hierarchy and helpers.
- **No Multiple Elements:** Don't use `class="card button"`.
- **No Nesting Violations:** Don't put block elements inside `<span>` or other inline elements.
- **No Guessing:** Don't assume a class exists if it's not in the documentation.

---

## Performance Optimization

1. **Use the CDN:** For fastest loading and automatic updates.
2. **Vite Build:** Set `assetsInlineLimit: 0` to prevent CSS size issues.
3. **Minimize Custom CSS:** Use helpers for 90% of your styling needs. Only write custom CSS for layout-specific needs that helpers can't cover.
4. **Subset Icons:** If weight is critical, use the `Material Symbols Subset` icon font.

---

## Accessibility (A11y)

- **Labels:** Every input, textarea, and select MUST have a label.
- **Alt Text:** Provide descriptive `alt` attributes for all images.
- **Contrast:** Stick to semantic themes (`primary`, `error`) to ensure Material Design compliant color contrast.
- **Keyboard Navigation:** BeerCSS components are designed to be keyboard-friendly; don't break this behavior with custom JS that stops event propagation unnecessarily.