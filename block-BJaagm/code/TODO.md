1. What does thread of execution means in JavaScript?

- Thread of execution means a single unit of code that is being executed by the JavaScript engine. Each function / block of code is a thread in JS.

2. Where the JavaScript code gets executed?

- JS code gets executed in the JS Engine, under a concept called Execution Context.

3. What does context means in Global Execution Context?

- Context is an environment where code is executed.

4. When do you create a global execution context.

- Global Execution Context is created by the JS Engine as soon as the program starts executing. 

5. Execution context consists of what all things?

- Execution context consists of a memory section where data is stored, and another section where code is executed. 

6. What are the different types of execution context?

- Global Execution Context
- Function Execution Context

7. When global and function execution context gets created?

- GEC is created by the JS Engine immediately when a program is executed. FEC is run whenever a function is executed.

8. Function execution gets created during function execution or while declaring a function.

- During function execution. It gets deleted as soon as a value is returned from it. 


9. Create a execution context diagram of the following code on your notebook. Take a screenshot/photo and store it in the folder named `img`. Use `![](./img/image-name.png)` to display it here.



```js
var user = "Arya";

function sayHello(){
  return `Hello ${user}`;
}

var userMsg = sayHello(user);
```

<!-- Put your image here -->

![](/img/img1.png)



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

![](./img/image-name.jpg)



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

![](./img/image-name.jpg)