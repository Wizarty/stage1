#js #methods

# **bind()**

The `**bind()**` method creates a new function that, when called, has its `this` keyword set to the provided value. (It actually talks about even more stuff, but we’ll leave that for another time :) )

This is extremely powerful. It let’s us explicitly define the value of `this` when calling a function.

When we use the `bind()` method:

1.  the JS engine is creating a new `pokemonName` instance and binding `pokemon` as its `this` variable. It is important to understand that **_it copies the pokemonName function._**
2.  After creating a copy of the `pokemonName` function it is able to call `logPokemon()`, although it wasn’t on the pokemon object initially. It will now recognizes its properties (_Pika_ and _Chu) and its methods._

And the cool thing is, after we bind() a value we can use the function just like it was any other normal function. We could even update the function to accept parameters, and pass them.

# **call(), apply()**
The `**call()**` method calls a function with a given `this` value and arguments provided individually.

What that means, is that we can call any function, and _explicitly specify what_ `_this_` _should reference_ within the calling function. Really similar to the `bind()` method! This can definitely save us from writing hacky code (even though we are all still hackerzzz).

The main differences between `bind()` and `call()` is that the `call()` method:

1.  Accepts additional parameters as well
2.  Executes the function it was called upon right away.
3.  The `call()` method does not make a copy of the function it is being called on.

`call()` and `apply()` serve the **exact same purpose.** The **_only difference between how they work is that_** call() expects all parameters to be passed in individually, whereas apply() expects an array of all of our parameters.