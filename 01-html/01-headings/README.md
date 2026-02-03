# HTML Headings (h1 → h6)

## 📌 Overview

Headings in HTML are used to define titles and subtitles on a webpage.  
They help organize content into a clear structure, just like chapters in a book.

HTML provides **six heading levels**, from:

- `<h1>` (most important)
- `<h6>` (least important)

---

## ✅ Heading Levels

| Tag   | Meaning |
|------|---------|
| `<h1>` | Main page title |
| `<h2>` | Section heading |
| `<h3>` | Subsection heading |
| `<h4>` | Smaller heading |
| `<h5>` | Less important heading |
| `<h6>` | Smallest heading |

---

## ✅ Example Code

```html
<h1>Main Title</h1>
<h2>Section Title</h2>
<h3>Subsection Title</h3>
<h4>Small Heading</h4>
<h5>Smaller Heading</h5>
<h6>Smallest Heading</h6>
---

## ✅ Default Browser Styles for Headings

Even if you do not write any CSS, browsers apply default styling to heading tags.

Headings are:

- **bold by default**
- have different **font sizes**
- include **top and bottom margin**

### ✅ Default Font Size & Weight (Approximate)

| Tag   | Default Font Size | Default Font Weight |
|------|------------------|--------------------|
| `<h1>` | 2em (32px)        | Bold (700)         |
| `<h2>` | 1.5em (24px)      | Bold (700)         |
| `<h3>` | 1.17em (18.7px)   | Bold (700)         |
| `<h4>` | 1em (16px)        | Bold (700)         |
| `<h5>` | 0.83em (13.3px)   | Bold (700)         |
| `<h6>` | 0.67em (10.7px)   | Bold (700)         |

---

### ✅ Notes

- The sizes are relative to the browser’s default font size (usually 16px).
- All headings are bold automatically because browsers set:

```css
h1, h2, h3, h4, h5, h6 {
  font-weight: bold;
}
