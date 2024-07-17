## About me

Hi, I have a React technical interview this monday and I am preparing for it by finding interview questions online and answering them here. I will post this since it may help somebody :D.  

  
Wish me luck and good luck to you aswell!

## Sources

[Web Dev Cody Video 1](https://www.youtube.com/watch?v=xo1sW5HD7os)  

[Web Dev Cody Video 2](https://www.youtube.com/watch?v=AHbAAnt9qsY)

## JS Questions
**Q1:** What is hoising in JS?  
**A1:** The process whereby the interpreter appears to move the declaration of functions, variables, classes, or imports to the top of their scope, prior to execution of the code.  
Example:  
```
printHelloWorld();

function printHelloWorld() {
  console.log("Hello World!")
}
```
This works in JavaScript cause the declaration of the function is automatically moved on top of the block and that's why printHelloWorld(); is executed without an error.  

**Q2:** What is closure in JS?  
**A1:** A function that has access to the variables in its parent scope, even after the parent function has completed execution.  
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

//This will print out 4 cause the function remembers the counter variable in the parent function. No idea how it works but it does.
```

## React Questions
