# CSS Box Model

## Diagram
```
+------------------------------+
|      Margin (transparent)    |
|  +------------------------+  |
|  |    Border (visible)    |  |
|  |  +------------------+  |  |
|  |  |  Padding (space) |  |  |
|  |  |  +------------+  |  |  |
|  |  |  |  Content   |  |  |  |
|  |  |  | (text/...) |  |  |  |
|  |  |  +------------+  |  |  |
|  |  +------------------+  |  |
|  +------------------------+  |
+------------------------------+
```

## Content Size
```css
.element {
  width: 300px;      /* Content width */
  height: 200px;     /* Content height */
}
```

## Padding
```css
.element {
  padding: 20px;                    /* All sides */
  padding: 10px 20px;               /* Top/Bottom, Right/Left */
  padding: 10px 20px 15px 30px;     /* Top, Right, Bottom, Left (TRBL) */

  /* Individual properties */
  padding-top: 10px;
  padding-right: 20px;
  padding-bottom: 15px;
  padding-left: 30px;
}
```

## Border
```css
.element {
  border: 2px solid #333;           /* Shorthand */
  border-width: 2px;
  border-style: solid;
  border-color: #333;

  /* Individual sides */
  border-top: 1px dashed red;
  border-radius: 10px;              /* Rounded corners */
}
```

## Margin
```css
.element {
  margin: 20px;                     /* All sides */
  margin: 0 auto;                   /* Center horizontally */
  margin: 10px 20px 30px 40px;      /* TRBL */

  /* Negative margins */
  margin-left: -10px;               /* Can pull elements */
}
```

## Total Size (content-box)
```css
.box {
  width: 300px;
  padding: 20px;
  border: 5px solid black;
  /* Total width = 300 + 40 + 10 = 350px! */
}
```

## Border-Box
```css
.box {
  box-sizing: border-box;
  width: 300px;
  padding: 20px;
  border: 5px solid black;
  /* Total width = 300px (content shrinks to fit) */
}
```

## Global Box Sizing
```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
```

## Centering
```css
.center-me {
  width: 80%;
  max-width: 1200px;
  margin: 0 auto;  /* Top/Bottom = 0, Left/Right = auto */
}
```

## Formula
```text
/* With content-box (default) */
totalWidth = width + padding-left + padding-right 
             + border-left + border-right + margin-left + margin-right

/* With border-box */
contentWidth = width - padding-left - padding-right 
               - border-left - border-right
```
