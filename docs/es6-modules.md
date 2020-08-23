---
title: ES6 Modules
icon: 🥜
tags:
  - javascript
  - es6
---

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
