# STRINGS

## What is string ?

A string is a sequence of characters, typically used to represent text.

A javascript string is zero or more character written inside quotes. ( it can be single or double quotes )

**Example:**

```javascript
let a = "Hello World"; // double quotes
let b = "Hello World"; // single quotes
```

**Quotes inside string** :<br>
we can use single quotes inside double quotes and vice versa.

```javascript
let a = "Hello 'World'";
// Output: Hello 'World'
```

\
`note:`

- `Indexes` in strings start from 0 and -1 from backwards.
- `Escape Characters`: Because strings must be written within quotes, JavaScript will misunderstand quotes, we use `\` to escape quotes

**Template Strings**:<br>
Template strings are enclosed by backticks (`` ` ``). This allows quotes and variables to be included in the string.\
also known as `interpolated` strings.

```javascript
let name = "Raj";
console.log(`Hello "${name}"`);
// Output: Hello "Raj"
```

**String Length**\
Length is a build-in property of string that returns the number of characters in a string.

```javascript
let a = "Hello World";
console.log(a.length); // Output: 11
```

## String Methods

String methods are built-in functions that can be used to manipulate and perform operations on strings.

1. `indexOf()`, `lastIndexOf()`, `includes()`:

   - `indexOf(substring)` : returns the index of the first occurrence of the specified substring. If not found, it returns -1.

   - `lastIndexOf(substring)` : returns the index of the last occurrence of the specified substring. If not found, it returns -1.

   - `includes(substring)` : checks if a string contains a specified substring and returns true or false.

   ```javascript
   let a = "Hello World";

   console.log(a.indexOf("o"));
   // Output: 4

   console.log(a.indexOf("x"));
   // Output: -1

   console.log(a.lastIndexOf("o"));

   // Output: 7

   console.log(a.includes("World"));
   // Output: true

   console.log(a.includes("world"));
   // Output: false
   ```

2. `toUpperCase()` : Converts a string to uppercase letters.

   ```javascript
   let a = "Hello World";
   console.log(a.toUpperCase());
   // Output: HELLO WORLD
   ```

3. `toLowerCase()` : Converts a string to lowercase letters.

   ```javascript
   let a = "Hello World";
   console.log(a.toLowerCase());
   // Output: hello world
   ```

4. `charAt()`: Returns the character at a specified index in a string.

   ```javascript
   let a = "Hello World";
   console.log(a.charAt(0));
   // Output: H
   ```

5. `charCodeAt()`: Returns the **Unicode** (UTF-16) of the character at a specified index in a string.

   ```javascript
   let a = "Hello World";
   console.log(a.charCodeAt(0));
   // Output: 72
   ```

6. `startsWith()`: Checks if a string starts with a specified substring. we can also provide a position / **Index** to start the search as a second argument.

   ```javascript
   let a = "Hello World";
   console.log(a.startsWith("Hello"));
   // Output: true

   console.log(a.startsWith("World", 6));
   // Output: true

   console.log(a.startsWith("World", 5));
   // Output: false
   ```

7. `endsWith()`: Checks if a string ends with a specified substring. we can also provide a **length** to consider as a second argument.

   ```javascript
   let a = "Hello World";
   console.log(a.endsWith("World"));
   // Output: true

   console.log(a.endsWith("Hello", 5));
   // Output: true

   console.log(a.endsWith("Hello", 6));
   // Output: false
   ```

8. `substring()` , `substr()`, `slice()` : These methods are used to extract a part of a string.

   - `substring(startIndex, endIndex)` : extracts characters from startIndex to endIndex (not including endIndex). does not support negative indices.

   - `substr(startIndex, length)` : extracts characters from startIndex for the specified length.

   - `slice(startIndex, endIndex)` : extracts characters from startIndex to endIndex (not including endIndex). It also supports negative indices.

   ```javascript
   let a = "Hello World";

   console.log(a.substring(0, 5));
   // Output: Hello

   console.log(a.substr(0, 7));
   // Output: Hello W

   console.log(a.slice(0, 5));
   // Output: Hello

   console.log(a.slice(-5));
   // Output: World
   ```
