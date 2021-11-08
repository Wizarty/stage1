Know how to define Function parameters :

If a function is called with missing arguments (less than declared), the missing values are set to undefined.

Sometimes this is acceptable, but sometimes it is better to assign a default value to the parameter:

Example
function myFunction(x, y) {
  if (y === undefined) {
    y = 2;
  }
}


ECMAScript 2015 allows default parameter values in the function declaration:

function myFunction(x, y = 2) {
  // function code
}


Know difference between parameters passing by value and by reference :
https://dmitripavlutin.com/value-vs-reference-javascript/

● difference between parameters passing by value and by reference:
	-arguments are Passed by Value, Objects are Passed by Reference.
	-If a function changes an argument's value, it does not change the parameter's original value.
	-If a function changes an object property, it changes the original value.


In JavaScript primitive types are passed around as values: meaning that each time a value is assigned, a copy of that value is created.

On the other side objects (including plain objects, array, functions, class instances) are references. If you modify the object, then all variables that reference that object are going to see the change.

The comparison operator distinguishes comparing values and references. 2 variables holding references are equal only if they reference exactly the same object, but 2 variables holding values are equal if they simply have 2 same values no matter where the value originates: from a variable, literal, etc.

Often, however, you might want to compare objects by their structure rather than by reference. Check out the post How to Compare Objects in JavaScript.

Know how to handle dynamic amount of Function parameters : 

var args = Array.prototype.slice.call(arguments);
var args = [].slice.call(arguments);

// ES2015
const args = Array.from(arguments);
const args = [...arguments];

Properties
arguments.callee
Reference to the currently executing function that the arguments belong to. Forbidden in strict mode.

arguments.length
The number of arguments that were passed to the function.

arguments[@@iterator]
Returns a new Array iterator object that contains the values for each index in arguments.

The arguments object is not an Array. It is similar, but lacks all Array properties except length


There are three main differences between rest parameters and the arguments object:

The arguments object is not a real array, while rest parameters are Array instances, meaning methods like sort, map, forEach or pop can be applied on it directly;
The arguments object has additional functionality specific to itself (like the callee property).
The ...restParam bundles all the extra parameters into a single array, therefore it does not contain any named argument defined before the ...restParam. Whereas the arguments object contains all of the parameters -- including all of the stuff in the ...restParam -- unbundled.