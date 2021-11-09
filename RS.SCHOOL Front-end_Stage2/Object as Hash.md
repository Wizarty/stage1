Be able to loop through Object keys

Object.keys().forEach()

Object.keys(obj).forEach(function (key) {
   // do something with obj[key]
});


Iterators and Generators bring the concept of iteration directly into the core language and provide a mechanism for customizing the behavior of for...of loops.

For details, see also:

Iteration_protocols
for...of
function* and Generator
yield and yield*
Iterators
In JavaScript an iterator is an object which defines a sequence and potentially a return value upon its termination.

Specifically, an iterator is any object which implements the Iterator protocol by having a next() method that returns an object with two properties:

value
The next value in the iteration sequence.

done
This is true if the last value in the sequence has already been consumed. If value is present alongside done, it is the iterator's return value.

Once created, an iterator object can be iterated explicitly by repeatedly calling next(). Iterating over an iterator is said to consume the iterator, because it is generally only possible to do once. After a terminating value has been yielded additional calls to next() should continue to return {done: true}.

The most common iterator in JavaScript is the Array iterator, which returns each value in the associated array in sequence.

While it is easy to imagine that all iterators could be expressed as arrays, this is not true. Arrays must be allocated in their entirety, but iterators are consumed only as necessary. Because of this, iterators can express sequences of unlimited size, such as the range of integers between 0 and Infinity.

Here is an example which can do just that. It allows creation of a simple range iterator which defines a sequence of integers from start (inclusive) to end (exclusive) spaced step apart. Its final return value is the size of the sequence it created, tracked by the variable iterationCount.