# map and filter over arrays

## Objectives

* Use map to transform an array
* Use filter to transform an array
* Explain how filter and map abstract over arrays.

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

1. Study the `doubleNumbers`, `pluckName`, and `mailMerge` functions in the file, and determine what the similarities and differences are between them.
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

1. Create a new function named `map`. And use it refactor `doubleNumbers`, `pluckName`, and `mailMerge`. See example below.

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

1. Study the `onlyOdds`, `hasBelow30000CareerPoints`, and `firstNameStartsWithA` functions in the file, and determine what the similarities and differences are between them.
1. For each function, create a function that maps the change of each element of the given array to the elements of the output array. See example below

```javascript
function isLessThan10(value){
  return value < 10
}

function keepLessThan10(array){
  const result = []

  for(const e of array){
    // abstract the transformation
    // instead of
    //   if( e < 10 )
    // use the following
    if( isLessThan10(e) ){
      result.push( e )
    }
  }
  return result
}

keepLessThan10([ 5,7,8,9,10,11,12,13  ]) // [ 5,7,8,9 ]
```

1. Create a new function named `map`. And use it refactor `onlyOdds`, `hasBelow30000CareerPoints`, and `firstNameStartsWithA`. See example below.

```javascript

// add this to `array.filter.js` and complete the code.
function filter(array, fn){
  // add code here
}

// existing code show to show how to use `map`
function isLessThan10(value){
  return value < 10
}

function keepLessThan10(array){
  return filter(array, isLessThan10)
}

keepLessThan10([ 1,2,3,4,5,6 ]) // [ 2,3,4,5,6,7 ]

```

1. Refactor using `Array.prototype.filter()`, you can find the documentation here, https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter
 * What arguments does the `.filter()` method take?
 * Does it make a difference if `.filter()` receives a named function versus an anonymous function? When would you choose to use which one?


### How do `map` and `filter` abstract over arrays?

* Turn you your neighbor and answer the follwing:
  * What is abstraction? and why is is useful?
  * How does `map` and `filter` use abstraction?