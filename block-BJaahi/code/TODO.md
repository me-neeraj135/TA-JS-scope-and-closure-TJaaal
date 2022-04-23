For the given code below:

- re-write the code in ways that system will understand

For Example:

1.

```js
var username = "Arya";
let brothers = ["John", "Ryan", "Bran"];

console.log(username, brothers[0]);

function sayHello(name) {
  return `Hello ${name}`;
}

let message = sayHello(username);
var nextMessage = sayHello("Test");
```

<!-- Answer -->

```js
var username = undefined; //`Arya
let brothers; //["John", "Ryan", "Bran"];
console.log(username, brothers[0]);
`Arya`, `John`;
function sayHello(name) {
  return `Hello ${name}`;
}
let messag; //`Arya`
var nextMessage = undefined; //`Hello Test`
```

```js
// Declaration Phase
var username = undefined;
let brothers;

function sayHello(name) {
  return `Hello ${name}`;
}

let message;
var nextMessage = undefined;

// Execution Phase

username = "Arya";
brothers = ["John", "Ryan", "Bran"];

console.log(username, brothers[0]);

message = sayHello(username);
nextMessage = sayHello("Test");
```

2.

```js
console.log(username, numbers);

var username = "Arya";
let number = 21;

function sayHello(name) {
  return `Hello ${name}`;
}

let message = sayHello(username);
var nextMessage = sayHello("Test");
```

<!-- Answer -->

```js
// Your code goes here

//declaration
console.log(username, numbers);

var username = undefined;
let number;

function sayHello(name) {
  return `Hello ${name}`;
}

let message;
var nextMessage = undefined;

// Execution

console.log(username, numbers);(undefined,number is not defined)

var username = "Arya";
let number = 21;

function sayHello(name) {
  return `Hello ${name}`;
}

let message = sayHello(username);
var nextMessage = sayHello("Test");
```

3.

```js
console.log(username, numbers);
let username = "Arya";
let number = 21;

let sayHello = function (name) {
  return `Hello ${name}`;
};

let message = sayHello(username);
var nextMessage = sayHello("Test");
```

<!-- Answer -->

```js
// Your code goes here

// declaration
console.log(username, numbers);
let username = undefined;
let number;

let sayHello;

let message;
var nextMessage = undefined;

// Execution

console.log(username, numbers);(undefined, error=fnumber is not defined)
let username = "Arya";
let number = 21;

let sayHello = function (name) {
  return `Hello ${name}`;
};

let message = sayHello(username);
var nextMessage = sayHello("Test");
```

4.

```js
let username = "Arya";
console.log(username, numbers);

let number = 21;
let message = sayHello(username);

let sayHello = function (name) {
  return `Hello ${name}`;
};

var nextMessage = sayHello("Test");
```

<!-- Answer -->

```js
// Your code goes here

// declaration

let username;
console.log(username, numbers);

let number;
let message;

let sayHello;

var nextMessage = undefined;

// execution

let username = "Arya";
console.log(username, numbers); //(Error number is not defined)

let number = 21;
let message = sayHello(username); //Error sayHello is not defined

let sayHello = function (name) {
  return `Hello ${name}`;
};

var nextMessage = sayHello("Test");
```

5.

```js
console.log(name);
console.log(age);
var name = "Lydia";
let age = 21;
```

<!-- Answer -->

```js
// Your code goes here

// Declaration

console.log(name);
console.log(age);
var name = undefined;
let age;

// Execution

console.log(name); //undefined
console.log(age); //Error age is not defined
var name = "Lydia";
let age = 21;
```

6.

```js
function sayHi(name) {
  console.log(name);
  console.log(age);
  var name = "Lydia";
  let age = 21;
}

sayHi();
```

<!-- Answer -->

```js
// Your code goes here

// Declaration

function (){};


// Execution

function sayHi(name) {
  //declaration
  var name=undefined;
   var name = undefined;
  let age;

  // Execution
 console.log(name);// undefined
  console.log(age);// Error age is not defined
  var name = "Lydia";
  let age = 21;



}

sayHi();


```

7.

```js
sayHi();
function sayHi(name) {
  console.log(name);
  console.log(age);
  var name = "Lydia";
  let age = 21;
}
```

<!-- Answer -->

```js
// Your code goes here

//Declaration
function sayHi() {}

//Execution
sayHi();
function sayHi(name) {
  //declaration
  var name = undefined;
  var name = undefined;
  let age;
  //Execution
  console.log(name); //undefined
  console.log(age); //Error is not defined
  var name = "Lydia";
  let age = 21;
}
```

8.

```js
sayHi();
let sayHi = function sayHi(name) {
  console.log(name);
  console.log(age);
  var name = "Lydia";
  let age = 21;
};
```

<!-- Answer -->

```js
// Your code goes here
//declaration
let sayHi;
var name = undefined;
let age;

// Execution
sayHi(); //error sayHi is not defined
```

9.

```js
let num1 = 21;
console.log(sum);
var sum = num1 + num2;
let num2 = 30;
```

<!-- Answer -->

```js
// Your code goes here

// declaration

let num1;
var sum = undefined;
let num2;

// Execution
let num1 = 21;
console.log(sum); // num2 is not defined
var sum = 21 + not defined;
let num2 = 30;
```

10.

```js
var num1 = 21;

let sum2 = addAgain(num1, num2, 4, 5, 6);

let add = (a, b, c, d, e) => {
  return a + b + c + d + e;
};
function addAgain(a, b) {
  return a + b;
}
let num2 = 200;

let sum = add(num1, num2, 4, 5, 6);
```

<!-- Answer -->

```js
// Your code goes here

// declaration

var num1 = undefined;

let sum2;

let add;
function addAgain() {}
let num2;

let sum;

// Execution
var num1 = 21;

let sum2 = addAgain(num1, num2, 4, 5, 6); // num2 is not defined
function addAgain(a, b) {
  //declaration
  var a = undefined;
  var b = undefined;

  //Execution
  var a = num1;
  var b = num2;

  return a + b;
}

let add;

let num2;

let sum;
```

11.

```js
function test(a) {
  let num1 = 21;
  return add(a, num1);
}

let sum = test(100);

let add = (a, b) => {
  return a + b;
};
```

<!-- Answer -->

```js
// Your code goes here

// Declaration

function test() {}

let sum;

let add;

// Execution

function test(a) {
  // Declaration
  var a = undefined;

  let num1;

  // Execution
  var a = 100;
  let num1 = 21;
  return add(a, num1); //add is not defined
}
let sum = test(100);
```

12.

```js
function test(a) {
  let num1 = 21;
  return add(a, num1);
}

let sum = test(100);

function add(a, b) {
  return a + b;
}
```

<!-- Answer -->

```js
// Your code goes here

//declaration
function test() {}
let sum;
function add() {}

// Execution
function test(a) {
  //declaration
  var a = undefined;
  let num1;
  //Execution
  var a = 100;
  let num1 = 21;
  return add(a, num1);
}

function add(a, b) {
  //Declaration
  var a = undefined;
  var b = undefined;

  //execution

  var a = 100;
  var b = 21;
  return a + b; //121
}
```
