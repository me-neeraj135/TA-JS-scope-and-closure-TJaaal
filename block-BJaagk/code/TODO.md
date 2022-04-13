1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

// Your code goes here
```

```js
let percentage = function myFunction(marks, total) {
  return (marks * 100) / total;
};

let percentage = function (marks, total) {
  return (marks * 100) / total;
};
let percentage = (marks, total) => (marks * 100) / 100;
```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}
// Your answer
```

```js
let percentage = (marks, total) => (marks * 100) / 100;
```

```js
let percentage = function percentage(marks, total) {
  return (marks * 100) / total;
};
```

```js
function percentage(marks,total){
  return (marks*100)total
}

```

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}
```

```js
let percentage = (marks, total) => (marks * 100) / total;
```

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
};
```

```js
function percentage(marks, total) {
  return (marks * 100) / 100;
}
```

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
};
```

```js
function percentage(marks, total) {
  return (marks * 100) / 100;
}
```

```js
let percentage = (marks, total) => (marks * 100) / total;
```

```js
function percentage(marks, total) {
  return (marks * 100) / 100;
}
```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.

Function declarations load before any code is executed.

Function expressions load only when the interpreter reaches that line of code.

So if you try to call a function expression before it's loaded, you'll get an error! If you call a function declaration instead, it'll always work, because no code can be called until all declarations are loaded.

4. Why is a function call an expression in JavaScript?

A function call expression is used to execute a specified function with the provided arguments. If the function being called is overloaded, the compiler will attempt to match the argument types with the function parameter types. If there are no matching function declarations, a compile-time error will be raised.

5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3); // Answer   ---valid
five = add; // Answer--valid
five = five(10, 11); // Answer--invalid
five = function () {
  return "Hello";
}; // Answer  ---valid
```

6. What is the difference between function definition and function call? Explain with an example.

Using a function to do a particular task any point in program is called as function call.

So the difference between the function and function call is,

A function is procedure to achieve a particular result while function call is using this function to achive that task.

7. What is the similarities between function definition and function call?

A function is a block of code that does a particular operation and returns a result. It usually accepts inputs as parameters and returns a result. The parameters are not mandatory. A function call is the code used to pass control to a function

8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log("Hello World!");
}

hello.user = "Sam"; // valid or invalid---valid because function is treated as an object in javascript  so we can assign a value  in an object.
```

9. What is higher order function explain with an example.

The functions those one take a function as a argument or return a function.

```js
let num = [1, 2, 3, 4, 5, 6, 7, 8, 9];

function isEven(num) {
  return num % 2 === 0;
}

function filter(arry, cb) {
  let even = [];
  for (let num of arry) {
    if (cb(num)) {
      even.push(num);
    }
  }
  return even;
}

filter(num, isEven);
```

10. Explain what is callback function. Why you can pass a function inside a function?

the function that is passed as a argument to other function called callback function.
