# CSS Margin Guide

## What is Margin in CSS?

Margin is the space outside an element's border. It creates distance
between the element and other elements around it.

Margin does not affect the internal size of an element. Instead, it
controls the outer spacing.

------------------------------------------------------------------------

## The Margin Box Model Context

In the CSS box model, the structure is:

-   Content
-   Padding
-   Border
-   Margin

Margin is always the outermost layer.

------------------------------------------------------------------------

## Basic Syntax

``` css
selector {
  margin: value;
}
```

Example:

``` css
div {
  margin: 20px;
}
```

This applies 20px margin on all four sides (top, right, bottom, left).

------------------------------------------------------------------------

## Margin Shorthand

You can define margins in different ways.

### 1. One Value (All Sides)

``` css
margin: 20px;
```

Applies 20px to top, right, bottom, and left.

------------------------------------------------------------------------

### 2. Two Values (Vertical \| Horizontal)

``` css
margin: 20px 40px;
```

-   20px → top and bottom
-   40px → left and right

------------------------------------------------------------------------

### 3. Three Values (Top \| Horizontal \| Bottom)

``` css
margin: 10px 20px 30px;
```

-   10px → top
-   20px → left and right
-   30px → bottom

------------------------------------------------------------------------

### 4. Four Values (Top \| Right \| Bottom \| Left)

``` css
margin: 10px 15px 20px 25px;
```

Order goes clockwise: Top → Right → Bottom → Left

------------------------------------------------------------------------

## Individual Margin Properties

You can set margins separately:

``` css
margin-top: 20px;
margin-right: 10px;
margin-bottom: 15px;
margin-left: 5px;
```

------------------------------------------------------------------------

## Common Margin Patterns

### 1. Centering a Block Element

``` css
.container {
  width: 300px;
  margin: 0 auto;
}
```

Explanation: - 0 → top and bottom - auto → left and right This centers
the element horizontally.

------------------------------------------------------------------------

### 2. Adding Vertical Spacing Between Sections

``` css
section {
  margin-bottom: 40px;
}
```

Commonly used to separate content sections.

------------------------------------------------------------------------

### 3. Resetting Default Margins

Browsers add default margins to elements like body and headings.

``` css
body {
  margin: 0;
}
```

This removes unwanted spacing.

------------------------------------------------------------------------

### 4. Creating Space Between Inline Elements

``` css
button {
  margin-right: 10px;
}
```

Adds spacing between buttons.

------------------------------------------------------------------------

## Margin Collapse

Vertical margins between block elements can collapse.

Example:

``` css
div {
  margin-top: 20px;
  margin-bottom: 20px;
}
```

If two elements are stacked vertically, the larger margin is used
instead of adding both together.

------------------------------------------------------------------------

## Negative Margin

Margins can be negative.

``` css
div {
  margin-top: -10px;
}
```

This pulls the element upward. Use carefully because it can break layout
flow.

------------------------------------------------------------------------

## Key Takeaways

-   Margin controls outer spacing.
-   It does not affect the element's internal size.
-   Shorthand values follow clockwise order.
-   `margin: 0 auto;` is commonly used for horizontal centering.
-   Vertical margins can collapse.
-   Negative margins are allowed but should be used carefully.

------------------------------------------------------------------------

End of Guide
