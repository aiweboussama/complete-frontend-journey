# CSS Classes and IDs -- Complete Guide

## Introduction

In CSS, **classes** and **IDs** are selectors used to target HTML
elements and apply styles.\
They are fundamental concepts for building structured, maintainable, and
scalable websites.

---

# 1. CSS Classes

## What is a Class?

A **class** is a reusable selector that can be applied to multiple HTML
elements.

### HTML Example

```html
<p class="text-red">Hello World</p>
```

### CSS Example

```css
.text-red {
  color: red;
}
```

---

## Key Characteristics of Classes

- Reusable across multiple elements
- An element can have multiple classes
- Lower specificity than IDs
- Preferred for styling

### Multiple Elements Example

```html
<p class="box">Box 1</p>
<div class="box">Box 2</div>
```

```css
.box {
  padding: 20px;
  background-color: lightgray;
}
```

---

## Multiple Classes on One Element

```html
<button class="btn primary large">Click Me</button>
```

```css
.btn {
  padding: 10px;
}
.primary {
  background: blue;
  color: white;
}
.large {
  font-size: 20px;
}
```

---

# 2. CSS IDs

## What is an ID?

An **ID** is a unique selector used for a single element on a page.

### HTML Example

```html
<h1 id="main-title">Welcome</h1>
```

### CSS Example

```css
#main-title {
  color: blue;
}
```

---

## Key Characteristics of IDs

- Must be unique per page
- Only one ID per element
- Higher specificity than classes
- Often used for JavaScript or anchor links

---

# 3. Class vs ID Comparison

Feature Class ID

---

CSS Symbol . \#
Reusable Yes No
Multiple per element Yes No
Specificity Lower Higher
Best for Styling groups Unique elements

---

# 4. Specificity Explained

CSS uses specificity to decide which style wins.

Order of priority:

1.  Element selector (p)
2.  Class selector (.box)
3.  ID selector (#box)
4.  Inline styles

Example:

```css
.box {
  color: green;
}
#box {
  color: red;
}
```

```html
<p
  class="box"
  id="box"
>
  Hello
</p>
```

Result: Text will be **red** because ID has higher specificity.

---

# 5. Combining Class and ID

You can combine selectors for more precision.

```css
.box#special-box {
  background: orange;
}
```

Targets:

```html
<div
  class="box"
  id="special-box"
></div>
```

---

# 6. Common Naming Conventions

## Good Naming Practices

- Use meaningful names
- Use kebab-case
- Avoid styling-based names

### Good Examples

    .navbar
    .card
    .button-primary
    .user-profile

### Avoid

    .red-text
    .big-box

---

# 7. BEM Naming Technique

BEM = Block Element Modifier

Example:

```html
<div class="card card--featured">
  <h2 class="card__title">Title</h2>
</div>
```

Meaning:

- card → Block
- card\_\_title → Element
- card--featured → Modifier

This improves scalability and organization.

---

# 8. Best Practices

Use classes for styling\
 Avoid overusing IDs in CSS\
 Keep specificity low\
 Use semantic, meaningful names\
 Structure CSS clearly

---

# 9. Complete Working Example

## HTML

```html
<div class="card">
  <h2 id="main-title">My Card</h2>
  <p class="text">This is content.</p>
</div>
```

## CSS

```css
.card {
  border: 1px solid black;
  padding: 20px;
}

#main-title {
  color: blue;
}

.text {
  font-size: 16px;
}
```

---

# Final Summary

- Classes are reusable and preferred for styling.
- IDs are unique and have higher specificity.
- Combine them carefully.
- Follow naming conventions for scalable projects.

---

Author: CSS Learning Guide
