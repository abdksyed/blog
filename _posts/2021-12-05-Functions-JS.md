---
toc: true
layout: post
description: Basics of Functions in JavaScript
categories: [JavaScript, Beginner]
title: Learning JavaScript - Functions
---

# Functions in JavaScript

Functions are the building blocks of JavaScript. The are used to avoid repetition and to share code. We can wrap a code inside a function and call the function any number of times to execute the wrapped code.

Let's see with code.

```js
function functionName() {
  // code to be executed
  consloe.log('Hello World');
}
>>> 
```
We created the above function and ran the code, but didn't get any output🙄🙄🙄

This is because the code above is function `decleration`, JavaScript just stores the function code in memory during `Memory Creation` phase. Since we didn't `called` (`invoked`) the function, the function code is not executed.

To invoke/call the function, we use the `functionName()` syntax.

```js
functionName();
>>> Hello World
```

Now we can call the function any number of times, to get same result.
```js
functionName();
>>> Hello World

functionName();
>>> Hello World

functionName();
>>> Hello World
```

What if we just write the function name and run it without the `()`?

```js
functionName
>>>
```

We don't get any output. Lets see what happends when we print the function.

```js
console.log(functionName);
>>> [Function: functionName]
```

We get the output, which shows that the object we called is a function with name `functionName`.

Let's see what happens when we call the function inside console.log.

```js
console.log(functionName());
>>> Hello World
>>> undefined
```

We see that we can two outputs. The first is the output when the function is running i.e. the content which ran during the function execution.  
And the second is the output of the function call. Here the output of the function call is `undefined` because the function doesn't have return statement, so it returns `undefined` by default.

# Context

The concept of `context` is crtitical, so we will discuss the basic stuff here and come back to the context later with more information.

JavaScript, even before running the the script, creates something called `Global Context`. This is the place/space where all the variables and functions are stored and the code is present to be run.

For browser, the Global context is the `window` object. For nodeJS, the Global context is the `module.exports` object. Since different 

```js
var someVar = 'someVar'
if (someVar === someVar) {
    console.log(someVar);
}
>>> someVar

var someVar = 'someVar'
if (someVar === window.someVar) {
    console.log(someVar);
}
>>> someVar
```

There are concepts like `Hoisting`, `Scope`, `Scope Chain` which are part of Hitesh's YouTube series. But we will discuss those in much detail later.

## END!
That is it for today, getting to know basic functions in Java Script. We will see more in the upcoming days.

> Note: This material is created as part of learning Java Script from various resource, like [Hitesh Choudhary's JS Course](https://www.youtube.com/watch?v=2md4HQNRqJA&list=PLRAV69dS1uWSxUIk5o3vQY2-_VKsOpXLD) and [Akshay Saini's Namaste JS Course](https://www.youtube.com/watch?v=pN6jk0uUrD8&list=PLlasXeu85E9cQ32gLCvAvr9vNaUccPVNP)

