---
title: JavaScript for Loops
icon: 🎡
tags:
  - javascript
---

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
