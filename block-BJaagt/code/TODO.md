Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

Example:

```js
function hello() {
  var username = 'Arya';
}
console.log(username); // ReferenceError: username is not defined
```

In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable is inside the function named `hello` and we can't access the variable defined inside a function from outside.

The above code will throw an error `Reference Error username is not defined`.

2. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
{
  const username = 'Arya';
}
console.log(useranme); // ReferenceError: username is not defined
```

In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable is inside a block, i.e., an unnamed object, and we can't access the variable from outside.

The above code will throw an error `Reference Error username is not defined`.

3. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  let username = 'Arya';
}
console.log(useranme); // output
```

In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable is inside a block, i.e., an `if` statement, and we can't access the variable from outside.

The above code will throw an error `Reference Error username is not defined`.

4. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  var username = 'Arya';
}
console.log(useranme); // Arya
```

In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. But the variable is declared with `var` so it can be accessed from outside the block as well.

The above code will return `Arya` as output.

5. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
if (true) {
  var username = 'Arya';
}
console.log(useranme); // Identifier 'username' has already been declared
```

Since `username` is already declared once with `let`, it cannot be declared again with `var`. `var` declarations are global scoped, so even though it is declared inside an `if` block, it acts as a redeclaration of the same variable. 

6. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
if (true) {
  let username = 'Arya';
}
console.log(useranme); // John
```

Here, the variable is decalared both times with `let` but the scope is localised to their respective blocks. Hence the output in this case is John, since the global variable value is being called. 

7. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
function sayHello() {
  let username = 'Arya';
}
sayHello();
console.log(username); // John
```

Here, the username inside the function scope is localised to the function, and the function execution context is deleted as soon as the function execution is finished. So, the console.log() would return the value of global `username` variable, which is `John`.

8. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (var i = 0; i < 10; i++) {
  console.log(i, 'First'); // 0 to 9 with the suffix 'First'
}
console.log(i, 'Second'); // 10 "Second"
```

Here, the variable `i` is declared with `var` so the scope is global. Hence both `console.log()` statements are able to access `i` variable.

9. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (let i = 0; i < 10; i++) {
  console.log(i, 'First'); // output
}
console.log(i, 'Second'); // ReferenceError: i is not defined
```

Since `i` is declated with `let`, its scope remains localised the `for` loop. Hence the second `console.log()` throws an error.


