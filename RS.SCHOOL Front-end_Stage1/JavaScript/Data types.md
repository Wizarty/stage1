#js

# Javascript Data Types

JavaScript provides different **data types** to hold different types of values. There are two types of data types in JavaScript.

1.  Primitive data type
2.  Non-primitive (reference) data type

JavaScript is a **dynamic type language**, means you don't need to specify type of the variable because it is dynamically used by JavaScript engine. You need to use **var** here to specify the data type. It can hold any type of values such as numbers, strings etc. For example:

1.  var a\=40;//holding number 
2.  var b\="Rahul";//holding string 

## JavaScript primitive data types

There are five types of primitive data types in JavaScript. They are as follows:

| Data Type 	| Description 	|
|---	|---	|
| String 	| represents sequence of characters e.g. "hello" 	|
| Number 	| represents numeric values e.g. 100 	|
| Boolean 	| represents boolean value either false or true 	|
| Undefined 	| represents undefined value 	|
| Null 	| represents null i.e. no value at all 	|

## JavaScript non-primitive data types

The non-primitive data types are as follows:

| Data Type 	| Description 	|
|---	|---	|
| Object 	| represents instance through which we can access members 	|


---------------------------
--------------------------

There are 8 basic data types in JavaScript.

-   `number` for numbers of any kind: integer or floating-point, integers are limited by `±(253-1)`.
-   `bigint` is for integer numbers of arbitrary length.
-   `string` for strings. A string may have zero or more characters, there’s no separate single-character type.
-   `boolean` for `true`/`false`.
-   `null` for unknown values – a standalone type that has a single value `null`.
-   `undefined` for unassigned values – a standalone type that has a single value `undefined`.
-   `object` for more complex data structures.
-   `symbol` for unique identifiers.

The `typeof` operator allows us to see which type is stored in a variable.

-   Two forms: `typeof x` or `typeof(x)`.
-   Returns a string with the name of the type, like `"string"`.
-   For `null` returns `"object"` – this is an error in the language, it’s not actually an object.
