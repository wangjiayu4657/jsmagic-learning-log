### 学习中遇到的问题

创建 index.js，然后导出函数 greet应该使用如下方法

```
 module.export = function greet(name) {
     return "hello, " + name;
    }

```
否则当使用命令 :
``` 
    $node
    > greet("howard");
```
会报如下错误:

```
TypeError: greet is not a function
 at repl:1:1
 at sigintHandlersWrap (vm.js:22:35)
 at sigintHandlersWrap (vm.js:96:12)
 at ContextifyScript.Script.runInThisContext (vm.js:21:12)
 at REPLServer.defaultEval (repl.js:313:29)
 at bound (domain.js:280:14)
 at REPLServer.runBound [as eval] (domain.js:293:12)
 at REPLServer.<anonymous> (repl.js:513:10)
 at emitOne (events.js:101:20)
 at REPLServer.emit (events.js:188:7)

```