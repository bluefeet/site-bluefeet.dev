---
title: JS Object Initializer Notation
icon: ✒️
tags:
  - javascript
---

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
