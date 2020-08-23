---
title: JS Spread Syntax and Rest Parameters
icon: 🌳
tags:
  - javascript
---

The [spread syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax) takes an array or object and expands it into its elements.  So these two lines are identical:

```js
let foo = [ 1, 2, 3 ];
let foo = [ ...[1, 2, 3] ];
```

[Rest parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters) are used to gather multiple arguments to a function into a single array.

```js
function bar (firstNum, ...nums) { /* nums is [2,3] */ }
bar( 1, 2, 3 );
```

Spread syntax and rest parameters, together, provide the ability to cascade arguments:

```js
function doThingA (firstArg, ...args) {
  firstArg = this.modifyFirstArg( firstArg );
  return this.doThing( firstArg, ...args );
}
```

The spread syntax may be used with objects.  For example, a shallow clone:

```js
let clone = { ...someObject };
```