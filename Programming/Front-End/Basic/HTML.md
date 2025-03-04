## Introduction

HTML (HyperText Markup Language) is the standard language for creating web pages. It provides the structure of a webpage using elements enclosed in tags.

---

## Basic Structure

Every HTML document follows a basic structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Webpage</title>
</head>
<body>
    <h1>Welcome to My Webpage</h1>
    <p>This is a sample webpage.</p>
</body>
</html>
```

---

## Essential HTML Elements

### Headings

```html
<h1>Main Heading</h1>
<h2>Subheading</h2>
<h3>Smaller Subheading</h3>
```

Headings range from `<h1>` to `<h6>` with `<h1>` being the largest.

### Paragraphs & Line Breaks

```html
<p>This is a paragraph.</p>
<br>
<p>This is another paragraph.</p>
```

### Lists

#### Unordered List

```html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
</ul>
```

#### Ordered List

```html
<ol>
    <li>First item</li>
    <li>Second item</li>
</ol>
```

### Links

```html
<a href="https://example.com">Visit Example</a>
```

### Images

```html
<img src="image.jpg" alt="Description of image">
```

### Tables

```html
<table>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>Data 1</td>
        <td>Data 2</td>
    </tr>
</table>
```

### Forms

```html
<form action="submit.php" method="POST">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">
    <input type="submit" value="Submit">
</form>
```

---

## Semantic HTML

Semantic HTML enhances accessibility and SEO. Key tags:

- `<header>`: Defines introductory content
- `<nav>`: Navigation links
- `<main>`: Main content of the document
- `<article>`: Self-contained content
- `<section>`: Thematic grouping of content
- `<aside>`: Sidebar content
- `<footer>`: Footer section

Example:

```html
<header>
    <h1>Website Title</h1>
</header>
<nav>
    <a href="#">Home</a>
    <a href="#">About</a>
</nav>
<main>
    <article>
        <h2>Blog Post</h2>
        <p>Content goes here.</p>
    </article>
</main>
<footer>
    <p>© 2025 My Website</p>
</footer>
```

---

## HTML Best Practices

- Always use semantic elements.
- Close all tags properly.
- Use lowercase for tag names.
- Optimize images for the web.
- Validate your HTML using the [W3C Validator](https://validator.w3.org/).

---

## Additional Resources

- [MDN Web Docs on HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [HTML Reference by W3Schools](https://www.w3schools.com/html/)

---