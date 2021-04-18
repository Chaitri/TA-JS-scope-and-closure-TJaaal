1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

// Your code goes here

let funcPercentage = function (marks, total) {
  return (marks * 100) / total;
}

let anotherFuncPercentage = (marks, total) => (marks * 100) / total;

```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}
// Your answer

Function Declaration

```

```js
let percentage = function percentage(marks, total) {
  return (marks * 100) / total;
};

Function Expression

```

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
};

Function Expression

```

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
};

Function Expression

```

```js
let percentage = (marks, total) => (marks * 100) / total;

Function Expression

```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.

Functions are treated as objects in Javascript. Hence, we can assign functions to variables. When we do this, we create function expressions, like so:

```js

let printName = function (name) {
  console.log(name);
}

```

4. Why is a function call an expression in JavaScript?

Function call is an expression, as when the function executes, it will ultimately return a value. Even if explicit return is not defined in the function, a function will return the default value of undefined. 

5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3); // Valid, as return value 5 is stored in variable
five = add; // Valid, as function definition is asssigned to variable
five = five(10, 11); // Valid, as it first evaluates the function call, then assigns the value back to varibale, thus over-riding the previous function defintion stored in it.
five = function () {
  return 'Hello';
}; // Valid, as we are over-writing the previous value of 21 with a new function defintion
```

6. What is the difference between function definition and function call? Explain with an example.

Function defintion just contains the statements which are meant to be executed, whereas a function call actually executes these statements and run the function. Ex:

Function defintion:
```js
function add( num1 , num2) {
  return num1 +  num2;
}

```

Function call:
```js
add(1,2); // returns 3

```

7. What is the similarities between function definition and function call?

None, as function defition is used to define the statements , whereas a function call executes these statements.

8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log('Hello World!');
}

hello.user = 'Sam'; // Valid, as functions are objects, and we can assign a prorperty to an object.
```

9. What is higher order function explain with an example.

Higher order function, is a function which accepts a function defintion as a parameter, or it returns a function definition.

```js

function isOdd(n) {
  return n % 2 !== 0;
}

function filterNums(arr, cb) { // higher order function, accepts isOdd as a parameter
  let result = arr.filter( num => cb(num));
  return result;
}

filterNums([2,3,5,6,7], isOdd);

```

10. Explain what is callback function. Why you can pass a function inside a function?

A callback function is one which is sent to a higher order function.
Since functions are objects, it's possible to pass them as arguments to other functions or have them returned as well.