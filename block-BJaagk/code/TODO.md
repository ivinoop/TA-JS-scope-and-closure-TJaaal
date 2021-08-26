1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

// Your code goes here
// Type 1
let percentage = function (marks, total) {
  return (marks * 100) / total;
}
// Type 2
let percentage = (marks,total) => {
  return (marks * 100) / total;
}
```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}
// Function Declaration
```

```js
let percentage = function percentage(marks, total) {
  return (marks * 100) / total;
};
// Function Expression
```

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
};
// Function Expression
```

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
};
// Function Expression
```

```js
let percentage = (marks, total) => (marks * 100) / total;
//Funtion Expression with Arrow function
```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.

- Function definition is writing what we want the function to do. Function Expression is equating the definition into a result / value. 

```js
// Function Expression example
let result = function add (a,b) {
  return a + b;
}
```

4. Why is a function call an expression in JavaScript?

- Since calling a function results in a value, a function call is also considered an expression.

5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3); // VALID
five = add; // VALID
five = five(10, 11); // VALID
five = function () {
  return 'Hello';
}; // VALID
```

6. What is the difference between function definition and function call? Explain with an example.

- Function Definition is where we define the behaviour of a function and write instructions on how the function should be carried out. Function Call is when the defined function is executed. 

7. What is the similarities between function definition and function call?

- Both function defintion and function call are expressions. 

8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log('Hello World!');
}

hello.user = 'Sam'; // Valid
```

9. What is higher order function explain with an example.

- A function that accepts a function definition as an argument is called a Higher Order Function

```js
// HoF Example
const numbers = [1,2,3,4,5];

numbers.forEach((number)=> console.log(number * 2));
// forEach() is a HoF that applies the logic of multiplying each number in the array by 2
```

10. Explain what is callback function. Why you can pass a function inside a function?

- A function passed as an argument inside another function is called a callback function. This callback function is invoked by another outer function to define and / or complete a set of instructions. 

- We can pass a function inside another function since a function is also an expression in JS.