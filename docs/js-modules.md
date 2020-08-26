---
title: JavaScript Modules
icon: 🥜
tags:
  - javascript
  - commmonjs
  - es6
---

## CommonJS

Setup exports with the `module.exports` object:

```js
module.exports = { someFunc1, someFunc2 };
```

Import a module with the `require` function:

```js
let { someFunc1 } = require('path/to/module');
```

## ES6

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