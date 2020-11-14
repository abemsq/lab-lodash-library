# Javascript Intermediate Exercise: Recreating Lodash Library

In this project, you will be implementing some of the most exciting functionality from the widely-popular lodash.js library. You will be implementing ten methods that add new functionality for numbers, strings, objects, and arrays.

In implementing each method, we will follow these four steps:

Specify the functionality of the method we are implementing
Ideate a game plan for how to implement this functionality in code
Implement our game plan
Test our code to ensure it works as expected
We encourage you to try to complete the “Ideate” and “Implement” steps on your own before consulting our suggestions for each. It may be difficult at points, but working through difficult problems on your own will be incredibly helpful in your journey to become a stronger developer. Once you’ve come up with a solution on your own, or if you have become so stuck you are no longer being productive, check out our steps to see our suggestions for how to solve the problem.

There is no right or wrong answer when it comes to programming. As a result, don’t be frustrated if the solution we present is different than the solution you came up with. We are merely trying to challenge you to consider many different solutions. Your solution is equally as valid as ours. Consider the one you were going to write and then consider ours. Whichever you pick in the end is completely your decision, and we support it completely.

You have the choice of writing this project within the Codecademy environment to the right or locally on your own computer by downloading the starting code here. Feel free to proceed in whichever environment you are most comfortable with.

With all of that said, let’s get started implementing some awesome new functionality!

```
const _ = {

clamp (number, lower, upper) {
  const lowerClampedValue =
 Math.max(number, lower);
const clampedValue = Math.min(lowerClampedValue, upper);
return clampedValue;
},
  
inRange (number, start, end) {
 if (end === undefined) {
 end = start;
 start = 0
 }
 if (start > end) {
    const temp = end; 
    end = start;
    start = temp
  }
  const isInRange =
  (number >= start && number < end) 
 return isInRange
},  
words (string) {
  const words = string.split(' ')
  return words
},
pad (string, length) {
  if (length < string.length) {
    return string
  }
  const startPaddingLength = Math.floor((length - string.length)/2)
  const endPaddingLength = (length - string.length - startPaddingLength)
  const paddedString = ' ' .repeat(startPaddingLength) + string + ' ' .repeat(endPaddingLength)
  return paddedString
},
has (object, key) {
  var hasValue = object[key];
  if (hasValue !== undefined) {
    return true
  }
else {
  return false
}
},
invert (object) {
  let invertedObject = {}
  for (let key in object) {
    let originalValue = object[key]
  invertedObject = {originalValue: key}
  }
  return invertedObject;
},
findKey (object, predicate) {
  for (let key in object) {
    let value = object[key]
        if (predicate(object[key])) {
          return key
        } 
  } 
},
drop (array, number) {
    if (number === undefined) {
      let number = 1
      return array.slice(number, array.length)
    }
    let dropArray = array.slice(number, array.length)
    return dropArray
  },
dropWhile (array, predicate) {
  const callback = (element, index) => {
  return !predicate(element, index, array) }
  let dropNumber = array.findIndex(callback);
  let droppedArray = this.drop(array, dropNumber);
  return droppedArray
},
chunk (array, size) {
  if (size === undefined) {
    let size = 1
  }
  let arrayChunks = [];
  for (let i = 0; i<array.length; i+ size) {
  let arrayChunk = array.slice(i, i+= size);
      arrayChunks.push(arrayChunk)
  } return arrayChunks;
}
}

// Do not write or modify code below this line.
module.exports = _;
```
