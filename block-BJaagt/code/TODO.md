Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

Example:

```js
function hello() {
  var username = "Arya";
}
console.log(username); // output --user name is not defined
```

In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable is inside the function named `hello` and we can't access the variable defined inside a function from outside.

The above code will throw an error `Reference Error username is not defined`.

2. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
{
  const username = "Arya";
}
console.log(username); // output  --username is not defined.
```

In the above code we are looking for the variable named `username` . There is no variable in global scope so we can not access the variable named `username` from the out side of the its' scope.

3. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  let username = "Arya";
}
console.log(username); // output---username is not defined.
```

In the above code we can not access the variable named `username` from the out-side the it's scope be let keyword is a function and block scope variable.

4. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  var username = "Arya";
}
console.log(username); // output---Arya
```

In this above code there has been created a variable using var named `username` and var create function scope so there is no function declaration above code so we can access the variable .

5. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
if (true) {
  var username = "Arya";
}
console.log(username); // output---The above code will throw an error `syntaxError: username has already been declared`
```
In this above code there are two variable defined with same name first one with let and second one with var keyword so in this code let does not create any scope and var also does not create any scope when the execution will be  happen so the execution will start from the firs line ,there is variable named `username` and when we will reach another variable which has defined with same named `username` so it will not update because first one is defined with same name so the code will go throw syntaxError  which is username has already been declared. 

6. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
if (true) {
  let username = "Arya";
}
console.log(useranme); // output--John
```
let create a block scope so we can not access inside from block  and there is a global scope variable that can be accessed.

7. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
function sayHello() {
  let username = "Arya";
}
sayHello();
console.log(username); // output  `John`
```
In this above code function will return undefine and logged value will be John.

8. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (var i = 0; i < 10; i++) {
  console.log(i, "First"); // output  --0 to 9
}
console.log(i, "Second"); // output  --10
```

9. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (let i = 0; i < 10; i++) {
  console.log(i, "First"); // output --0 to 9
}
console.log(i, "Second"); // output---10
```
the above code let is not inside any scope so we can access it from out side .
