## Introduction

JavaScript (JS) is a programming language used to add interactivity to web pages. It enables dynamic content, event handling, and API integration.

---

## JavaScript Basics

### Including JavaScript in HTML

#### Inline JavaScript

```html
<button onclick="alert('Hello, World!')">Click Me</button>
```

#### Internal JavaScript

```html
<script>
    alert("Hello, World!");
</script>
```

#### External JavaScript

```html
<script src="script.js"></script>
```

Using external scripts improves code organization and reusability.

---

## Variables and Data Types

### Declaring Variables

```js
var name = "John"; // Old way
let age = 25; // Preferred for variables that change
const PI = 3.1416; // Constant value
```

### Data Types

```js
let number = 10; // Number
let text = "Hello"; // String
let isTrue = true; // Boolean
let list = [1, 2, 3]; // Array
let person = { name: "Alice", age: 30 }; // Object
```

---

## Functions

### Function Declaration

```js
function greet(name) {
    return "Hello, " + name;
}
console.log(greet("Alice"));
```

### Arrow Function (ES6)

```js
const greet = (name) => `Hello, ${name}`;
console.log(greet("Alice"));
```

---

## Control Structures

### If-Else Statement

```js
let num = 10;
if (num > 5) {
    console.log("Greater than 5");
} else {
    console.log("Less than or equal to 5");
}
```

### Loops

#### For Loop

```js
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

#### While Loop

```js
let i = 0;
while (i < 5) {
    console.log(i);
    i++;
}
```

---

## Arrays and Objects

### Working with Arrays

```js
let colors = ["red", "green", "blue"];
console.log(colors[0]); // red
colors.push("yellow");
console.log(colors.length); // 4
```

### Working with Objects

```js
let person = {
    name: "Alice",
    age: 30,
    greet: function() {
        return "Hello, " + this.name;
    }
};
console.log(person.greet());
```

---

## DOM Manipulation

### Selecting Elements

```js
let heading = document.getElementById("title");
let paragraphs = document.querySelectorAll("p");
```

### Changing Content

```js
document.getElementById("title").innerText = "New Title";
```

### Adding Event Listeners

```js
document.getElementById("btn").addEventListener("click", function() {
    alert("Button clicked!");
});
```

---

## Asynchronous JavaScript

### setTimeout & setInterval

```js
setTimeout(() => console.log("Hello after 3 seconds"), 3000);
setInterval(() => console.log("Repeats every second"), 1000);
```

### Fetch API (AJAX)

```js
fetch("https://api.example.com/data")
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.log(error));
```

---

## ES6+ Features

- Template Literals: ``console.log(`Hello, ${name}`);``
- Destructuring: `let {name, age} = person;`
- Spread Operator: `let newArray = [...oldArray];`
- Promises & Async/Await:

```js
async function fetchData() {
    let response = await fetch("https://api.example.com");
    let data = await response.json();
    console.log(data);
}
fetchData();
```

---

## Best Practices

- Use `const` and `let` instead of `var`
- Keep code modular with functions
- Use `===` instead of `==` to avoid type coercion
- Handle errors with `try-catch`
- Optimize performance with event delegation and throttling

---

## Additional Resources

- [MDN Web Docs on JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [JavaScript Info](https://javascript.info/)

---