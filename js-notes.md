# JavaScript notes

## Logging to console:
* done using 'console.log'

## Variables & Types
* JS is a 'duck-typed language'
* every variable defined using 'var' keyword
* 'var' can contain all types of variables
* ex: var myNumber = 3;
* var myString = "Hello, World";
* var myBoolean = true;
* in JS,  the Number type can be BOTH floating point number & an integer
* Boolean variables can only be equal to either true or false (known)

### Variables - advanced types
* Arrays & Objects exist as well
* ex: var myArray = []
* ex: var myObject = {};

### Variables - undefined & null
* When a variable used w/o defining a value for it, it is equal to undefined
* ex: var newVariable;
* console.log(newVariable);  // prints 'undefined'
* null different type of value, used when variable should be marked as empty
* undefined can be used for this purpose but it should NOT be used
* ex: var emptyVariable = null;
* console.log(emptyVariable); // prints 'null'
