# Decision Protocol

## When to Ask vs When to Decide

**Purpose:** Guide Gemini CLI on when to proceed vs when to consult user.

---

## Decision Matrix

### ✅ PROCEED WITHOUT ASKING

**Criteria:** All of these are true:
1. Component exists in documentation (in `@./components/`)
2. Pattern is an exact match from docs/examples.
3. Uses theme colors from `@./rules/color-system.md`.
4. Follows BeerCSS conventions strictly.

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
1. Combining multiple components.
2. Complex layout.
3. Similar pattern exists but not an exact match.
4. Multiple valid approaches/variations.

**Examples:**
```
User: "Create a login form"
→ VERIFY: "Should I include: username, password, remember me, submit?"
→ THEN PROCEED with confirmed spec.

User: "Add navigation"
→ VERIFY: "Desktop sidebar, mobile bottom bar, or both?"
→ THEN PROCEED with choice.
```

**Protocol:**
1. Ask clarifying question.
2. Present 2-3 specific options.
3. Wait for response.
4. Proceed with confirmed approach.

---

### 🛑 ASK USER (REQUIRED)

**Criteria:** ANY of these is true:
1. Component NOT in documentation.
2. Custom class requested (not a BeerCSS class).
3. Color NOT in theme/tokens.
4. Pattern significantly different from docs.
5. Would require custom CSS styling.

**Examples:**
```
User: "Create a fancy-slider component"
→ ASK: "BeerCSS has 'slider' component. Did you mean that, or something custom?"

User: "Use class='product-card'"
→ ASK: "product-card isn't a BeerCSS class. Should I use 'card' instead or create custom?"

User: "Make it neon green"
→ ASK: "Neon green isn't in your theme. Should I add it to styles.css?"
```

**Protocol:**
1. Identify the uncertainty.
2. Explain why asking (referencing documentation).
3. Provide documented alternatives.
4. Wait for decision.
5. Proceed ONLY after confirmation.

---

## Question Format

### ✅ GOOD Questions (Specific)
- "Should I use navigation rail (desktop sidebar) or bottom bar (mobile)?"
- "The theme uses blue primary. Should the button be blue or use error red?"
- "This pattern isn't in docs. Should I create with custom CSS or use the closest match?"

### ❌ BAD Questions (Vague)
- "Is this okay?"
- "Should I proceed?"
- "What do you want?"

---

## Confidence Thresholds

- **High Confidence (90-100%):** Exact match in docs. → **PROCEED**
- **Medium Confidence (60-89%):** Valid pattern but needs choice. → **VERIFY**
- **Low Confidence (< 60%):** Not in docs or custom request. → **ASK USER**

---

## Escalation Path

1. Try to match with a documented component in `@./components/`.
2. Try to find a similar component or pattern in examples.
3. Check if a combination of standard components works.
4. **ASK USER** for clarification/decision.
5. If user confirms custom: Explain required custom CSS and proceed only with approval.

---

## Summary

```
Standard pattern?       → PROCEED
Multiple valid options? → VERIFY with user
Not in documentation?   → ASK before proceeding
Complex request?        → ASK for specification
Custom CSS needed?      → ASK for approval
```

**Golden Rule:** It's better to ask once than apologize twice.
