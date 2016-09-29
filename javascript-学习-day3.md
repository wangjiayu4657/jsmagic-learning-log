### 学习中遇到的问题

1. 创建 index.js，然后导出函数 greet应该使用如下方法

```
 module.export = function greet(name) {
     return "hello, " + name;
    }

```
否则当使用命令 :
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

2.当使用命令 `$ npm install -g .`安装全局的包时可能会遇到如下错误:

```
Error: Cannot find module 'greet'
 at Function.Module._resolveFilename (module.js:455:15)
 at Function.Module._load (module.js:403:25)
 at Module.require (module.js:483:17)
 at require (internal/module.js:20:19)
 at repl:1:1
 at sigintHandlersWrap (vm.js:22:35)
 at sigintHandlersWrap (vm.js:96:12)
 at ContextifyScript.Script.runInThisContext (vm.js:21:12)
 at REPLServer.defaultEval (repl.js:313:29)
 at bound (domain.js:280:14)

```
产生的原因是:
要知道，当你用 require 加载一个包时，node 会先在本地的 node_modules 目录里查找。如果它找不到这个包，它会继续到全局的 node_modules 目录里找。
所以，我们需要把全局的 node_modules 目录的位置告诉 node，这样 node 才会知道要到哪里去加载 nodemon。下一步，我们需要设置 NODE_PATH 环境变量

解决办法:
把以下内容添加到你的命令行配置文件：

```
# ~/.bashrc
export NODE_PATH=`npm root -g`
然后执行:
source ~/.bashrc使其生效即可
```
