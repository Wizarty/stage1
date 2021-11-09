Immediately invoked functional expression (IIFE) (optional) :

It runs as soon as the browser finds it.
That means it is unaffected by code which appears further down in the script.
The variable and functions that were declared in the scope of IIFE are available for garbage collection, once the IIFE is executed. Hence managing Memory in an efficient manner and ensures that the function and variables do not bind itself to the global scope.

Know IIFE pattern (optional) :
https://www.codeproject.com/Articles/1110916/JavaScript-IIFE-Design-Pattern


Because our application could include many functions and global variables from different source files, it's important to limit the number of global variables. If we have some initiation code that we don't need to use again, we could use the IIFE pattern. As we will not reuse the code again, using IIFE in this case is better than using a function declaration or a function expression.

 IIFE pattern is a work around to the fact that ES5 and below do not have a way to create block scopes. By wrapping everything in a function and immediately invoking it, we can create a scope.

 blocks are going to replace IEFEs, as soon as block-scoped declarations (functions, let/const/class) become widely adopted. You need a scope, e.g. for a closure? Here you have a block, be it a loop body or just part of a statement list.

However, there is still one application of IEFEs that blocks cannot replace: the module pattern. Blocks don't have return values, and mutating higher-scoped variables is ugly, so we will still see function expressions in the creation of objects that need private state:

const example = (() => {
    …
    return …;
}());

Callback (Function as argument) :

A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

The above example is a synchronous callback, as it is executed immediately.

Note, however, that callbacks are often used to continue code execution after an asynchronous operation has completed — these are called asynchronous callbacks. A good example is the callback functions executed inside a .then() block chained onto the end of a promise after that promise fulfills or rejects. This structure is used in many modern web APIs, such as fetch().


Know callback pattern :


This pattern consists of these principles:

One callback to rule them all: one sole function instead of a success and an error one;
The callback is called once and exactly once. It’s called when an error occurs, or a result is available;
Function-last: the function is the last argument of the call that initiates I/O;
Error-first: the callback has the following function signature:
function (err, result) {    
  //...  
}
The values passed into the callback have different values depending on whether an error occurred or not:

If no error occurred:

The first callback argument is null or undefined;
The second argument contains the callback results.
On the other hand, if an error occurred:

the first argument contains an error object, an instance of the JavaScript Error class (or sub-class) that describes the error;
the second argument will be undefined.
This patterns forces the programmer to not ignore errors (by not defining an error callback) and, more importantly, defines a common pattern on top of which you can build abstractions and utilities.

Here is an example of the callback pattern in action in Node.js when reading the contents of a file:

var fs = require('fs');
fs.readFile('/some/path/to/file.txt', function(err, fileContent) {    
  if (err) {  
    handleError(err);  
  } else {  
    // use fileContent  
  }  
});
function handleError(err) {    
  console.error('error caught while reading file:', err);  
}
Here we’re handling occurring errors simply by logging into the console, but depending on your application you may want to handle it more appropriately: log it into a central place, notify someone, terminate a request, etc.

The important part of the callback function is that we’re breaking the flow of the application. Instead of using an if/else branch for that, you may also use a return, which would go like this:

fs.readFile('/some/path/to/file.txt', function(err, fileContent) {    
  if (err) {  
    return handleError(err);  
  }  
  // use fileContent  
});


Understand callback limitations (callback hell) (optional) :

freecodecamp.org/news/how-to-deal-with-nested-callbacks-and-avoid-callback-hell-1bc8dc4a2012/


Binding, binding one function twice :


