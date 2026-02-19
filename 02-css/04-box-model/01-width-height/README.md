# CSS Box Model -- Complete Guide

## 1. Box Model Diagram

    +--------------------------------------------------+
    |                    MARGIN                        |
    |  +--------------------------------------------+  |
    |  |                   BORDER                   |  |
    |  |  +--------------------------------------+  |  |
    |  |  |                PADDING               |  |  |
    |  |  |  +--------------------------------+  |  |  |
    |  |  |  |            CONTENT             |  |  |  |
    |  |  |  +--------------------------------+  |  |  |
    |  |  +--------------------------------------+  |  |
    |  +--------------------------------------------+  |
    +--------------------------------------------------+

## 2. The Four Parts of the Box Model (Brief Explanation)

### Content

The actual text, image, or media inside the element.

### Padding

Space between the content and the border.

### Border

Wraps around the padding and content.

### Margin

Space outside the border that separates elements.

---

# Understanding Width & Height Deeply

## 1. width and height

- `width` → Controls the width of the **content area** (unless
  `box-sizing: border-box` is used).
- `height` → Controls the height of the **content area**.

Example:

```css
.box {
  width: 300px;
  height: 200px;
}
```

---

## 2. Width with Percentage (%)

Percentage width is calculated relative to the **parent element's
width**.

```css
.container {
  width: 800px;
}

.child {
  width: 50%; /* 400px */
}
```

Important: - `%` for width depends on the parent width. - `%` for
height only works if the parent has a defined height.

---

# Intrinsic Sizing Keywords

## min-content

The smallest width the content can shrink to without overflowing
unnecessarily.

```css
.box {
  width: min-content;
}
```

The element becomes as small as possible (breaks text at every
opportunity).

---

## max-content

The width the content needs if it does NOT wrap at all.

```css
.box {
  width: max-content;
}
```

The element expands as much as needed to fit content in one line.

---

# min-width & max-width

## min-width

Prevents the element from becoming smaller than a specific value.

```css
.box {
  width: 50%;
  min-width: 300px;
}
```

Even if 50% becomes 200px → it stays 300px minimum.

---

## max-width

Prevents the element from exceeding a specific value.

```css
.box {
  width: 100%;
  max-width: 800px;
}
```

Common for responsive layouts.

---

# min-height & max-height

## min-height

Ensures the element is never shorter than a given value.

```css
.box {
  min-height: 200px;
}
```

---

## max-height

Limits the maximum height.

```css
.box {
  max-height: 400px;
  overflow: auto;
}
```

---

# Most Common Combinations (Best Practices)

## 1. Responsive Container (Most Used Pattern)

```css
.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
}
```

- Fills screen on small devices\
- Stops growing on large screens\
- Perfectly centered

---

## 2. Flexible but Safe Card

```css
.card {
  width: 100%;
  max-width: 400px;
  min-width: 250px;
}
```

- Flexible\
- Never too small\
- Never too large

---

## 3. Full Height Section

```css
.section {
  min-height: 100vh;
}
```

Ensures section always fills at least the full viewport height.

---

# How Browser Resolves Conflicts

If you set:

```css
width: 500px;
min-width: 600px;
max-width: 800px;
```

Final width = **600px** (because min-width wins).

If:

```css
width: 900px;
max-width: 800px;
```

Final width = **800px** (max-width limits it).

### Priority Rule:

    min-width > width > max-width

(Same applies to height.)

---

# Bonus: box-sizing

By default:

```css
box-sizing: content-box;
```

Width applies only to content.

Better practice:

```css
box-sizing: border-box;
```

Width includes padding and border.

---

# Final Summary

Property Controls

---

width Content width
height Content height
min-width Minimum allowed width
max-width Maximum allowed width
min-height Minimum allowed height
max-height Maximum allowed height
min-content Smallest intrinsic size
max-content Largest intrinsic size

---

# Recommended Default Setup

```css
* {
  padding: 0px;
  margin: 0px;
  box-sizing: border-box;
}
```

This makes layout sizing predictable and easier to manage.

---

© 2026 -- CSS Box Model Guide
