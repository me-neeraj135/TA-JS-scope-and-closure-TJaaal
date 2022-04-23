## Understanding Scope and the difference between var, let and const

Watch this video before doing the exercise: https://www.youtube.com/watch?v=XgSjoHgy3Rk

1. Guess the output:

```js
let firstName = "Arya";
const lastName = "Stark";
var knownAs = "no one";

console.log(
  window.firstName, //undefined
  window.lastName, // undefined
  window.knownAs // no one
);
```

2. Guess the output:

```js
let firstName = "Arya";
const lastName = "Stark";
var knownAs = "no one";

function fullName(a, b) {
  return a + b;
}

console.log(window.fullName(firstName, lastName)); //AryaStark
```

3. Make a Execution Context Diagram for the following JS and write the output.

```js
function addOne(num) {
  return num + 1;
}
var one = addOne(0);
var two = addOne(1);
console.log(one, two); //1 2
```

4. Make a Execution Context Diagram for the following JS and write the output.

```js
var one = addOne(0);
function addOne(num) {
  return num + 1;
}
var two = addOne(1);
console.log(one, two); //1 2
```

5. Make a Execution Context Diagram for the following JS and write the output.

```js
console.log(addOne(0)); //1
function addOne(num) {
  return num + 1;
}
var two = addOne(1);
console.log(two); //2
```

6. Make a Execution Context Diagram for the following JS and write the output.

```js
var one = addOne(0); //  reference error undefined
const addOne = num => {
  return num + 1;
};
var two = addOne(1);
console.log(two); //2
```

7. Make a Execution Context Diagram for the following JS and write the output.

```js
console.log(addOne(0)); //Uncaught ReferenceError addOne is not defined
const addOne = num => {
  return num + 1;
};
var two = addOne(1);
console.log(two); //2
```

8. What will be the output of the following

```js
function isAwesome() {
  var awesome;
  if (false) {
    awesome = true;
  }
  console.log(awesome); //undefined
}
isAwesome(); //undefined
```

9. What will be the output of the following

```js
function isAwesome() {
  let awesome;
  if (true) {
    awesome = true;
  }
  console.log(awesome); //true
}
isAwesome(); //undefined
```

10. What will be the output of the following

```js
function isAwesome() {
  let awesome;
  if (false) {
    awesome = true;
  }
  console.log(awesome); //undefined
}
isAwesome(); //undefined
```

11. What will be the output of the following

```js
let firstName = "Arya";
const lastName = "Stark";
var knownAs = "no one";

function fullName(a, b) {
  return a + b;
}
const name = fullName(firstName, lastName);
console.log(name); //AryaStark
```

12. Guess the output of the code below with a reason.

````js
function sayHello() {
  let name = 'Arya Stark';
}
sayHello();  //undefined

console.log(name);//  name is not defined
```

13. Guess the output of the code below with a reason.

````js
if (true) {
  var name = 'Arya Stark';
}
console.log(name);//Arya Stark

````

14. Guess the output of the code below with a reason.

```js
if (true) {
  let name = "Arya Stark";
}
console.log(name); //not defined
```

15. Guess the output of the code below with a reason.

```js
for (var i = 0; i < 20; i++) {
  //
}
console.log(i); //var does not create block scoped so it will log the value out side of loop  20.
```

16. Guess the output of the code below with a reason.

```js
for (let i = 0; i < 20; i++) {
  //
}
console.log(i); //  we can log the value which is 20 at last.
```

17. Guess the output and the reason behind that.

```js
function sample() {
  if (true) {
    var username = "John Snow";
  }
  console.log(username);
}
sample(); // John Snow
```

18. Guess the output and the reason behind that.

```js
function sample() {
  if (true) {
    let username = "John Snow";
  }
  console.log(username); //there is an reference error because username creates a block scoped so we can not log that.
}
sample(); // undefined
```

19. Guess the output and the reason behind that.

```js
function sample() {
  var username = "Arya Stark";
  if (true) {
    var username = "John Snow";
    console.log(username); //John Snow---in this function we overwrite the var with new value.
  }
  console.log(username, "second"); //John Snow second
}
sample();
```

20. Guess the output and the reason behind that.

```js
function sample() {
  let username = "Arya Stark";
  if (true) {
    let username = "John Snow";
    console.log(username, "first"); //John Snow--- in this function we create two variable using let keyword with same name in two-different blocks-scoped.
  }
  console.log(username, "second"); //Arya Stark second
}
sample();
```

21. Guess the output and the reason behind that.

```js
function sample(...args) {
  for (let i = 0; i < args.length; i++) {
    let message = `Hello I am ${args[i]}`;
    console.log(message); //  Hello I am First,Hello I am Second,Hello I am Third.---
    //  spread operator will make the argument iterable .
  }
}

sample("First", "Second", "Third");
```

22. Guess the output and the reason behind that.

```js
function sample(...args) {
  for (let i = 0; i < args.length; i++) {
    const message = `Hello I am ${args[i]}`; //in every iteration we assign a new value
    console.log(message); //Hello I am First ,Hello I am Second, Hello I am Third
  }
}

sample("First", "Second", "Third");
```

23. Guess the output and the reason behind that.

```js
if (true) {
  const myFunc = function () {
    console.log(username, "Second"); //ReferenceError: Cannot access 'username' before initialization
  };
  console.log(username, "First");
  let username = "Hello World!";
  myFunc();
}
```

24. Guess the output and the reason behind that.

```js
function outer() {
  let movie = "Mad Max: Fury Road";
  function inner() {
    console.log(
      `I love this movie called ${movie.toUpperCase()}` //I love this movie called MAD MAX: FURY ROAD
    );
  }
  inner();
}

outer();
```

25. Guess the output and the reason behind that.

```js
function outer() {
  let movie = "Mad Max: Fury Road";
  function inner() {
    let movie = "Before Sunrise";
    console.log(
      `I love this movie called ${movie.toUpperCase()}` //I love this movie called BEFORE SUNRISE
    );
  }
  inner();
}

outer();
```

26. Guess the output and the reason behind that.

```js
function outer() {
  let movie = "Mad Max: Fury Road";
  function inner() {
    let movie = "Before Sunrise";
    function extraInner() {
      let movie = "Gone Girl";
      console.log(
        `I love this movie called ${movie.toUpperCase()}` //I love this movie called GONE GIRL
      );
    }
    extraInner();
  }
  inner();
}
outer();
```

30. Using reduce find the final value when the initial value passed is `100`. You have to pass the output of one function into the input of next function in the array `allFunctions` starts with `addOne` ends with `half`.

```js
const addOne = num => {
  return num + 1;
};
const subTwo = num => {
  return num - 2;
};
const multiplyThree = num => {
  return num * 3;
};
const half = num => {
  return num / 2;
};

let allFunctions = [addOne, subTwo, multiplyThree, addOne, multiplyThree, half];
allFunctions.reduce((acc, cv) => {
  acc = cv(acc);
  return acc;
}, 100);

// Answer is: 447
```
