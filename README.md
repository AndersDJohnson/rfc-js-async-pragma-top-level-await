# rfc-js-async-scripts

In order to use `await`, you need to be inside an `async` function.

For scripting purposes, this is cumbersome:

```js

(async () => {
  const foo = await bar()
  
  // ...
})()
```

JavaScript should support making a whole file async by default, either as a pragma comment, like `// @flow`:

```js
// @async

const foo = await bar()

// ...
```

or a directive prologue, like `'use strict';`:

```js
'async';

const foo = await bar()

// ...
```

or even a keyword:

```js
async

const foo = await bar()

// ...
```

May be possible to implement as a Babel transform plugin.
