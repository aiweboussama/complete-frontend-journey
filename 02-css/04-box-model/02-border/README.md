# CSS Border (Box Model) - Practical Guide

The `border` is the line that wraps around an element's padding and content, and sits inside the margin.
It affects layout size unless you use `box-sizing: border-box`.

---

## 1) Border basics

### Shorthand
```css
.box {
  border: 2px solid #222;
}
```

Order (common): `border: <width> <style> <color>;`

### Individual properties
```css
.box {
  border-width: 2px;
  border-style: solid;
  border-color: #222;
}
```

---

## 2) Common border styles

```css
.solid {
  border: 2px solid #222;
}
.dashed {
  border: 2px dashed #222;
}
.dotted {
  border: 2px dotted #222;
}
.double {
  border: 4px double #222;
}
```

Tip: `border-style` is required. If you forget it, the border will not show.

---

## 3) Border on specific sides

### One side only
```css
.card {
  border-left: 6px solid #0a84ff;
}
```

### Mixed sides
```css
.box {
  border-top: 2px solid #222;
  border-right: 0;
  border-bottom: 2px solid #222;
  border-left: 0;
}
```

### Logical properties (RTL/LTR friendly)
```css
.notice {
  border-inline-start: 6px solid #ffb020;
}
```

---

## 4) Border vs layout size

By default:
```css
box-sizing: content-box;
```

So `width` is for the content, and border adds extra size.

Example:
```css
.box {
  width: 300px;
  padding: 20px;
  border: 10px solid #222;
}
```

Total rendered width = 300 + 20 + 20 + 10 + 10 = 360px

### Recommended for predictable sizing
```css
* {
  box-sizing: border-box;
}
```

With `border-box`, border and padding are included inside the declared width.

---

## 5) Transparent borders

Keep spacing without showing a border:

```css
.btn {
  border: 2px solid transparent;
}
.btn-active {
  border-color: #222;
}
```

This keeps spacing stable and uses a normal class (no pseudo-class).

---

## 6) Borders for separators and dividers

### Divider line
```css
.divider {
  border-top: 1px solid #ddd;
}
```

### Table-like rows
```css
.row {
  border-bottom: 1px solid #eee;
}
```

---

## 7) Border images

```css
.fancy {
  border: 12px solid transparent;
  border-image: url("border.png") 30 round;
}
```

Use this when you need decorative frames.

---

# Border Radius (Rounded corners)

`border-radius` rounds the border corners and can clip content/background.

## 1) Basic rounding
```css
.card {
  border: 2px solid #222;
  border-radius: 12px;
}
```

## 2) Perfect circle
```css
.avatar {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  border: 2px solid #222;
}
```

## 3) Pill shape
```css
.pill {
  padding: 10px 16px;
  border: 2px solid #222;
  border-radius: 9999px;
}
```

## 4) Different radius per corner
```css
.box {
  border: 2px solid #222;
  border-radius: 16px 4px 16px 4px; /* TL TR BR BL */
}
```

## 5) Elliptical radius
```css
.shape {
  border: 2px solid #222;
  border-radius: 40px / 20px; /* horizontal / vertical */
}
```

## 6) Overflow + radius
```css
.card {
  border-radius: 12px;
  overflow: hidden;
}
```

---

# Common real-world patterns

## 1) Modern card
```css
.card {
  border: 1px solid #e6e6e6;
  border-radius: 12px;
  padding: 16px;
}
```

## 2) Left accent border (alerts/notes)
```css
.note {
  border-left: 6px solid #0a84ff;
  border-radius: 10px;
  padding: 12px 14px;
}
```

## 3) Simple input border (class only)
```css
.input {
  border: 2px solid #0a84ff;
  border-radius: 10px;
  padding: 10px 12px;
}
```

---

# Quick reference

| Goal | Example |
|------|---------|
| Basic border | `border: 1px solid #222;` |
| One side only | `border-left: 4px solid #0a84ff;` |
| No hover shift | `border: 2px solid transparent;` |
| Rounded corners | `border-radius: 12px;` |
| Circle | `border-radius: 50%;` |
| Pill | `border-radius: 9999px;` |

---

CSS Border and Border Radius Notes (2026)
