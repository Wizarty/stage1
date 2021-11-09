#this #this_scope

`this` Keyword :

https://medium.com/tech-tajawal/javascript-this-4-rules-7354abdb274c

The this keyword behaves differently in JavaScript compared to other languages. In JavaScript the value of this not refer to the function in which it is used or it’s scope but is determined mostly by the invocation context of function (context.function()) and where it is called.

#ReferenceTypeAndLosing_this

Reference Type & losing this :

 this loses context in many situations. It loses context:
inside nested functions
in callbacks
when the method is used as an event handler
this has no encapsulation
this creates security problems. All members declared on this are public.

#Difference_between_function_and_method

Understand difference between function and method :
https://www.geeksforgeeks.org/difference-between-methods-and-functions-in-javascript/

 Methods are functions stored as object properties.
 The method operates the data contained in a Class.
 A method implicitly passes the object on which it was called.

#how_this_works_and_realize_this_possible_issues

Understand how this works, realize this possible issues :

this has no encapsulation
 this creates security problems. All members declared on this are public.

#Manage_this_scope

Manage this scope :

call(), apply(), bind()
 The bind() method creates a new function that, when called, has its this keyword set to the provided value.
 call() method does the same as bind, except it calls itself
 apply() is the same as call, but second argument is always array.

#replace_this_scope

Be able to replace this scope :

https://ultimatecourses.com/blog/everything-you-wanted-to-know-about-javascript-scope

#call_and_apply_Function_built-in_methods
Be able to use call and apply Function built-in methods :

Use .bind() when you want that function to later be called with a certain context, useful in events. Use .call() or .apply() when you want to invoke the function immediately, and modify the context.

Call/apply call the function immediately, whereas bind returns a function that, when later executed, will have the correct context set for calling the original function. This way you can maintain context in async callbacks and events.

I do this a lot:

function MyObject(element) {
    this.elm = element;

    element.addEventListener('click', this.onClick.bind(this), false);
};

MyObject.prototype.onClick = function(e) {
     var t=this;  //do something with [t]...
    //without bind the context of this function wouldn't be a MyObject
    //instance as you would normally expect.
};
I use it extensively in Node.js for async callbacks that I want to pass a member method for, but still want the context to be the instance that started the async action.

A simple, naive implementation of bind would be like:

Function.prototype.bind = function(ctx) {
    var fn = this;
    return function() {
        fn.apply(ctx, arguments);
    };
};
