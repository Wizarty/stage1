#js

| Keyword	| Description |	Scope |
|------- |---------- |------ |
| var	| Var is used to declare variables(old way of declaring variables)	| Function or global scope |
| let	| let is also used to declare variables(new way)	| Global or block Scope| 
| const |	const is used to declare const values. Once the value is assigned it can not be modified	| Global or block Scope |
# Let
Variables defined with `let` cannot be Redeclared.

Variables defined with `let` must be Declared before use.

Variables defined with `let` have Block Scope.

`let` and `const` keywords provide **Block Scope** in JavaScript.

Variables declared inside a { } block cannot be accessed from outside the block:

### Example
```js
{  
  let x = 2;  
}  
// x can NOT be used here
```

Variables declared with the `var` keyword can NOT have block scope.

Variables declared inside a { } block can be accessed from outside the block.

### Example
```js
{  
  var x = 2;  
}  
// x CAN be used here
```

## Redeclaring Variables

Redeclaring a variable using the `var` keyword can impose problems.

Redeclaring a variable inside a block will also redeclare the variable outside the block:

### Example
```js
var x = 10;  
// Here x is 10  
  
{  
var x = 2;  
// Here x is 2  
}  
  
// Here x is 2
```

Redeclaring a variable using the `let` keyword can solve this problem.

Redeclaring a variable inside a block will not redeclare the variable outside the block:

### Example
```js
let x = 10;  
// Here x is 10  
  
{  
let x = 2;  
// Here x is 2  
}  
 
// Here x is 10
```

# Const

## Cannot be Reassigned

A `const` variable cannot be reassigned:

### Example
```js
const PI = 3.141592653589793;  
PI = 3.14; // This will give an error  
PI = PI + 10; // This will also give an error
```

## Must be Assigned

JavaScript `const` variables must be assigned a value when they are declared:

### Correct

```js
const PI = 3.14159265359;  
```

### Incorrect

```js
const PI;  
PI = 3.14159265359;
```

Use `const` when you declare:

-   A new Array
-   A new Object
-   A new Function
-   A new RegExp

## Constant Objects and Arrays

The keyword `const` is a little misleading.

It does not define a constant value. It defines a constant reference to a value.

Because of this you can NOT:

-   Reassign a constant value
-   Reassign a constant array
-   Reassign a constant object

But you CAN:

-   Change the elements of constant array
-   Change the properties of constant object


## Constant Arrays

You can change the elements of a constant array:

### Example

```js
// You can create a constant array:  
const cars = \["Saab", "Volvo", "BMW"\];  
  
// You can change an element:  
cars\[0\] = "Toyota";  
  
// You can add an element:  
cars.push("Audi");  
```


But you can NOT reassign the array:

### Example

```js
const cars = \["Saab", "Volvo", "BMW"\];  
  
cars = \["Toyota", "Volvo", "Audi"\];    // ERROR
```


## Constant Objects

You can change the properties of a constant object:

### Example

```js
// You can create a const object:  
const car = {type:"Fiat", model:"500", color:"white"};  
  
// You can change a property:  
car.color \= "red";  
  
// You can add a property:  
car.owner \= "Johnson";
```

But you can NOT reassign the object:

### Example

```js
const car = {type:"Fiat", model:"500", color:"white"};  
  
car = {type:"Volvo", model:"EX60", color:"red"};    // ERROR
```