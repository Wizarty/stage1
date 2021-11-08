The term "global objects" (or standard built-in objects) here is not to be confused with the global object. Here, "global objects" refer to objects in the global scope.

The global object itself can be accessed using the this operator in the global scope. In fact, the global scope consists of the properties of the global object, including inherited properties, if any.

Other objects in the global scope are either created by the user script or provided by the host application. The host objects available in browser contexts are documented in the API reference.

Static methods :

Object.assign()
Copies the values of all enumerable own properties from one or more source objects to a target object.

Object.create()
Creates a new object with the specified prototype object and properties.

Object.defineProperty()
Adds the named property described by a given descriptor to an object.

Object.defineProperties()
Adds the named properties described by the given descriptors to an object.

Object.entries()
Returns an array containing all of the [key, value] pairs of a given object's own enumerable string properties.

Object.freeze()
Freezes an object. Other code cannot delete or change its properties.

Object.fromEntries()
Returns a new object from an iterable of [key, value] pairs. (This is the reverse of Object.entries).

Object.getOwnPropertyDescriptor()
Returns a property descriptor for a named property on an object.

Object.getOwnPropertyDescriptors()
Returns an object containing all own property descriptors for an object.

Object.getOwnPropertyNames()
Returns an array containing the names of all of the given object's own enumerable and non-enumerable properties.

Object.getOwnPropertySymbols()
Returns an array of all symbol properties found directly upon a given object.

Object.getPrototypeOf()
Returns the prototype (internal [[Prototype]] property) of the specified object.

Object.is()
Compares if two values are the same value. Equates all NaN values (which differs from both Abstract Equality Comparison and Strict Equality Comparison).

Object.isExtensible()
Determines if extending of an object is allowed.

Object.isFrozen()
Determines if an object was frozen.

Object.isSealed()
Determines if an object is sealed.

Object.keys()
Returns an array containing the names of all of the given object's own enumerable string properties.

Object.preventExtensions()
Prevents any extensions of an object.

Object.seal()
Prevents other code from deleting properties of an object.

Object.setPrototypeOf()
Sets the object's prototype (its internal [[Prototype]] property).

Object.values()
Returns an array containing the values that correspond to all of a given object's own enumerable string properties.




Property flags and descriptors
As we know, objects can store properties.

Until now, a property was a simple “key-value” pair to us. But an object property is actually a more flexible and powerful thing.

In this chapter we’ll study additional configuration options, and in the next we’ll see how to invisibly turn them into getter/setter functions.

Property flags
Object properties, besides a value, have three special attributes (so-called “flags”):

writable – if true, the value can be changed, otherwise it’s read-only.
enumerable – if true, then listed in loops, otherwise not listed.
configurable – if true, the property can be deleted and these attributes can be modified, otherwise not.
We didn’t see them yet, because generally they do not show up. When we create a property “the usual way”, all of them are true. But we also can change them anytime.

First, let’s see how to get those flags.

The method Object.getOwnPropertyDescriptor allows to query the full information about a property.




Symbol.iterator symbol specifies the default iterator for an object. Used by for...of.

Whenever an object needs to be iterated (such as at the beginning of a for..of loop), its @@iterator method is called with no arguments, and the returned iterator is used to obtain the values to be iterated.

Some built-in types have a default iteration behavior, while other types (such as Object) do not. The built-in types with a @@iterator method are:

Array.prototype[@@iterator]()
TypedArray.prototype[@@iterator]()
String.prototype[@@iterator]()
Map.prototype[@@iterator]()
Set.prototype[@@iterator]()