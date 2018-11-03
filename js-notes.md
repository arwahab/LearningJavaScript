# JavaScript notes

## Logging to console:
* done using 'console.log'

## Variables & Types
* JS is a 'duck-typed language'
* every variable defined using `var` keyword
* `var` can contain all types of variables
* ex: `var myNumber = 3;`
* `var myString = "Hello, World";`
* `var myBoolean = true;`
* in JS,  the `Number` type can be BOTH floating point number & an integer
* Boolean variables can only be equal to either true or false (known)

### Variables - advanced types
* Arrays & Objects exist as well
* ex: `var myArray = [];`
* ex: `var myObject = {};`

### Variables - undefined & null
* When a variable used w/o defining a value for it, it is equal to `undefined`
* ex: `var newVariable;`
* `console.log(newVariable);`  // prints 'undefined'
* `null` different type of value, used when variable should be marked as empty
* undefined can be used for this purpose but it should NOT be used
* ex: `var emptyVariable = null;`
* `console.log(emptyVariable);` // prints 'null'

## Arrays
* JS can hold an array of variables in an Array object
* In JS, array also functions as a list, a stack, or a queue
* Ways to define an array ex:
* `var myArray = [1, 2, 3];`
* `var theSameArray = new Array(1, 2, 3);`

### Arrays - Addressing
* We can use square brackets `[]` to address a specific cell in array
* Like Java, addressing uses zero-based indices
* ex: `console.log(myArray[1])` // prints 2
* Arrays in JS are sparse, aka we can also assign variables to random locations even tho previous cells were `undefined`
* ex: `var myArray = [];`
* `myArray[3] = "hello";`
* `console.log(myArray)`;
* this prints: `, , , hello`

### Arrays - Manipulation via `push()` and `pop()`
* Arrays can fxn as `stacks`
* `push` and `pop` methods used to insert and remove variables from the END of an Array
* ex: here's an empty array where we push variables
* `var myStack = [];`
* `myStack.push(1);`
* `myStack.push(2);`
* `myStack.push(3);`
* `console.log(myStack)`;
*  Prints: `1,2,3`

* After pushing, we can `pop` variables off from the end of the array
* ex:
* `console.log(myStack.pop());`
* `console.log(myStack)`;
*  Prints:
* `3` // result from the one myStack.pop() we did
* `1,2` // now is what myStack contains

### Arrays - Queues using `shit()` and `unshift()`
* `shit()` and `unshift()` similar to `push()` and `pop()` except they work fro BEGINNING of the array.
* `push()` and `shift()` methods can be used consecutively to utilize an array as a queue. ex:
* `var myQueue = [];`
* `myQueue.push(1);`
* `myQueue.push(2);`
* `myQueue.push(3)`
* `console.log(myQueue.shift());`
* `console.log(myQueue.shift());`
* `console.log(myQueue.shift());`

* Above code prints:
* `1`
* `2`
* `3`

* `unshift()` method used to insert variables at BEGINNING of array. ex:

* `var myArray = [1,2,3];`
* `myArray.unshift(0);`
* `console.log(myArray)`

* Above code prints: `0,1,2,3`

### Arrays - Splicing
* Splicing arrays in JS removes certain part of an array to create a NEW array, made up from the part we took

* ex:
* `var myArray = [0,1,2,3,4,4,5,6,7,8,9];`
* `var splice = myArray.splice(3,5);`
* `console.log(splice)`  // prints out 3,4,5,6,7
* `console.log(myArray)` // prints out 0,1,2,8,9

* After splicing the array, it will ONLY contain the part BEFORE & AFTER the splicing. The splice is equal to ALL VARIABLES between `3 and 7 (inclusive)` and the remainder of the array which contains ALL variables between  `0 and 2 (inclusive), and 8 to 9 (inclusive).`

## Operators
*
