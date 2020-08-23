---
title: JS Prototype and Constructor Inheritance
icon: 👨‍👩‍👧‍👦
tags:
  - javascript
  - inheritance
---

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
