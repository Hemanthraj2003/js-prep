# Keywords and Variables

- **Keywords**: Reserved words in JavaScript that have special meaning and cannot be used as identifiers (e.g., `var`, `let`, `const`, `if`, `else`, `function`, etc.).

- **Variables**: Containers for storing data values. In JavaScript, you can declare variables using `var`, `let`, or `const`.

## Variable Declaration

- **var**: The oldest way to declare a variable. It has function scope and can be re-declared and updated.

  ```javascript
  var name = "John";
  name = "Doe"; // Updated
  var name = "Smith"; // Re-declared
  ```

- **let**: Introduced in ES6, it has block scope and can be updated but not re-declared within the same scope.

  ```javascript
  let age = 25;
  age = 26; // Updated
  // let age = 30; // Error: Cannot re-declare
  ```

- **const**: Also introduced in ES6, it has block scope and cannot be updated or re-declared. It must be initialized at the time of declaration.

  ```javascript
  const pi = 3.14;
  // pi = 3.14159; // Error: Cannot update
  // const pi = 3.14159; // Error: Cannot re-declare
  ```

### NOTES

- variables declared with `var` are hoisted to the top of their scope and initialized with `undefined`.

  - **Example**:

    ```javascript
    console.log(x); // undefined
    var x = 5;
    console.log(x); // 5
    ```

- variables declared with `let` and `const` are also hoisted, but they are not initialized. Accessing them before the declaration results in a `ReferenceError`.

- `const` does not make the variable immutable. If the variable holds an object or array, the contents of the object or array can still be modified.

- If we do not mention declaration keywords (`var`, `let`, or `const`) while declaring a variable, it becomes a global variable (not recommended).

  - **Example**:

    ```javascript
    function myFunction() {
      x = 10; // Implicitly creates a global variable
    }
    myFunction();
    console.log(x); // 10
    ```
