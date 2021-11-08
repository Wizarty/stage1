Know global scope and functional scope :

-Global scope
There's only one Global scope in the JavaScript document. 
The area outside all the functions is consider the global scope
The variables defined inside the global scope can be accessed and altered in any other scopes.

-Local scope
Variables declared inside the functions become Local to the function.
Every Functions has its own scope so same variable can be used in different functions.
Local scope can be divided into function scope and block scope:
	1.Function scope
Whenever you declare a variable in a function, the variable is visible only within the function. You can't access it outside the function. var is the keyword to define variable for a function-scope accessibility.
	2.Block scope
whenever you see {curly brackets}, it is a block.
const and let are block scoped.

-Lexical scope
When the children scope have the access to the variables defined in the parent scope.



●variables visibility areas
var declarations are globally scoped or function scoped, while let and const are block scoped.

●nested scopes
The inner scope can access the variables of its outer scope, while the outer scope can’t access the variables of inner scope.
