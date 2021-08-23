#js

# Types of functions in javascript?

1.  **Named** function
2.  **Anonymous** function
3.  **Immediately invoked** function expression. It runs as soon as the browser finds it.

# **Named** function

**Named function** is the function that we **_define_** it in the code and then call it whenever we need it by referencing its _name and passing some arguments_ to it. Named functions are useful if we need to call a function **many times** to pass **different values** to it or run it several times.

# **Anonymous** function

The anonymous functions don’t have **names**. They need to be tied to something: _variable or an event to run_.

# **Immediately invoked** function expression—

**IIFE**

**Invoked function** expression runs as soon as the **_browser encounters_** it. The benefit of this function is that it **runs immediately** where it’s located in the code and produces a _direct output_. That means it is **unaffected** by code which appears further down in the script which can be useful.

**An invoked function** expression is great for **_quickly populating_** _a variable or argument_ in a larger function or a property in an object and are often hooked to event listeners for immediate output.

-----------------------

## Function Parameters and Arguments

A JavaScript `function` does not perform any checking on parameter values (arguments).

```js
function _functionName_(_parameter1, parameter2, parameter3_) {  
 // _code to be executed_  
}
```

Function **parameters** are the **names** listed in the function definition.

Function **arguments** are the real **values** passed to (and received by) the function.

## Parameter Rules

JavaScript function definitions do not specify data types for parameters.

JavaScript functions do not perform type checking on the passed arguments.

JavaScript functions do not check the number of arguments received.

---

## Default Parameters

If a function is called with **missing arguments** (less than declared), the missing values are set to `undefined`.

Sometimes this is acceptable, but sometimes it is better to assign a default value to the parameter:

### Example

```js
function myFunction(x, y) {  
  if (y === undefined) {  
    y = 2;  
  }  
}
```

[ECMAScript 2015](https://www.w3schools.com/js/js_es6.asp) allows default parameter values in the function declaration:

```js
function (x, y = 2) {  
  // function code  
}
```