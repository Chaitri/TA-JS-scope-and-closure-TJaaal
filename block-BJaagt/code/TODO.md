Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

Example:

```js
function hello() {
  var username = 'Arya';
}
console.log(username); // output
```

In above code we are looking for the variable named `usename`. There is no variable named `username` in the global scope. The variable is inside the function named `hello` and we can't access the variable defined inside a function from outside.

The above code will throw an error `Reference Error username is not defined`.

2. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
{
  const username = 'Arya';
}
console.log(username); // Error: ReferenceError: username is not defined
```

Above, it is looking for variable `username`. But this variable is defined only within a block scope as a `const` , and hence cannot be accessed from global scope. Error will be thrown : ReferenceError: username is not defined.


3. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  let username = 'Arya';
}
console.log(username); //  Error: ReferenceError: username is not defined
```

Above, it is looking for variable `username`. But this variable is defined only within a block scope as a `let`, which is executed as it is defined within a `true conditional check`. Hence , it cannot be accessed from global scope. Error will be thrown : ReferenceError: username is not defined.


4. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  var username = 'Arya';
}
console.log(username); // Arya
```
Here, we can access `username` within a block scope, as it defined as `var`. Output will be `Arya`.


5. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
if (true) {
  var username = 'Arya';
}
console.log(username); // Identifier 'username' has already been declared
```
Error will be thrown as `username` has already been declared using `let` and hence will not allow for re-declaring it as `var`. Error: `Identifier 'username' has already been declared`

6. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
if (true) {
  let username = 'Arya';
}
console.log(username); // John
```

Variable `username` is already declared in global scope, and hence it will be accessed with value `John`. The variable being re-declared as `let` in block has no effect.


7. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
function sayHello() {
  let username = 'Arya';
}
sayHello();
console.log(username); // output
```

`username` will be accessed through the global scope declaration. Even though, sayHello() was called, it manipulates only the variable defined within the function scope.

8. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (var i = 0; i < 10; i++) {
  console.log(i, 'First'); // output
}
console.log(i, 'Second'); // output
```

`i` is first initialized as `var` with value 0 till 9 in for loop. This gives output as `0 First, 1 First, .... 9 First`. Once for loop is executed, i has a value of 10 which gets printed out as `10 Second`.


9. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (let i = 0; i < 10; i++) {
  console.log(i, 'First'); // output
}
console.log(i, 'Second'); // output
```
`i` is first initialized as `let` with value 0 till 9 in for loop. This gives output as `0 First, 1 First, .... 9 First`. Once for loop is executed, i is also erased as it was created as `let` only in the scope of the for loop. Hence, outside the loop, i is not defined, and we get Error: i is not defined.
