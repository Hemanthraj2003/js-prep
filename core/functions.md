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

### 1. `General Functions`

These are the functions that we define using the `function` keyword followed by a name.

As shown in the above example.

### 2. `Anonymous Functions`

These are the functions that do not have a name and are aften assigned to a variable (also called function expressions).

`note:` these functions are not hoisted.

```javascript
// syntax
let functionName = function (parameter1, parameter2, ...) {
  // code to be executed
};
```

### Example

```javascript
let add = function (a, b) {
  return a + b;
};
console.log(add(2, 3)); // 5
```

### 3. `Arrow Functions`

Arrow functions provide a shorter syntax for writing functions. They are always anonymous and are often used for short functions.

arrow functions do not have their own `this` context, which means they inherit `this` from the surrounding code.

```javascript
// syntax
let functionName = (parameter1, parameter2, ...) => {
  // code to be executed
};
```

### Example

```javascript
let multiply = (a, b) => {
  return a * b;
};
console.log(multiply(2, 3)); // 6
```

In arrow functions,

- if there is only one parameter, the parentheses can be omitted. `let square = x => x * x;`

- if the function body contains a single expression, the curly braces and `return` keyword can be omitted. `let square = x => x * x;`

- if their are no parameters, we can use `_` or empty parentheses `()`. `let greet = () => console.log("Hello!");` or `let greet = _ => console.log("Hello!");`

### 4. `Self-Invoking Functions` or `Immediately Invoked Function Expressions (IIFE)`

These functions are executed immediately after they are defined.
these functions needs to be wrapped in parentheses and followed by another set of parentheses to invoke them.we can pass arguments to the function by including them in the second set of parentheses.

```javascript
// syntax
(function (parameter1, parameter2, ...) {
  // code to be executed
})(argument1, argument2, ...);
```

the function inside the parenthese can be general, anonymous or arrow function.

These functios are executed only once and are often used to create a new scope to [avoid polluting the global scope](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function#avoid_polluting_the_global_namespace_in_script_code).

### Example

```javascript
(function (name) {
  console.log("Hello, " + name + "!");
})("Alice"); // Hello, Alice!
```

### 5. `Callback Functions`

A callback function is a function that is passed as an argument to another function.

```javascript
// syntax
function higherOrderFunction(callback) {
  // code to be executed
  callback();
}
```

### Example

```javascript
function greet(name, callback) {
  console.log("Hello, " + name + "!");
  callback();
}
function sayGoodbye() {
  console.log("Goodbye!");
}
greet("Alice", sayGoodbye);
// Output:
// Hello, Alice!
// Goodbye!
```

### 6. `Higher-Order Functions`

A higher-order function is a function that takes another function ( callback ) as an argument or returns a function as its result.

```javascript
// syntax
function higherOrderFunction(callback) {
  // code to be executed
  callback();
}
// or
function higherOrderFunction() {
  return function () {
    // code to be executed
  };
}
```

### Example

```javascript
function repeat(n, action) {
  for (let i = 0; i < n; i++) {
    action(i);
  }
}
repeat(3, console.log);
// Output:
// 0 1 2
// or
function createGreeter(name) {
  return function () {
    console.log("Hello, " + name + "!");
  };
}
let greetAlice = createGreeter("Alice");
greetAlice(); // Hello, Alice!
```
