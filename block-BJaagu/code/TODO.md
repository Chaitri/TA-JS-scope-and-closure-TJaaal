Find the output of the code snippets below:

```js
console.log(numA + numB); //NaN
var numA = 21,
  numB = 30;
```

here, numA and numB will be undefined by the time `console.log` executes. And result of  `undefined + undefined` is `NaN`.

Find the output of the code snippets below:

```js
console.log(numA + numB); //numA is not defined error
let numA = 21,
  numB = 30;
```

As variables are created with `let` keyword, these are not initialized to any value, and hence, cannot be used in `console.log()` statement.

Find the output of the code snippets below:

```js
let numA = 21,
  numB = 30;
console.log(numA + numB); //51
```

As variables have been declared and initialized by the time `console.log` runs, we get a valid output of - 51.

Find the output of the code snippets below:

```js
console.log(sayHello()); // Hello
function sayHello() {
  console.log("Hey");
}
function sayHello() {
  console.log("Hello");
}
```

The second function defintion of `sayHello()` will overwrite the first one, and hence output will be `Hello` when this function is called.

Find the output of the code snippets below:

```js
let username = "Tyrion";
sayHello(); // Tyrion
function sayHello() {
  console.log(username);
}
```

When function is called, username is already initialized to Tyrion.

Find the output of the code snippets below:

```js
sayHello(); // username is not defined
let username = "Tyrion";
function sayHello() {
  console.log(username);
}
```

Variable has not yet been initialized, only created, when `sayHello()` is executed.

Find the output of the code snippets below:

```js
let username = "Tyrion";
sayHello(); // sayHello is not defined
let sayHello = () => {
  console.log(username);
};
```

Function has not yet been initialized, only created, when `sayHello()` is executed.

Find the output of the code snippets below:

```js
sayHello(); // sayHello is not defined
let username = "Tyrion";
let sayHello = () => {
  console.log(username);
};
```

Both the variable `username` and the function `sayHello` has not been initialized. But since, sayHello is called first, an error for this function is thrown.

Find the output of the code snippets below:

```js
sayHello(); // sayHello is not defined
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
};
```
Function has not yet been initialized, only created, when `sayHello()` is executed.


Find the output of the code snippets below:

```js
var username = "Tyrion";
sayHello(); // sayHello is not defined
let sayHello = () => {
  console.log(username);
};
```

Function has not yet been initialized, only created, when `sayHello()` is executed.


Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
  var username = "John";
};
sayHello(); // undefined
```
Inside the function, `username` is used before it has been initialized to value John. As it was created with `var`, it was initially initialized to `undefined` and thus it shows in output as well.

Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  var username = "John";
  console.log(username);
};
sayHello(); // John
```

Variable in function is accessed instead of the one in global scope, and output is John.

Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
  let username = "John";
};
sayHello(); // Cannot access 'username' before initialization
```

As the variable `username` has already been created within function, it will not look in global scope for it. But, this variable has not yet been initialized, and hence error is shown. 