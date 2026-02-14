# Introduction to HTML (First Lesson)

This is my first HTML practice file. The goal is to understand the minimum structure every page needs before moving to CSS and JavaScript.

## File in this folder

- `index.html`: basic page that shows `hello,world!`

## Code used

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>introduction</title>
  </head>
  <body>
    <div>hello,world!</div>
  </body>
</html>
```

## Quick notes

- `<!doctype html>` tells the browser to use HTML5 mode.
- `<html lang="en">` sets the document language.
- `<head>` contains metadata (not visible page content).
- `<meta charset="UTF-8" />` prevents character encoding problems.
- `<meta name="viewport" content="width=device-width, initial-scale=1.0" />` helps the page display correctly on phones.
- `<title>` sets the tab name in the browser.
- `<body>` contains everything visible on the page.
- `<div>` here is just a simple container.

## How to view it

Open `index.html` in any browser, or run it with Live Server in VS Code.

## Next step

Replace the `<div>` text with headings, paragraphs, and links to keep practicing basic HTML tags.
