## Introduction

CSS (Cascading Style Sheets) is used to style and layout web pages. It controls colors, fonts, spacing, positioning, and responsiveness.

---

## CSS Syntax

CSS consists of selectors and declarations:

```css
selector {
    property: value;
}
```

Example:

```css
p {
    color: blue;
    font-size: 16px;
}
```

---

## Ways to Apply CSS

### Inline CSS

```html
<p style="color: red;">This is a red paragraph.</p>
```

### Internal CSS

```html
<style>
p {
    color: green;
}
</style>
```

### External CSS

```html
<link rel="stylesheet" href="styles.css">
```

External stylesheets are the recommended approach for maintainability.

---

## Selectors

### Basic Selectors

```css
h1 { color: blue; }  /* Element selector */
.class-name { color: red; }  /* Class selector */
#id-name { color: green; }  /* ID selector */
```

### Grouping Selectors

```css
h1, h2, p { color: gray; }
```

### Descendant Selector

```css
div p { color: purple; }
```

### Pseudo-Classes

```css
a:hover { color: orange; }
input:focus { border: 2px solid blue; }
```

---

## Box Model

Elements in CSS are structured using the box model:

```
[ Margin ]
[ Border ]
[ Padding ]
[ Content ]
```

Example:

```css
div {
    width: 200px;
    padding: 10px;
    border: 2px solid black;
    margin: 20px;
}
```

---

## Positioning Elements

### Static (default)

```css
position: static;
```

### Relative

```css
position: relative;
top: 10px; left: 10px;
```

### Absolute

```css
position: absolute;
top: 50px; left: 50px;
```

### Fixed

```css
position: fixed;
bottom: 0; right: 0;
```

### Flexbox

```css
display: flex;
align-items: center;
justify-content: space-between;
```

---

## Responsive Design

### Media Queries

```css
@media (max-width: 600px) {
    body { background-color: lightgray; }
}
```

### CSS Grid

```css
display: grid;
grid-template-columns: repeat(3, 1fr);
gap: 10px;
```

---

## Best Practices

- Use external stylesheets for better organization.
- Minimize the use of `!important`.
- Keep selectors specific but not overly complex.
- Optimize CSS for performance.
- Use rem/em for scalable layouts.

---

## Additional Resources

- [MDN Web Docs on CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [CSS Tricks](https://css-tricks.com/)

---