
This is a fork based on [madrobby/zepto](https://github.com/madrobby/zepto).

```
npm install --save commonjs-zepto
```

```js
$ = require('commonjs-zepto').$
Zepto = require('commonjs-zepto').Zepto
$ === Zepto // true
```

How I made this:

```
git rm *json zepto.min.js Makefile
npm init
subl zepto.js
subl README.md
git diff zepto.js
```

```diff
+// @@ modified by shinygang
+ else if (typeof exports === 'object')
+   module.exports = factory(global)
+// @@ modifications end
```