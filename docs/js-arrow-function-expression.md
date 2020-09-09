---
title: JavaScript Arrow Function Expression
icon: 😜
---

The [arrow function expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) (=>) creates anonymous functions who do not have their `this`, `arguments`, `super`, or `new.target` set.  This is especially useful for callbacks where you don’t need all that state.

```js
[1,2,3].forEach( num => {
  // Do something with num.
});

const someFunc = () => { /* do stuff */ };
someFunc();
```
