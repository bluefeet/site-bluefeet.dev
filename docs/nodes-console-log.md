---
title: Node's console.log
icon: 📋
---

```js
Console.prototype.log = function() {
  this._stdout.write(util.format.apply(this, arguments) + '\n');
};
```
