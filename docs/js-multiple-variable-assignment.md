---
title: JavaScript Multiple Variable Assignment
icon: 🌗
---

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
