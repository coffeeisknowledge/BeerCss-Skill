# Feedback & Actions Reference

Detailed reference for components that provide feedback or trigger actions.

## Button

### Purpose
Triggers actions.

### Basic Pattern
```html
<button class="fill">Primary Action</button>
```

### Variations
- **Outlined:** `class="border"`.
- **Text:** No extra class.
- **Icon + Text:** `<i>home</i><span>Home</span>`.

---

## Dialog (Modal)

### Purpose
Critical interactions or information.

### Basic Pattern
```html
<dialog id="dialog-id">
  <h5>Title</h5>
  <nav class="right-align">
    <button data-ui="#dialog-id">Close</button>
  </nav>
</dialog>
```

---

## Snackbar

### Purpose
Brief messages.

### Basic Pattern
```html
<div class="snackbar bottom" id="snackbar-id">
  <span>Message</span>
</div>
```

---

## Progress

### Purpose
Showing task duration or wait time.

### Basic Pattern
```html
<progress class="circle"></progress>
```

---

## Badge & Chip

### Badge
Used to emphasize elements.
```html
<button>
  <i>notifications</i>
  <label class="badge circle red">3</label>
</button>
```

### Chip
Compact elements for tags or filters.
```html
<label class="chip border">Tag name</label>
```
