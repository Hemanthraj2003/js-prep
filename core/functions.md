# FUNCTIONS

In javaScript, functions are `first-class objects`, which means they can be treated like any other value. They can be assigned to variables, passed as arguments to other functions, and returned from functions.

Functions are a reusable block of code that perfroms a specific task.
They help in breaking down complex problems into smaller, manageable pieces, promoting code reusability and maintainability.

## Function Declaration

we can define a function using the `function` keyword followed by the function name and parentheses `()`. The code to be executed is enclosed within curly braces `{}`. and the function can optionally take parameters.

```javascript
// syntax
function functionName(parameter1, parameter2, ...) {
  // code to be executed
}
```

### Example

```javascript
function greet(name) {
  console.log("Hello, " + name + "!");
}
greet("Alice"); // Hello, Alice!
greet("Bob"); // Hello, Bob!
```

#### `Note:` Functions are `hoisted` to the top of their scope, which means we can call a function before its declaration.

```javascript
greet("Alice"); // Hello, Alice!
function greet(name) {
  console.log("Hello, " + name + "!");
}
```

## Types of Functions

1. General Functions

2. Anonymous Functions

3. Arrow Functions

4. Self-Invoking Functions

5. Callback Functions

6. Higher-Order Functions
