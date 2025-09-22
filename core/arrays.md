# Arrays in JavaScript

Arrays are special objects used to store multiple values in a single variable. They come with built-in methods to perform various operations.

## 1. Creating Arrays

You can create an array using the Array constructor or by using array literals.

**Example using array literals:**

```js
const fruits = ["apple", "banana", "orange"];
```

**Example using the Array constructor:**

```js
const fruits = new Array("apple", "banana", "orange");
```

## 2. Accessing Array Elements

You can access array elements using their index (starting from 0).

**Example:**

```js
console.log(fruits[0]); // Output: 'apple'
```

## 3. `Array Properties`

#### `length`

The `length` property returns the number of elements in an array.

**Example:**

```js
console.log(fruits.length); // Output: 3
```

## 4. `Array Methods`

Arrays come with various built-in methods to manipulate and interact with the data.

### Common Methods ( [completeReference](https://www.w3schools.com/js/js_array_reference.asp))

---

### `push()`

> Used to add one or more elements to the end of an array and returns the new length of the array.
> **Syntax:**

```js
array.push(element1, ..., elementN);
```

**Example:**

```js
const fruits = ["apple", "banana"];
fruits.push("orange");
console.log(fruits); // Output: ['apple', 'banana', 'orange']
```

---

### `pop()`

> Used to remove the last element from an array and returns that element.

**Syntax:**

```js
array.pop();
```

**Example:**

```js
const fruits = ["apple", "banana", "orange"];
const lastFruit = fruits.pop();
console.log(lastFruit); // Output: 'orange'
console.log(fruits); // Output: ['apple', 'banana']
```

---

### `slice()`

> Used to return a shallow copy of a portion of an array into a new array object selected from start to end (end not included).
> **Syntax:**

```js
array.slice(start, end);
```

**Example:**

```js
const fruits = ["apple", "banana", "orange", "mango"];
const citrus = fruits.slice(1, 3);
console.log(citrus); // Output: ['banana', 'orange']
```

---

### `filter()`

> Used to create a new array with all elements that pass the test implemented by the provided function.

**Syntax:**

```js
array.filter(callback);
```

**Example:**

```js
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter((num) => num % 2 === 0);
console.log(evenNumbers); // Output: [2, 4]
```

---

### `map()`

> Used to create a new array by applying a function to each element of the original array.

**Syntax:**

```js
array.map(callback);
```

**Example:**

```js
const numbers = [1, 2, 3];
const doubled = numbers.map((num) => num * 2);
console.log(doubled); // Output: [2, 4, 6]
```

---

### `reduce()`

> Used to convert all array elements to a single value after performing arithmetic or other operations.

**Syntax:**

```js
array.reduce((accumulator, currentValue) => { ... }, initialValue);
```

- `initialValue` is optional.

**Example:**

```js
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce(
  (accumulator, currentValue) => accumulator + currentValue
);
console.log(sum); // Output: 10
```

---

### `sort()`

> Used to sort the elements of an array in place and return the sorted array.

- Sorts single-digit numbers correctly but not multi-digit numbers by default.
- To sort numbers correctly, provide a compare function.

**Syntax:**

```js
array.sort([compareFunction]);
```

**Example:**

```js
const numbers = [3, 1, 4, 1, 5, 9];
numbers.sort(); // sorts as strings by default
console.log(numbers); // Output: [1, 1, 3, 4, 5, 9]

// To sort numbers correctly:
numbers.sort((a, b) => a - b);
console.log(numbers); // Output: [1, 1, 3, 4, 5, 9]
```

---

### `forEach()`

> Used to execute a provided function once for each array element.
> **Syntax:**

```js
array.forEach(callback);
```

**Example:**

```js
const fruits = ["apple", "banana", "orange"];
fruits.forEach((fruit) => console.log(fruit));
// Output:
// apple
// banana
// orange
```

### `array operators`

#### Spread Operator (`...`)

> Used to expand an array into individual elements.
> **Example:**

```js
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

const combined0 = [arr1, arr2];
console.log(combined0); // Output: [[1, 2, 3], [4, 5, 6]]

const combined = [...arr1, ...arr2];
console.log(combined); // Output: [1, 2, 3, 4, 5, 6]
```

#### rest Operator (`...`)

> Used to combine multiple elements into a single array.
> **Example:**

```js
function sum(...numbers) {
  return numbers.reduce((acc, num) => acc + num, 0);
}
console.log(sum(1, 2, 3)); // Output: 6

const [a, ...num] = [1, 2, 3, 4, 5];
console.log(a); // Output: 1
console.log(num); // Output: [2, 3, 4, 5]
```

## MORE METHODS

| Method        | Description                                                                                                      |
| ------------- | ---------------------------------------------------------------------------------------------------------------- |
| `concat()`    | Merges two or more arrays and returns a new array.                                                               |
| `join()`      | Joins all elements of an array into a string.                                                                    |
| `indexOf()`   | Returns the first index at which a given element can be found in the array, or -1 if it is not present.          |
| `find()`      | Returns the value of the first element in the array that satisfies the provided testing function.                |
| `includes()`  | Determines whether an array includes a certain value among its entries, returning true or false as appropriate.  |
| `shift()`     | Removes the first element from an array and returns that element.                                                |
| `unshift()`   | Adds one or more elements to the beginning of an array and returns the new length of the array.                  |
| `splice()`    | Changes the contents of an array by removing or replacing existing elements and/or adding new elements in place. |
| `findIndex()` | Returns the index of the first element in the array that satisfies the provided testing function.                |
| `every()`     | Tests whether all elements in the array pass the test implemented by the provided function.                      |

## [Complete Reference](https://www.w3schools.com/js/js_array_reference.asp)
