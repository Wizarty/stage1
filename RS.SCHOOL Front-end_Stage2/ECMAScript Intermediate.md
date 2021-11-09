Function default parameters :

Default function parameters allow named parameters to be initialized with default values if no value or undefined is passed.
We can also use a function as a default value.

ECMA script modules:

ES module is a mechanism for code reuse in JavaScript. Updating a single module is much easier when  the module is decoupled from other pieces of code.
Add type=”module” in html script tag to activate modules.


An ECMAScript module (ES module for short) is a mechanism for code reuse in JavaScript, introduced in 2015. It's finally becoming the standard in the highly fragmented JavaScript module scene.

Up until 2015 JavaScript didn't have a standard mechanism for code reuse. There had been a lot of attempts to standardize this aspect, which lead to messy fragmentation during the years.

You might have heard about AMD modules, UMD, or CommonJS. There was no clear winner. Finally, with ECMAScript 2015, ES modules landed in the language.

We now have an "official" module system.


Know how to use spread operator for Function arguments :

Syntax
For function calls:
myFunction(...iterableObj); // pass all elements of iterableObj as arguments to function myFunction

For array literals or strings:
[...iterableObj, '4', 'five', 6]; // combine two arrays by inserting all elements from iterableObj

For object literals (new in ECMAScript 2018):
let objClone = { ...obj }; // pass all key:value pairs from an object 

Rest syntax looks exactly like spread syntax. In a way, rest syntax is the opposite of spread syntax. Spread syntax "expands" an array into its elements, while rest syntax collects multiple elements and "condenses" them into a single element. 

Be able to compare arguments and rest parameters :

Rest parameters
With rest parameter, you can represent a number of arguments as an array. ES6 brought rest parameter to ease the work of developers. For arguments objects, rest parameters are indicated by three dots … and precedes a parameter.

Arguments object
Arguments object in JavaScript is an object, which represents the arguments to the function executing.

Here is the difference between rest parameters and the arguments object.

Arguments object includes all arguments passed to the function, whereas rest parameters are those, which are not given another name.
The rest parameters are Array instances, whereas arguments object isn’t an array. Array instances are the following methods: map, sort, pop, etc


When we see "..." in the code, it is either rest parameters or the spread syntax.

There’s an easy way to distinguish between them:

When ... is at the end of function parameters, it’s “rest parameters” and gathers the rest of the list of arguments into an array.
When ... occurs in a function call or alike, it’s called a “spread syntax” and expands an array into a list.
Use patterns:

Rest parameters are used to create functions that accept any number of arguments.
The spread syntax is used to pass an array to functions that normally require a list of many arguments.
Together they help to travel between a list and an array of parameters with ease.

All arguments of a function call are also available in “old-style” arguments: array-like iterable object.


Spread operator for Array :

A better way to concatenate arrays
Array.prototype.concat() is often used to concatenate an array to the end of an existing array. Without spread syntax,



Understand and able to use spread operator for Array concatenation Destructuring assignment : 

https://www.excellarate.com/blogs/destructuring-assignment-in-es6/




String templates :

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals


Know how for..of loop works (optional) :

for-of is a new loop in ES6 that replaces both for-in and forEach() and supports the new iteration protocol.

The operand of the of clause must be iterable. That means that you need a helper function if you want to iterate over plain objects (see “Plain objects are not iterable”). If a value is Array-like, you can convert it to an Array via Array.from():

If you const-declare the iteration variable, a fresh binding (storage space) will be created for each iteration. That can be seen in the following code snippet where we save the current binding of elem for later, via an arrow function. Afterwards, you can see that the arrow functions don’t share the same binding for elem, they each have a different one.

https://exploringjs.com/es6/ch_for-of.html

Difference between for...of and for...in
Both for...in and for...of statements iterate over something. The main difference between them is in what they iterate over.

The for...in statement iterates over the enumerable properties of an object.

The for...of statement iterates over values that the iterable object defines to be iterated over.



