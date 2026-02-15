# Waves & Ripples

Expert guidance for BeerCSS interactive effects based on official documentation.

Source: `beercss/docs/WAVES-AND-RIPPLES.md`
Last Updated: 2026-02-15

---

## Quick Reference

### Interactive Patterns

**Standard Wave:**
```html
<button class="wave">Click for wave effect</button>
```

**Standard Ripple:**
```html
<button class="ripple">Click for ripple effect</button>
```

**Slow/Fast Ripples:**
```html
<button class="slow-ripple">Slow Animation</button>
<button class="fast-ripple">Fast Animation</button>
```

---

## Attributes & Classes

### Effects
- `wave`: Spreading circle animation from the click point.
- `ripple`: Expansion animation covering the entire element.
- `slow-ripple`: Slower ripple duration.
- `fast-ripple`: Faster ripple duration.

---

## Rules from Source

1. **Usage:** Apply these classes to interactive elements like `button`, `a`, or `chip`.
2. **Combination:** These effects can be combined with other component classes.
3. **Feedback:** Use these classes to provide visual confirmation of user interaction.

---

## Common Pitfalls

❌ **Don't:**
```html
<!-- Incorrectly applying to non-interactive static text -->
<p class="wave">Static Text</p>
```

✅ **Do:**
```html
<button class="wave">Action</button>
```
