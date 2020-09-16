---
title: JavaScript
icon: 📜
---

## Arrow Function Expression

The [arrow function expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) (=>) creates anonymous functions who do not have their `this`, `arguments`, `super`, or `new.target` set.  This is especially useful for callbacks where you don’t need all that state.

```js
[1,2,3].forEach( num => {
  // Do something with num.
});

const someFunc = () => { /* do stuff */ };
someFunc();
```

## for Loops

Iterating over elements in an array using [for...of](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of):

```js
for (const thing of things) { /* ... */ }
```

Iterating over elements in an array using [forEach](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach):

```js
things.forEach( thing => { /* ... */ } );
```

Iterating over elements in an array using [for](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for):

```js
for (let i=0; i<things.length; i++) { /* ... */ }
```

Iterate over the properties in an object using [for...in](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in):

```js
for (const property in thing) { /* ... */ }
```

Iterate over the properties in an object using [Object.keys()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for) and [forEach](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach):

```js
Object.keys( thing ).forEach( property => { /* ... */ });
```

## Modules

### CommonJS

Setup exports with the `module.exports` object:

```js
module.exports = { someFunc1, someFunc2 };
```

Import a module with the `require` function:

```js
let { someFunc1 } = require('path/to/module');
```

### ES6

Export things:

```js
// One at a time.
export someFunc1;
export someFunc2;

// Or all together:
export { someFunc1, someFunc2 };

// Or export a single default:
export default mainFunc;
```

Import things:

```js
import { someFunc1, someFunc2 } from 'path/to/module';

// You can also import everything.
import * as variableName from 'path/to/module';

// Use as to alias an import:
import { someFunc1 as myFunc } from 'path/to/module';

// Import the default export:
import variableName from 'path/to/module';
```

## Multiple Variable Assignment

This creates the variable `a` and `b` from the left side and assigns them to the value of the same-named object key on the right.

```js
let { a, b } = { a:32, b:45 };
```

This does the same with an array:

```js
let [ a, b ] = [ 32, 45 ];
```

When using object notation you can alias keys to a different variable name:

```js
let { b:bbb } = { a:32, b:45 };
```

The above creates a `bbb` variable which has the value `45`.

## Object Initializer Notation

The official syntax for the [object initializer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer):

```js
let o = {
  key: value,
  variable, // Shorthand for: variable: variable
  property: function (parameters) {},
  property (parameters) {}, // Shorthand for the above.
  get property() {},
  set property(value) {},
  ["a"+"b"]: 'A computed key of ab.'
};
```

These two lines are the same:

```js
let someObj = { a, b };
let someObj = { a:a, b:b };
```

## Prototype and Constructor Inheritance

Given:

```js
function Animal () {}
function Human () {}
Human.prototype.__proto__ = Animal.prototype;
var person = new Human();
```

Then:

```js
person.__proto__ === Human.prototype;
person.constructor === Human;

Human.prototype.constructor === Human;
Human.prototype.__proto__ === Animal.prototype;

Animal.prototype.constructor === Animal;
Animal.prototype.__proto__ === Object.prototype;
```

## Spread Syntax

The [spread syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax) takes an array or object and expands it into its elements/properties.

These two lines are identical:

```js
let foo = [ 1, 2, 3 ];
let foo = [ ...[1, 2, 3] ];
```
A shallow clone of an object:

```js
const clone = { ...someObject };
```

Building arguments with defaults:

```js
const args = { defKey: 'defVal', ...customArgs }; // Right side wins.
```

## Rest Parameters

[Rest parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters) are used to gather multiple arguments to a function into a single array.

```js
function bar (firstNum, ...nums) { /* nums is [2,3] */ }
bar( 1, 2, 3 );
```

## Cascading Inherited Arguments

Spread syntax and rest parameters, together, provide the ability to cascade arguments:

```js
function doThingA (firstArg, ...args) {
  firstArg = this.modifyFirstArg( firstArg );
  return this.doThing( firstArg, ...args );
}
```
