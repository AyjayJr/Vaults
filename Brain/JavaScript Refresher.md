![[next-gen-js-summary.pdf]]

---
## Import / Export

- You can export objects and functions using the export keyword
- Using the default keyword you can select the default item that gets exported
- You can use the import keyword to import these in another file

Syntax is as follows:
- import person from 'person.js' <- this will always import the default export
- import { baseData } from 'utility.js' <- imports the variable baseData, i.e. a named import
- import { baseData as bd } from 'utility.js' <- renames the variable on import
- import * as bundled from 'utility.js' <- creates an object that contains all exports as a property

## Classes

- Needs constructor
- Can have properties and methods
- Can be inherited using the extends keyword
	- Inherited classes need to user super() function in constructor
	- Super() executes the parent constructor

Classes are used in React to create the components

## Spread and Rest operators

both operators use the same syntax '...'
whether they are called spread or rest depends on their usage

Spread: used to split up array elements or object properties
Rest: used to merge a list of function arguments into an array
- useful when you may receive more than one argument into a function
- allows you to use array methods on incoming arguments

## Destructuring

Easily extract array elements or object properties and store them in variables.

Array Destructuring, also allows you to set values of multiple variables at once
[a, b] = ['Hello', 'World!']

Object Destructuring
{name} = {name: 'Max', age: 28}
- allows you to pull out specified property from an object

## Reference vs primitive types

Numbers, strings, and booleans are Primitive types. They will create a copy of each other when stored in a new variable.

Objects and arrays are Reference types. Basically pointers from C. They do not create a copy they point to the original instance of the object/array. Use the spread operator to create a new copy of an object or array.

## Array functions

Some functions such as map() and filter() take an arrow function and execute said function on each element of the array.