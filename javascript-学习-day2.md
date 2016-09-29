### 学习中遇到的问题





```
➜ $ babel-node

> const {pi,e} = require("./constants");

SyntaxError: repl: Only `var` variables are supported in the REPL

> 1 | const {pi,e} = require("./constants");

 | ^

```


- 当输入`babel-node`再接着在输入`> const {pi,e} = require("./constants");`后报了

`SyntaxError: repl: Only `var` variables are supported in the REPL`这个错误

解决办法:是将 const 改为 var 即可








