# CSS Priorities (Specificity) Guide

## Order of CSS Priority (Highest to Lowest)

1. `!important`
2. Inline styles
3. ID selectors (`#id`)
4. Class selectors (`.class`), attributes, pseudo-classes
5. Element selectors (`p`, `div`, etc.)

---

## 1. `!important`

Forces a property to override other normal rules.

```css
p {
  color: blue !important;
}
```

If two rules both use `!important`, normal specificity rules apply.

---

## 2. Inline Styles

Written directly inside HTML.

```html
<p style="color: red;">Hello</p>
```

Inline styles override ID, class, and element selectors, unless another rule uses `!important`.

---

## 3. ID Selector

```css
#title {
  color: red;
}
```

Stronger than class and element selectors.

---

## 4. Class Selector

```css
.text {
  color: blue;
}
```

Stronger than element selectors, weaker than ID.

---

## 5. Element Selector

```css
p {
  color: green;
}
```

Lowest priority.

---

## Important Rule

If two selectors have the same specificity, the one written last in the CSS file wins.

Example:

```css
.text { color: red; }
.text { color: blue; }
```

Result: Blue (last rule wins)

---

## Specificity Score System

CSS calculates specificity like this:

- Inline: 1000
- ID: 100
- Class: 10
- Element: 1

Example:

```css
div#main .box p
```

Specificity = (1 ID, 1 class, 2 elements) = (1,1,2)

---

## Final Summary

`!important > Inline > ID > Class > Element`

If both use `!important`, then:

`Inline > ID > Class > Element`

---

Tip: Avoid overusing `!important`. Use clean class-based styling for better maintainability.
