1. Write a function that accepts a callback function and return another function. But the function should only be called once.

```js
function once(cb) {
  let isCalled = false;
  return function() {
    if(isCalled === false) {
      cb();
      isCalled = true;
    }
  };
}

// TEST
function sayHello() {
  alert('Call me once!');
}
let log = once(sayHello);
log(); // alert message "You can only call me once!"
log(); // return undefined (can't be called twice)
```

2. Change the above function in such a way that the function accepts two parameter a callback function and parameter for the callback function. When calling the function pass the parameters.

```js
function once(cb, param) {
  let isCalled = false;
  return function() {
    if(isCalled === false) {
      cb(param);
      isCalled = true;
    }
  };
}

// TEST
let log = once(console.log, 'Hello Console');
log(); // log message "Hello Console"
log(); // return undefined (can't be called twice)
```

3. Change the above function in such a way that it can accept `n` number of parameters for the callback function.

**For handling `n` number of parameter use `rest` parameters `...` or predefined arguments variable present in every function declaration.**

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters

```js
function once(cb, ...params) {
  let isCalled = false;
  return function() {
    if(isCalled === false) {
      cb(...params);
      isCalled = true;
    } else {
      alert("You can't call the  function again!");
    }
  };
}

// TEST
let log = once(console.log, 'Message one', 'Message Two');
log(); // log message "Message One Message Two"
log(); // return undefined (can't be called twice)
```

4. Create a new function `nTimes` whose 1st parameter is a callback function, 2nd parameter is the number of times the function should be called and 3rd ... nth parameter should be passed to the callback function.

```js
function nTimes(cb, times, ...rest) {
  let numberOfTimesCalled = 0;
  return function() {
    if(numberOfTimesCalled >= times) {
      alert(`You cannot call this function more than ${times} times!`);
    } else {
      cb(...rest);
      numberOfTimesCalled += 1;
    }
  };
}

// TEST
let log = (msg) => console.log(msg);
let logThreeTimes = nTimes(log, 3, 'Hello Arya');
logThreeTimes(); // log message "Hello Arya" (1)
logThreeTimes(); // log message "Hello Arya" (2)
logThreeTimes(); // log message "Hello Arya" (3)
log(); // return undefined (can't be called)
```
