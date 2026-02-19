# CSS Padding -- Complete Guide

## What is Padding?

Padding in CSS is the space **inside** an element, between the content
and the border.

It increases the internal spacing of an element without affecting the
outer margin.

------------------------------------------------------------------------

## Basic Syntax

``` css
selector {
  padding: value;
}
```

Example:

``` css
div {
  padding: 20px;
}
```

This adds 20px of space on all four sides (top, right, bottom, left).

------------------------------------------------------------------------

## Padding for Each Side

You can control each side individually:

``` css
div {
  padding-top: 10px;
  padding-right: 20px;
  padding-bottom: 30px;
  padding-left: 40px;
}
```

------------------------------------------------------------------------

## Shorthand Padding

### 1 Value (All Sides)

``` css
padding: 20px;
```

Top = Right = Bottom = Left = 20px

------------------------------------------------------------------------

### 2 Values (Vertical \| Horizontal)

``` css
padding: 10px 20px;
```

Top & Bottom = 10px\
Left & Right = 20px

------------------------------------------------------------------------

### 3 Values (Top \| Horizontal \| Bottom)

``` css
padding: 10px 20px 30px;
```

Top = 10px\
Left & Right = 20px\
Bottom = 30px

------------------------------------------------------------------------

### 4 Values (Top \| Right \| Bottom \| Left)

``` css
padding: 10px 20px 30px 40px;
```

Clockwise order: Top → Right → Bottom → Left

------------------------------------------------------------------------

## Example with Background and Border

``` css
.box {
  background-color: lightblue;
  border: 2px solid black;
  padding: 20px;
}
```

This creates space between the text and the border.

------------------------------------------------------------------------

## Padding with Percentage

Padding can also use percentages:

``` css
div {
  padding: 5%;
}
```

Percentage padding is calculated relative to the **width of the parent
element**.

------------------------------------------------------------------------

## Padding vs Margin

-   Padding → Space inside the element
-   Margin → Space outside the element

Example:

``` css
div {
  padding: 20px;
  margin: 20px;
}
```

------------------------------------------------------------------------

## Best Practice (Modern Responsive Design)

``` css
.container {
  padding: 20px;
  max-width: 1200px;
  margin: auto;
}
```

This keeps content spaced properly and centered.

------------------------------------------------------------------------

## Final Tip

When designing layouts: - Use padding to create internal breathing
space. - Avoid too much padding on small screens. - Combine padding with
`box-sizing: border-box;` for better layout control.

``` css
* {
  box-sizing: border-box;
}
```

------------------------------------------------------------------------

Happy Coding 🚀
