# Lesson Workspace Higher Order Functions

## Objectives

* Use map to transform an array
* Use filter to transform an array
* Use reduce to accumulate an array
* Use functions that return functions to abstract functionality
* Define higher order functions

## Using this repo

To install

```bash
npm install
```

To run test

```bash
npm test
```

The tests are all passing, refactor the code without breaking the tests.

### How do you use map to transform an array?

In `array.map.js`

1. Study the three functions in the file and determine what the similarities and differences are between them.
1. For each function, create a function that maps the change of each element of the given array to the elements of the output array. See example below

```javascript
function increment(value){
  return value + 1
}

function addOne(array){
  const result = []

  for(const e of array){
    // abstract the transformation
    // instead of
    //   retVal.push(e + 1)
    // use the following
    result.push( increment(e) )
  }
  return result
}

addOne([ 1,2,3,4,5,6 ]) // [ 2,3,4,5,6,7 ]
```

1. Create a new function named `map`. And use it refactor `doubleNumbers`, `pluckName`, and `mailMerge`.

```javascript

// add this to `array.map.js` and complete the code.
function map(array, fn){
  // add code here
}

// existing code show to show how to use `map`
function increment(value){
  return value + 1
}

function addOne(array){
  return map(array, increment)
}

addOne([ 1,2,3,4,5,6 ]) // [ 2,3,4,5,6,7 ]

```

1. Refactor using `Array.prototype.map()`, you can find the documentation here, https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map
 * What arguments does the `.map()` method take?
 * Does it make a difference if `.map()` receives a named function versus an anonymous function? When would you choose to use which one?

### How do you use filter to transform an array?

In `array.filter.js`

* Create a function that checks to see if each value of the array should be pushed into `result`.
* Study the three main functions and determine what the similarities and differences are between them
* Create a function named `filter` that abstracts the looping structure, it has as arguments, an array and a function
* Add the `filter` function to all main functions
* Refactor using `array.filter`, bring in helper functions as anonymous functions

### How do you use reduce to accumulate an array?

In `array.reduce.js`

* Create a function to transform each element for each function
* Study the three main functions and determine what the similarities and differences are between them
* Create a function named `reduce` that abstracts the looping structure, it has as arguments, an array, a function, and a startign value
* Add `reduce` function to all main functions
* Refactor using `array.reduce`, bring in helper functions as anonymous functions

### How do you use a function that returns a function to abstract functionality?

In `array.map.js`

* From `functions-return-functions` use `multiplyBy` to abstract behavior on `doubleNumbers`
* From `functions-return-functions` use `pluckProperty` to abstract behavior on `pluckName`

In `array.filter.js`

* From `functions-return-functions` use `notDivisibleBy` to abstract behavior on `onlyOdds`
* In `functions-return-functions`, create a function named `scoreBelow` to abstract score number. Use it to abstract behavior in `hasBelow30000CareerPoints`
* In `functions-return-functions`, create a function named `startsWith` to abstract starting letter. Use it to abstract behavior in `firstNameStartsWithA`

In `array.reduce.js`

* rom `functions-return-functions` use `groupByProperty` to abstract behavior on `groupByUniversity`

### What is a higher order function?

* Turn you your neighbor and define what a higher order function is