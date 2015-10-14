
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
-
-window.Zepto = Zepto
-'$' in window || (window.$ = Zepto)
-
-
-
+// @@ original loader
+// window.Zepto = Zepto
+// '$' in window || (window.$ = Zepto)
+// @@ modified by shinygang
+module.exports.$ = Zepto;
+module.exports.Zepto = Zepto;
+// @@ modifications end
```