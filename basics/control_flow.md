# Control Flow Statements

Control flow refers to the order in which individual statements, instructions, or function calls are executed or evaluated in a programming language. In JavaScript, control flow is primarily managed through the use of conditional statements and loops.

Control flow statements can be categorized as follows:

1. Conditional Statements
2. Looping Statements
3. Jump Statements

## 1. Conditional Statements

Conditional statements allow you to execute different blocks of code based on certain conditions. the most common conditional statements in JavaScript are:

### 1. `if` Statement

The `if` statement executes a block of code if a specified condition is true.

```javascript
let age = 18;
if (age >= 18) {
  console.log("You are an adult.");
}
```

### 2. `if...else` Statement

The `if...else` statement executes one block of code if a specified condition is true, and another block if it is false.

```javascript
let age = 16;
if (age >= 18) {
  console.log("You are an adult.");
} else {
  console.log("You are a minor.");
}
```

### 3. `if...else if...else` Statement

The `if...else if...else` statement allows you to test multiple conditions.

```javascript
let score = 85;
if (score >= 90) {
  console.log("Grade: A");
} else if (score >= 80) {
  console.log("Grade: B");
} else if (score >= 70) {
  console.log("Grade: C");
} else {
  console.log("Grade: F");
}
```

### 4. `switch` Statement

The `switch` statement evaluates an expression and executes code based on matching case values.

```javascript
let day = 3;
switch (day) {
  case 1:
    console.log("Monday");
    break;
  case 2:
    console.log("Tuesday");
    break;
  case 3:
    console.log("Wednesday");
    break;
  case 4:
    console.log("Thursday");
    break;
  case 5:
    console.log("Friday");
    break;
  case 6:
    console.log("Saturday");
    break;
  case 7:
    console.log("Sunday");
    break;
  default:
    console.log("Invalid day");
}
```

## 2. `Looping` Statements

Looping statements allow you to execute a block of code multiple times. The most common looping statements in JavaScript are:

1. `for` loop
2. `while` loop
3. `do...while` loop

### 1. for Loop

The `for` loop is used to execute a block of code a specific number of times. `for` is typically used when the number of iterations is known beforehand.

```javascript
// syntax
for (initialization; condition; increment) {
  // code to be executed
}
for (;;) {
  // infinite loop
}
```

```javascript
// Example
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

### 2. `while` Loop

The `while` loop executes a block of code as long as a specified condition is true. `while` is typically used when the number of iterations is not known beforehand.

```javascript
// syntax
while (condition) {
  // code to be executed
}
```

```javascript
// Example
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

### 3. `do...while` Loop

The `do...while` loop is similar to the `while` loop, but it guarantees that the block of code will be executed at least once before checking the condition.

```javascript
do {
  // code to be executed
} while (condition);
```

```javascript
// Example
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5);
```

## 3. Jump Statements

Jump statements are used to alter the flow of control by jumping to another part of the code. There are two main jump statements in JavaScript:

### 1. `break` statement

The `break` statement is used to exit a loop or a switch statement prematurely.

```javascript
// Example
for (let i = 0; i < 5; i++) {
  if (i === 3) {
    break;
  }
  console.log(i);
}
```

### 2. `continue` statement

The `continue` statement is used to skip the current iteration of a loop and proceed to the next iteration.

```javascript
// Example
for (let i = 0; i < 5; i++) {
  if (i === 2) {
    continue;
  }
  console.log(i);
}
```
