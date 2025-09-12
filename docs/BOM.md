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

**Example Usage**

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
