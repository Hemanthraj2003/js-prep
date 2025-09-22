# BROWSER OBJECT MODEL (BOM)

In javascript, the Browser Object Model (BOM) refers to the objects provided by the web browser that allow interaction with the browser itself, outside of the content of a web page. The BOM includes `window` object.

- `window` object has many methods, properties and objects.\
- `window` object is the default object in the javascript.

## Window Methods:

- `alert()`: Displays an alert dialog with a specified message and an OK button.

- `confirm()`: Displays a dialog with a specified message, along with OK and Cancel buttons.\
  Returns `true` if OK is pressed, and `false` if Cancel is pressed.

- `prompt()`: Displays a dialog with a specified message, an input field, and OK and Cancel buttons.\
  Return `string` if OK is pressed, and `null` if Cancel is pressed.

### Example Usage

```javascript
let getUserName = () => {
  let userName = prompt("Enter Name:");
  if (!userName) {
    let confirmValue = confirm("Do u want to cancel?");
    confirmValue ? alert("Cancelled") : getUserName();
  } else {
    alert("Hello " + userName);
  }
};
```

## Timing Events/Functions:

- `setTimeout()`: Calls a function or evaluates an expression after a specified number of milliseconds.\
  takes 2 parameters: `function` and `time` in milliseconds.

  ```javascript
  setTimeout(() => {
    alert("Hello after 3 seconds");
  }, 3000);
  ```

- `setInterval()`: Calls the specified function at specified intervals (in milliseconds).\
  takes 2 parameters: `function` and `time` in milliseconds.

  ```javascript
  let func = () => {
    alert("Hello every 3 seconds");
  };
  setInterval(func, 3000);
  ```

- `note`: both the functions return a unique number ID.

- `clearTimeout()`: Cancels a timeout previously established by calling `setTimeout()`.\

  ```javascript
  clearTimeout(timeoutID);
  ```

- `clearInterval()`: Cancels a timed, repeating action which was previously established by a call to `setInterval()`.\
  takes 1 parameter: the `ID` of the interval to be cleared.

  ```javascript
  clearInterval(intervalID);
  ```

## EVENTS

- `onclick` - The `onclick` event occurs when the user clicks on an element.

  ```html
  <button onclick="alert('Hello World!')">Click Me!</button>
  ```

- `ondblclick` - occurs when the user double-clicks on an element.

  ```html
  <button
    onclick="alert('Hello World!')"
    ondblclick="alert('This is double-click')"
  >
    Double Click Me
  </button>
  ```

## Date and Time

The `Date` object is used to work with dates and times.

### Creating a Date Object

You can create a new date object using the `Date()` constructor.

```javascript
let currentDate = new Date();
console.log(currentDate);
// Output: "2024-06-15T10:20:30.000Z"
```

### Getting Date and Time Components

You can use various methods to get different components of the date and time.

```javascript
let currentDate = new Date();

let year = currentDate.getFullYear();
// output: 2024

let month = currentDate.getMonth();
// output: 5 (June, as months are zero-indexed)

let date = currentDate.getDate();
// output: 15

let hours = currentDate.getHours();
// output: 10

let minutes = currentDate.getMinutes();
// output: 20

let seconds = currentDate.getSeconds();
// output: 30

let day = currentDate.getDay();
// output: 6 (Saturday)
```
