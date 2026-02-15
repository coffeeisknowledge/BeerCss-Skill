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

### High Confidence (90-100%)

- Component in @./components/
- Exact pattern in examples
- Standard BeerCSS helper

### Medium Confidence (60-89%)

- Similar pattern exists
- Combining multiple components
- Complex layout

### Low Confidence (< 60%)

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
