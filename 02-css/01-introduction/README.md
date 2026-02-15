# CSS Simple Demo

## What is CSS?

CSS stands for **Cascading Style Sheets**.  
It is used to style HTML elements like colors, fonts, spacing, and layout.

---

## 1) External CSS

External CSS means writing styles in a separate file (like `02-style.css`)  
and linking it to HTML.

Example:

```html
<link rel="stylesheet" href="02-style.css" />
```

```css
p {
  color: #444;
}
```

This is the best and most recommended method.

---

## 2) Internal CSS

Internal CSS is written inside the HTML file using the `<style>` tag.

Example:

```html
<style>
h1 {
  color: blue;
  text-align: center;
}
</style>
```

It is useful for small pages.

---

## 3) Inline CSS

Inline CSS is written directly inside an HTML element using `style=""`.

Example:

```html
<p style="color: red; font-weight: bold">
  This paragraph uses inline CSS.
</p>
```

It is quick but not recommended for large projects.
