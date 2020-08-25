---
title: Node's console.log
icon: 📋
tags:
  - javascript
  - node
---

```js
Console.prototype.log = function() {
  this._stdout.write(util.format.apply(this, arguments) + '\n');
};
```
