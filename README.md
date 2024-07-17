## About me

Hi, I have a React technical interview this monday and I am preparing for it by finding interview questions online and answering them here. I will post this since it may help somebody :D.\
The questions are mainly from the two youtube videos from the youtuber Web Dev Cody (check out his channel very useful react content and he also has react exercises). I also added some questions myself that I thought could be useful. This does not guarantee that these will be the questions on YOUR interview, this is just my opinion on what is important.\
\
Wish me luck and good luck to you aswell!\
\
**NOTE: MY INTERVIEW IS FOR THE NEWER REACT THAT USES FUNCTIONAL REACT COMPONENTS, NOT OLD REACT THAT USE CLASSES, I WILL SKIP QUESTIONS ABOUT CLASSES**

## JS Questions
**Q1:** What is hoising in JS?\
**A1:** The process whereby the interpreter appears to move the declaration of functions, variables, classes, or imports to the top of their scope, prior to execution of the code.\
Example:
```
printHelloWorld();

function printHelloWorld() {
  console.log("Hello World!")
}
```
This works in JavaScript cause the declaration of the function is automatically moved on top of the block and that's why printHelloWorld(); is executed without an error.\
\
\
**Q2:** What is closure in JS?\
**A2:** A function that has access to the variables in its parent scope, even after the parent function has completed execution.\
Example:
```
function makeCounter() {
  let counter = 0;

  return function() {
    counter++;
    return counter;
  }
}

const myCounter = makeCounter();
myCounter();
myCounter();
myCounter();
console.log(myCounter();)
```
This will print out 4 cause the function remembers the counter variable in the parent function. No idea how it works but it does.\
\
\
**Q3:** What is the difference between var, let and const?\
**A3:** Var variables are function scoped, which means they can be used throughout the entire function, also they can be reassigned. This is because their declaration is hoisted, unlike the other two.\
Let variables can also be reassigned, but they are block scoped.\
Const variables cannot be reassigned, and they are also block scoped.\
Example:
```
if (true) {
  var x = 10;
  console.log("Inside block, x:", x); // Output: 10
}
console.log("Outside block, x:", x); // Output: 10
```
The example above shows that var is function scoped, if we put let or const instead, the second compose would cause an error since it is declared in the if block, but printed outside of the if block.\
\
\
**Q4:** What are arrow functions and how are they used?\
**A4:** Arrow functions are a different way to declare functions. They are often used with functions like .map, .filter, etc. since they provide better readability. They are also used for some practical thing with the this keyword but since I am doing functional react we don't use classes so I don't care about it that much. 
Example of arrow functions:
```
// Traditional function expression
const add = function(a, b) {
    return a + b;
};

// Arrow function
const add = (a, b) => a + b;
```
\
\
**Q5:** What is synchronous and what is asynchronous?\
**A5:** Synchronous means that the operation runs line by line, the next line only gets executed when the previous one is finished with execution. Asynchronous means that lines will run in parallel if that is possible.\
\
\
**Q6:** What are promises?\
**Q6:** Promises are a way to handle asynchronous operations. A promise has three states:\
Pending: The initial state, neither fulfilled nor rejected.\
Fulfilled: The operation completed successfully.\
Rejected: The operation failed.\
Example:
```
let promise = new Promise((resolve, reject) => {
  let success = true; // Change this to false to see the rejection case.

  if (success) {
    resolve("Message delivered successfully!");
  } else {
    reject("Failed to deliver the message.");
  }
});

// Handling the promise
promise
  .then((message) => {
    console.log(message); // This will run if the promise is resolved
  })
  .catch((error) => {
    console.error(error); // This will run if the promise is rejected
  });
```
## React Questions

## Sources

[Web Dev Cody Video 1](https://www.youtube.com/watch?v=xo1sW5HD7os)\
[Web Dev Cody Video 2](https://www.youtube.com/watch?v=AHbAAnt9qsY)\
[Difference between var, const and let](https://www.naukri.com/code360/library/difference-between-var-let-and-const-in-js)
