# Data Types

According to [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures), JavaScript provides different data types to hold different types of values. There are two types of data types in JavaScript:

## 1. **Primitive Data Types**:

These are the most basic data types in JavaScript, these are `immutable`. There are `7` Primitive Values:

- **`null`**: Represents the intentional absence of any object.\
  It has only one value: `null`.

  ```javascript
  let emptyValue = null;
  console.log(emptyValue); // null
  ```

- **`undefined`**: Its is the absence of a value. While `null` indicates the absence of an object, javascripts defaults to `undefined` when thier is no value.\
  It has only one value : `undefined`.

  ```javascript
  let notAssigned;
  console.log(notAssigned); // undefined
  ```

- **`boolean`**: Represents a logical entity and can have two values: `true` and `false`.

  ```javascript
  let isJavaScriptFun = true;
  let isFishTasty = false;
  console.log(isJavaScriptFun); // true
  console.log(isFishTasty); // false
  ```

- **`number`**: Represents both integer and floating-point numbers.\
  Example: `42`, `3.14`, `-7`, `0`.\
  `NaN` (Not-a-Number) is also considered a number type.

  ```javascript
  let integerNum = 42;
  let floatNum = 3.14;
  let negativeNum = -7;
  let notANumber = NaN;
  ```

- **`bigint`**: Represents integers with arbitrary precision. It is used for very large integers that exceed the limits of the `number` type.\
  Example:

  ```javascript
  let bigIntNum = 9007199254740991n;
  let bigIntNum2 = 1234567890123456789012345678901234567890n;
  ```

- **`string`**: Represents a sequence of characters.\
  Characters are represented using `UTF-16` encoding`.

  ```javascript
  let greeting = "Hello, world!";
  console.log(greeting); // Hello, world!
  ```

- **`symbol`**: Represents a unique identifier. Symbols are often used as keys in objects to avoid name collisions.\
  Example: `Symbol('description')`.

  ```javascript
  let sym1 = Symbol("uniqueKey");
  let sym2 = Symbol("uniqueKey");
  console.log(sym1 === sym2); // false
  let obj = {
    [sym1]: "value1",
    [sym2]: "value2",
  };
  console.log(obj[sym1]); // value1
  console.log(obj[sym2]); // value2
  ```

## 2. **Non-Primitive Data Types / Objects**:

In CS, object is a value in the memory. Objects in JavaSripts are the only `mutable` values.\
 Objects are collections of properties, where each property is a key-value pair.\
 The key is always a `string` or a `symbol`, and the value can be any data type, including other objects.\
 Example:

```javascript
const person = {
  name: "Alice",
  age: 30,
  address: {
    city: "Wonderland",
    zip: "12345",
  },
};
```

Many other non-primitive data types are built on top of objects, such as:

- `Arrays`
- `Functions`
- `Dates` and `Temporal`
- `Regular Expressions`
- `Maps`
- `Sets`
- etc......

### NOTES:

- we can use the `typeof` operator to determine the data type of a value.

  ```javascript
  console.log(typeof 42); // "number"
  console.log(typeof "Hello"); // "string"
  ```

- even though we can use `properties` and `methods` on primitive values like strings and numbers, they are not objects. JavaScript temporarily wraps them in their corresponding object types (like `String` or `Number`) when we access properties or methods.
