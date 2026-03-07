# HTML Lists Guide (README)

## Introduction

HTML lists are used to group related items together. The two most common
types of lists are:

-   **Ordered Lists (`<ol>`)** -- items are displayed with numbers or
    letters.
-   **Unordered Lists (`<ul>`)** -- items are displayed with bullet
    points.

Each list contains **list items** defined with the `<li>` tag.

------------------------------------------------------------------------

# 1. Ordered Lists

## Syntax

``` html
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ol>
```

### Result

1.  First item\
2.  Second item\
3.  Third item

------------------------------------------------------------------------

## Common Ordered List Attributes

### 1. `type`

Changes the numbering style.

  Value   Description
  ------- --------------------------
  1       Default numbers
  A       Uppercase letters
  a       Lowercase letters
  I       Uppercase Roman numerals
  i       Lowercase Roman numerals

### Example

``` html
<ol type="A">
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ol>
```

------------------------------------------------------------------------

### 2. `start`

Defines the starting number of the list.

``` html
<ol start="5">
  <li>Item</li>
  <li>Item</li>
</ol>
```

Result:

5.  Item\
6.  Item

------------------------------------------------------------------------

### 3. `reversed`

Displays the list in descending order.

``` html
<ol reversed>
  <li>Step Three</li>
  <li>Step Two</li>
  <li>Step One</li>
</ol>
```

------------------------------------------------------------------------

# 2. Unordered Lists

## Syntax

``` html
<ul>
  <li>Apple</li>
  <li>Banana</li>
  <li>Orange</li>
</ul>
```

### Result

-   Apple
-   Banana
-   Orange

------------------------------------------------------------------------

## Bullet Styles

The style of bullets can be changed using CSS.

### Example

``` html
<ul style="list-style-type:square;">
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

### Common Values

-   `disc` (default)
-   `circle`
-   `square`
-   `none`

------------------------------------------------------------------------

# 3. List Style in CSS

In HTML and CSS, **`list-style`** controls the appearance of the markers
(bullets or numbers) used in lists.

These markers appear before each `<li>` element.

### Example

``` css
ul {
  list-style-type: square;
}
```

Result:

■ HTML\
■ CSS\
■ JavaScript

------------------------------------------------------------------------

## Common `list-style-type` Values

### For Unordered Lists

  Value    Description
  -------- -----------------------
  disc     Default filled circle
  circle   Hollow circle
  square   Square bullet
  none     Removes the bullet

### For Ordered Lists

  Value         Description
  ------------- -------------
  decimal       1, 2, 3
  upper-alpha   A, B, C
  lower-alpha   a, b, c
  upper-roman   I, II, III
  lower-roman   i, ii, iii

------------------------------------------------------------------------

## Removing List Markers (Very Common Technique)

Developers often remove bullets when creating navigation menus.

``` css
ul {
  list-style: none;
}
```

------------------------------------------------------------------------

## The `list-style` Shorthand

Instead of writing multiple properties, you can combine them:

``` css
list-style: square inside;
```

This shorthand combines:

-   `list-style-type`
-   `list-style-position`
-   `list-style-image`

------------------------------------------------------------------------

# 4. Nested Lists

Lists can be placed inside other lists to create sub-items.

``` html
<ul>
  <li>Frontend
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
    </ul>
  </li>
</ul>
```

------------------------------------------------------------------------

# 5. Most Used Techniques

## 1. Navigation Menus

Lists are commonly used for navigation bars.

``` html
<ul class="navbar">
  <li>Home</li>
  <li>About</li>
  <li>Contact</li>
</ul>
```

------------------------------------------------------------------------

## 2. Task Lists

Used for steps or instructions.

``` html
<ol>
  <li>Install Node.js</li>
  <li>Create project folder</li>
  <li>Run the application</li>
</ol>
```

------------------------------------------------------------------------

## 3. Removing Default Styling

``` css
ul {
  list-style: none;
  padding: 0;
}
```

This technique is widely used in **modern website navigation menus**.

------------------------------------------------------------------------

# 6. Best Practices

-   Use **ordered lists** for steps or sequences.
-   Use **unordered lists** for groups of related items.
-   Avoid using lists only for layout.
-   Use **CSS for styling** instead of HTML attributes when possible.

------------------------------------------------------------------------

# Conclusion

HTML lists are fundamental elements for structuring content. By
combining `<ul>`, `<ol>`, and `<li>` with CSS styling, developers can
create clean and organized layouts for menus, documentation,
instructions, and more.

------------------------------------------------------------------------

Author: Web Development Notes
