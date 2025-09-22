# OPERATORS

In JavaScript, operators are special symbols or keywords that perform operations on one or more operands (values or variables) and return a result.

## Types of Operators

JavaScript provides a variety of operators, which can be categorized as follows:

1. **Assignment Operators**

2. **Comparison Operators**

3. **Arithmetic Operators**

4. **Bitwise Operators**

5. **Logical Operators**

6. **BigInt Operators**

7. **String Operators**

8. **Conditional (Ternary) Operator**

9. **Comma Operator**

10. **Unary Operators**

11. **Relational Operators**

### 1. Assignment Operators

---

Assignment operators are used to assign values to variables. The most common assignment operator is the equal sign (`=`).

```javascript
let x = 10; // Assigns the value 10 to variable x
```

we also have compount assignment operators also know as `shorthand` operators

| Operator | Example   | Equivalent to | operation      |
| -------- | --------- | ------------- | -------------- |
| `=`      | `x = 5`   | `x = 5`       | Assignment     |
| `+=`     | `x += 5`  | `x = x + 5`   | Addition       |
| `-=`     | `x -= 5`  | `x = x - 5`   | Subtraction    |
| `*=`     | `x *= 5`  | `x = x * 5`   | Multiplication |
| `/=`     | `x /= 5`  | `x = x / 5`   | Division       |
| `%=`     | `x %= 5`  | `x = x % 5`   | Modulus        |
| `**=`    | `x **= 5` | `x = x ** 5`  | Exponentiation |
| `<<=`    | `x <<= 5` | `x = x << 5`  | Left Shift     |
| `>>=`    | `x >>= 5` | `x = x >> 5`  | Right Shift    |

[more on shorthand operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_operators#assignment_operators)

### 2. Comparison Operators

---

Comparison operators are used to compare two values and returns a boolean result (`true` or `false`).

| Operator | Description              | Example     | Result  |
| -------- | ------------------------ | ----------- | ------- |
| `==`     | Equal to                 | `5 == '5'`  | `true`  |
| `===`    | Strict equal to          | `5 === '5'` | `false` |
| `!=`     | Not equal to             | `5 != '5'`  | `false` |
| `!==`    | Strict not equal to      | `5 !== '5'` | `true`  |
| `>`      | Greater than             | `5 > 3`     | `true`  |
| `<`      | Less than                | `5 < 3`     | `false` |
| `>=`     | Greater than or equal to | `5 >= 5`    | `true`  |
| `<=`     | Less than or equal to    | `5 <= 3`    | `false` |

### 3. Arithmetic Operators

---

Arithmetic operators are used to perform mathematical operations on numerical values.

| Operator | Description    | Example  | Result                   |
| -------- | -------------- | -------- | ------------------------ |
| `+`      | Addition       | `5 + 3`  | `8`                      |
| `-`      | Subtraction    | `5 - 3`  | `2`                      |
| `*`      | Multiplication | `5 * 3`  | `15`                     |
| `/`      | Division       | `5 / 2`  | `2.5`                    |
| `%`      | Modulus        | `5 % 2`  | `1`                      |
| `**`     | Exponentiation | `5 ** 2` | `25`                     |
| `++`     | Increment      | `x++`    | Increases `x` by 1       |
| `--`     | Decrement      | `x--`    | Decreases `x` by 1       |
| `-`      | Unary negation | `-x`     | Negates `x`              |
| `+`      | Unary plus     | `+x`     | Converts `x` to a number |

### 4. Bitwise Operators

---

Bitwise operators perform operations on the binary representations of numbers and converts them back to decimal.

| Operator | Description                  | Example  | Result |
| -------- | ---------------------------- | -------- | ------ |
| `&`      | AND                          | `5 & 3`  | `1`    |
| `\|`     | OR                           | `5 \| 3` | `7`    |
| `^`      | XOR                          | `5 ^ 3`  | `6`    |
| `~`      | NOT                          | `~5`     | `-6`   |
| `<<`     | Left shift                   | `5 << 1` | `10`   |
| `>>`     | Sign-propagating right shift | `5 >> 1` | `2`    |

### 5. Logical Operators

---

Logical operators are used with boolean values to perform logical operations.

| Operator | Description | Example           | Result  |
| -------- | ----------- | ----------------- | ------- |
| `&&`     | AND         | `true && false`   | `false` |
| `\|\|`   | OR          | `true \|\| false` | `true`  |
| `!`      | NOT         | `!true`           | `false` |

### 6. [BigInt Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_operators#bigint_operators)

---

### 7. String Operators

---

String operators are used to concatenate (combine) strings.

| Operator | Description              | Example                | Result                 |
| -------- | ------------------------ | ---------------------- | ---------------------- |
| `+`      | Concatenation            | `'Hello, ' + 'World!'` | `'Hello, World!'`      |
| `+=`     | Concatenation assignment | `str += '!'`           | Appends `'!'` to `str` |

### 8. Conditional (Ternary) Operator

---

The conditional (ternary) operator is a shorthand for the `if` statement. It takes three operands and evaluates a condition, returning one of two values based on the result.

| Operator | Description           | Example                     | Result                                                               |
| -------- | --------------------- | --------------------------- | -------------------------------------------------------------------- |
| `? :`    | Conditional (ternary) | `condition ? expr1 : expr2` | Returns `expr1` if `condition` is truthy, otherwise returns `expr2`. |

```javascript
let age = 18;
let canVote = age >= 18 ? "Yes" : "No"; // canVote will be 'Yes'
```

### 9. Comma Operator

---

The comma operator (`,`) allows you to evaluate multiple expressions, returning the value of the last expression.

| Operator | Description | Example              | Result           |
| -------- | ----------- | -------------------- | ---------------- |
| `,`      | Comma       | `let x = (1, 2, 3);` | `x` will be `3`. |

```javascript
let x = (1, 2, 3);
// x will be 3
```

### 10. Unary Operators

---

Unary operators operate on a single operand to produce a new value.

| Operator | Description           | Example           | Result               |
| -------- | --------------------- | ----------------- | -------------------- |
| `typeof` | Type of operand       | `typeof 5`        | `'number'            |
| `void`   | Discards return value | `void 0`          | `undefined`          |
| `delete` | Deletes a property    | `delete obj.prop` | `true` if successful |
| `++`     | Increment             | `x++`             | Increases `x` by 1   |
| `--`     | Decrement             | `x--`             | Decreases `x` by 1   |

### 11. Relational Operators

---

Relational operators are used to compare two values and determine their relative order. Results are returned as boolean values (`true` or `false`).

| Operator     | Description         | Example                | Result                                    |
| ------------ | ------------------- | ---------------------- | ----------------------------------------- |
| `in`         | Property in object  | `'prop' in obj`        | `true` if `obj` has property `prop`       |
| `instanceof` | Instance of a class | `obj instanceof Class` | `true` if `obj` is an instance of `Class` |

### NOTES:

- Both `relational` and `comparison`, and somtimes they are combined together as `relational operators` but in detail they are different.
- `comparison` operators are used to compare two values (equal, greater than, less than, etc.) and return a boolean result.
- `relational` operators are used to determine the relationship between two values (like checking if a property exists in an object or if an object is an instance of a class).
- some operators can be classified under multiple categories, ex: `++` can be both `arithmetic` and `unary` operator. and `+` can be both `arithmetic` and `string` operator.
