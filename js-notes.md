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
* Every variable in JS is casted automatically, so any operator b/w 2 variables will ALWAYS give some kind of result

### Operators - addition
* the `+` (addition) operator used for both numerical addition & concantenation of strings
* ex:
* `var a = 1;`
* `var b = 2;`
* `var c = a + b;`   // c = 3

* Here's string concantenation:
* `var name = "John";`
* `console.log("Hello " + name + "!");` // Hello John!
* `console.log("The meaning of life is " + 42);` // The meaning of life is 42
* `console.log(42 + " is the meaning of life");` // 42 is the meaning of life

### Operators - other math operators
*  subtract, multiply, and divide
* `console.log(3 - 5);`  // outputs -2
* `console.log(3 * 5);`  // outputs 15
* `console.log(3 / 5);`  // outputs 0.6
* `console.log(5 % 3);`  // outputs 2

### Operators - assignment & operation operators
* JS also supports combined assignment and operation operators. Aka, instead of `myNumber = myNumber / 2` one can do `myNumber /= 2`
* List of operators:
* `/=`
* `*=`
* `-=`
* `+=`
* `%=`
* Some `Math` operators:
* `Math.abs` for absolute value
* `Math.exp` calculates e to the power of a #
* `Math.pow(x,y)` does x^(y)
* `Math.floor` removes fractional part of #
* `Math.random` gives random # x where 0<=x<1

## Conditions - `if` statements and `switch` statements
* ex:
* `if (confirm("Are you John Smith?"))`
* `{`
* `console.log("Hello John, how are you?");`
* `} else {`
* `console.log("Then what is your name?");`
* `}`
* Its possible to omit the `else` keyword if we just want to run a block of code ONLY if a certain expression is true. Use `==` to see if 2 variables are equal.
* ex:
* `var foo = 1;`
* `var bar = 2;`

* `if (foo < bar)`
* `{`
*    `console.log("foo is smaller than bar.");`
* `}`

* ex: `switch` statement
* `var rank = "Commander";`
* `switch(rank)`
* `{`
*    `case "Private":`
*    `case "Sergeant":`
*        `console.log("You are not authorized.");`
*        `break;`
*    `case "Commander":`
*        `console.log("Hello commander! what can I` * `do for you today?");`
*       `break;`
*    `case "Captain":`
*        `console.log("Hello captain! I will do`
* `anything you wish.");`
*        `break;`
*    `default:`
*        `console.log("I don't know what your rank` * `is.");`
*        `break;`
* `}`

## Loops

### Loops - the `for` loop
* here's a simple example:
* `var i;`
* `for (i = 0; i < 3; i = i + 1)`
* `{`
* `console.log(i);`
* `}`
* Above ex prints this:
* `0`
* `1`
* `2`
* `for` has same syntax as in Java & C
* can also put `var` in loop ex:
* `for (var i = 0; i < 3; i++)`
* `{`
* `console.log(i);`
* `}`
* ex iterating over array and printing it
* `var myArray = ["A", "B", "C"];`
* `for (var i = 0; i < myArray.length; i++)`
* `{`
* `console.log("The member of myArray in index " + i + " is " + myArray[i]);`
* `}`
* Above ex prints this:
* `The member of myArray in index 0 is A`
* `The member of myArray in index 1 is B`
* `The member of myArray in index 2 is C`
### Loops - the `while` loop
* 
