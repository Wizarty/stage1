#custom_sorting_for_Array

Be able to custom sorting for Array :

array.sort(function(x, y) {
  if (x < y) {
    return -1;
  }
  if (x > y) {
    return 1;
  }
  return 0;
});


const numberSorted = numberArr.sort((a, b) => {
  if(a < 0 && b < 0) {
    return a - b
  } else if(a < 0 || b < 0) {
    return b - a
  } else {
    return a - b
  }
})

const descSort = numberArr.sort((a, b) => {
  return b - a
})

Be able to filter Array elements :

Using .filter()

function arrayFilter(arr, func) {
  let filteredArray = arr.filter(func);
  return filteredArray[0] ? filteredArray[0] : undefined;
}

An Imperative approach

function arrayFilter(arr, func) {
  for (let elem of arr) {
    if (func(elem)) {
      return elem
    }
  }
  return undefined
}

Using .find()
function arrayFilter(arr, func) {
  return arr.find(func)
}


// Arrow function
filter((element) => { ... } )
filter((element, index) => { ... } )
filter((element, index, array) => { ... } )

// Callback function
filter(callbackFn)
filter(callbackFn, thisArg)

// Inline callback function
filter(function(element) { ... })
filter(function(element, index) { ... })
filter(function(element, index, array){ ... })
filter(function(element, index, array) { ... }, thisArg)
Copy to Clipboard
Parameters
callbackFn
Function is a predicate, to test each element of the array. Return a value that coerces to true to keep the element, or to false otherwise.

It accepts three arguments:

element
The current element being processed in the array.

indexOptional
The index of the current element being processed in the array.

arrayOptional
The array on which filter() was called.

thisArgOptional
Value to use as this when executing callbackFn.

Return value
A new array with the elements that pass the test. If no elements pass the test, an empty array will be returned.