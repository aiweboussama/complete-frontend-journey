# 02 - HTML Headings (h1 to h6)

This lesson is about using headings to give a page a clear structure.
Headings are not only for bigger text; they show how content is organized.

## Files in this folder

- `01-index.html`: shows all heading levels from `h1` to `h6`
- `02-style.css`: adds basic visual styling to each heading

## Example from this codebase

From `02-headings/01-index.html`:

```html
<body>
  <h1>Main Page Title (H1)</h1>
  <h2>Section Title (H2)</h2>
  <h3>Subsection Title (H3)</h3>
  <h4>H4 Example</h4>
  <h5>H5 Example</h5>
  <h6>H6 Example</h6>
</body>
```

From `02-headings/02-style.css`:

```css
h1,
h2,
h3,
h4,
h5,
h6 {
  margin-bottom: 15px;
  padding: 15px;
  background-color: #ffffff;
  border-left: 4px solid #1a73e8;
}
```

This CSS gives all heading levels a consistent look while the HTML still controls the semantic order.

## How hierarchy should work

Use headings in order when possible:

1. `h1` for the main page title
2. `h2` for major sections
3. `h3` for subsections under an `h2`
4. `h4` to `h6` for deeper levels only when needed

Try not to jump from `h1` straight to `h4` unless there is a real structural reason.

## Examples outside this project

1. Blog article
   `h1`: "How to Start Running"
   `h2`: "Shoes", "Training Plan", "Recovery"
   `h3`: under "Training Plan", you might have "Week 1" and "Week 2"

2. Documentation page
   `h1`: "React Router Guide"
   `h2`: "Installation", "Basic Routes", "Nested Routes"
   `h3`: under "Basic Routes", "Route Params"

3. Product page
   `h1`: product name
   `h2`: "Features", "Specifications", "Reviews"
   `h3`: inside "Specifications", headings like "Display" and "Battery"

## Common mistakes to avoid

- Using headings only to change text size
- Skipping levels without a structural reason
- Putting multiple unrelated `h1` elements on the same simple page
- Styling plain paragraphs to look like headings instead of using heading tags

## Quick summary

Use `h1` to `h6` to describe structure first, then style them with CSS.
In this lesson, `01-index.html` shows the semantic levels and `02-style.css` handles visual presentation.
