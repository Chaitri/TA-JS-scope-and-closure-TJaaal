1. What does thread of execution means in JavaScript?

It means that when a JavaScript code snippet is executed, JS engine creates a Global context environment, and executes each statement one by one.

2. Where the JavaScript code gets executed?

In Global Execution Context

3. What does context means in Global Execution Context?

It is the environment in which the code is executed.

4. When do you create a global execution context.

It is created once at the start, when a program is first executed.

5. Execution context consists of what all things?

It consists of the execution block, and a memory section.

6. What are the different types of execution context?

There is Global Execution Context, and Function Execution Context.

7. When global and function execution context gets created?

Global execution context - gets created when the program is first executed.
Function execution context - gets created whenever a function is called, and is removed once funtion execution is over.

8. Function execution gets created during function execution or while declaring a function.

When function is executed.

9. Create a execution context diagram of the following code on your notebook. Take a screenshot/photo and store it in the folder named `img`. Use `![](./img/image-name.png)` to display it here.



```js
var user = "Arya";

function sayHello(){
  return `Hello ${user}`;
}

var userMsg = sayHello(user);
```

<!-- Put your image here -->

<!-- ![](./img/image-name.jpg) -->

![img1](./img/img1.png)

```js
var marks = 400;
var total = 500;

function getPercentage(amount, totalAmount){
  return (amount * 100) / totalAmount;
}

var percentageMarks = getPercentage(marks, total);
var percentageProfit = getPercentage(400, 200);
```

<!-- Put your image here -->

<!-- ![](./img/image-name.jpg) -->

![img2](./img/img2.png)



```js
var age = 21;

function customeMessage(userAge){
  if(userAge > 18){
    return `You are an adult`;
  }else {
    return `You are a kid`;
  }
}

var whoAmI = customeMessage(age);
var whoAmIAgain = customeMessage(12);
```

<!-- Put your image here -->

<!-- ![](./img/image-name.jpg) -->

![img3](./img/img3.png)