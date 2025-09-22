# OBJECTS

Objects are a fundamental data structure in JavaScript that allow you to store collections of data and more complex entities.

An object is a collection of properties, and a property is an association between a key and a value (key-value pair). The value can be of any data type, including other objects. and if the value is a function, it is called a `method`.

In this section, we will discuss How to create objects, access and modify their properties, methods.

## Creating Objects

There are several ways to create objects in JavaScript:

### 1. `Object Literals or Object Initializer`:

The most common way to create an object is by using curly braces `{}` and defining key-value pairs inside.

```javascript
// syntax
let objectName = {
  key1: value1,
  key2: value2,
  // more key-value pairs
};
```

each property is defined as a key followed by a colon `:` and then the value. Properties are separated by commas.

```javascript
// Example
let person = {
  name: "Alice",
  age: 30,
  isEmployed: true,
  greet: function () {
    console.log("Hello, " + this.name);
  },
};
```

More on `this` keyword below

### 2. `Constructor Function`:

This method uses a function to create an object with properties and methods, we can use the `new` keyword to create an instance of the object (i.e., constructor function).

```javascript
// syntax
function ConstructorName(param1, param2) {
  this.key1 = param1;
  this.key2 = param2;
  // more properties and methods
}
let objectName = new ConstructorName(value1, value2);
```

#### Example

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
  this.greet = function () {
    console.log("Hello, " + this.name);
  };
}
let person1 = new Person("Alice", 30);
```

### 3. `Object() Constructor`:

You can also create an object using the built-in `Object` constructor.

```javascript
let objectName = Object({ key1: value1, key2: value2 });
```

This is same as using object literals.

### 4. `Object.create()` Method:

This method creates a new object with the specified prototype object and properties.

```javascript
let newObject = Object.create(prototypeObject, propertiesObject);
```

#### Example

```javascript
let personPrototype = {
  name: "",
  age: 0,
  greet: function () {
    console.log("Hello, " + this.name);
  },
};

let person1 = Object.create(personPrototype);
person1.name = "Alice";
person1.age = 30;
person1.greet(); // Hello, Alice
```

## Accessing and Modifying Properties

Properties are same as variables that are attached to objects.

You can access and modify object properties using dot notation or bracket notation.

### 1. Dot Notation

```javascript
console.log(person1.name); // Alice
person1.age = 31;
```

### 2. Bracket Notation

```javascript
console.log(person1["name"]); // Alice
person1["age"] = 31;
```

## Methods

Methods are functions that are properties of an object. You can define methods within an object and call them using dot or bracket notation.

```javascript
// syntax
myObject = {
    method01: function(params){
        //code
    }
    // or
    method02(params){
        //code
    }
    // This works too
}

// accessing methods
myObject.method01(args);
myObject["method02"](args);
```

### `this` Keyword

`this` is used for object reference, we use this to refer the current object.

```javascript
let person = {
  name: "Alice",
  greet: function () {
    console.log("Hello, " + this.name);
    // this refers to the current object (person)
  },
};
person.greet(); // Hello, Alice
```

### `Getter and Setter`

Getters and setters are special methods that allow you to define how to access and modify properties of an object.

we use the `get` keyword to define a getter method and the `set` keyword to define a setter method.

```javascript
let person = {
  firstName: "Alice",
  lastName: "Smith",
  get fullName() {
    return this.firstName + " " + this.lastName;
  },
  set fullName(name) {
    let parts = name.split(" ");
    this.firstName = parts[0];
    this.lastName = parts[1];
  },
};
console.log(person.fullName); // Alice Smith
person.fullName = "Bob Johnson";
console.log(person.firstName); // Bob
console.log(person.lastName); // Johnson
```
