# JavaScript the Hard Parts: Promises, Async & the Event Loop:

The notes below are from Codesmith's [JavaScript the Hard Parts: Promises, Async & the Event Loop](https://www.youtube.com/watch?v=fOdcuDigxfw) video on youtube.

# Intro:

Promises: The most significant ES6 feature
Asynchronicity: the feature that makes dynamic web applications possible
The event loop: JavaScript's triage
Microtask queue, Callback queue and Web Browser features (APIs)

# JavaScript Principles:

Functions

- Set of code we save (define) and can use (call/invoke/execute/run) later on by using the function's name/label with parentheses
- Function definition is writing the function and the code that is in it
- Function invocation is actually running the code inside the function
- Functions hold parameters which are "placeholders" for the argument (value) which will be accepted by the function when it is called

Thread of Execution

- JavaScript goes through the code (globally or in a function) line by line and does whatever the line of code says to do
- The process of going through the code line by line and performing (executing) the tasks outlined by the code
- JavaScript is a single-threaded language
  - There is only one process that can do anything at a given time
  - JavaScript cannot multi-task (it can only execute one thing at a time)
    - Asynchronous JavaScript does not change this, it just changes the order in which lines of code are executed

Memory

- A store of data (variable environment) where anything defined in the function is stored
- Location in computer where labels and values are stored

# Global Execution Context:

- Environment in which the code is executing
- Global Execution Context consists of:
  - Global Memory
    - Associated Variables and their values
- Think of this as the global scope

# Call Stack

- Keeps what is currently being executed at the top of the stack
- Each running process on the call stack is referred to as a frame
- When a program is first run, a global execution context is placed on the stack (think of this as the global scope)
  - This is where variables are assigned and initialized
- When a variable is assigned to the evaluation of a function invocation (ex. `let hello = sayHello()`), a new execution context is created (function local scope)
  - This execution context is pushed onto the call stack
  - The thread of execution enters the function's local execution context the function parameters are mapped with their corresponding argument values
    - Any variable declarations are stored in the function's local execution context
    - Any calculations are also completed at the local execution context
  - The return value of a function is then stored in global memory (global scope)
    - The return keyword also triggers the function's local execution context to pop off of the call stack
    - The thread of execution leaves the local execution context
    - The local execution context is then garbage collected

# Asynchronicity is the backbone of modern web development in JavaScript

JavaScript is:

- Single threaded (one command runs at a time)
- Synchronously executed (each line is run in order the code appears)

So what if we have a task:

- Accessing Twitter's server to get new tweets that takes a long time
- code we want to run using those tweets

Challenge: We want to wait for the tweets to be stored in `tweets` so that they're there on run displayTweets on - **but no code can run in the meantime**

```js
const tweets = getTweets("http://twitter.com/will/1");
// 350ms wait while a request is sent to Twitter HQ

displayTweets(tweets);

// more code to run
console.log("I want to runnn!");
```

## What if we try to delay a function directly using setTimeout?

This is a problem because we don't know how long some of these tasks are going to take

setTimeout is a built in function

- First argument is the function to delay
- Second arguments in the ms to delay by
  In what order will our console logs occur?

```js
function printHello() {
  console.log("Hello");
}

setTimeout(printHello, 1000);
console.log("Me first!");
```

`console.log("Me first!")` will execute before the `setTimeout(printHello, 1000)` command

## What if we set the delay of 0ms?

Now, in what order will our console logs occur?

```js
function printHello() {
  console.log("Hello");
}

setTimeout(printHello, 0);
console.log("Me first!");
```

`console.log()` will still execute first. This is because when the thread of execution gets to setTimeout(), it puts printHello in the queue and moves on to print console.log()

# JavaScript is not enough

We need new pieces (some of which aren't JavaScript at all)

Our core JavaScript engine has 3 main parts:

- Thread of execution
- Memory / variable environment
- Call stack

We need to add some new components

- Web Browser APIs/Node background threads
- Promises
- Callback/Task queue and micro task queue
- Event loop

## ES5 Solution: Introducing 'callback functions', and Web Browser APIs

- Function definitions that would wait until they could execute
- Would have functions on top of functions

## Web Browser API

- Enabled by the web browser that adds additional functionality to JavaScript
