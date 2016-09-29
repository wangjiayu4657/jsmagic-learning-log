#### 创建一个 babel.js 文件



 - 终端通过命令:

```
 $ touch babel.js

```

 - 编辑该文件:

```
 $ vi babel.js

```

 注意:进入 babel.js文件后点击 i 进入编辑模式,编辑完成后先点击'esc'按键 然后输入':wq'保存退出即可.

#### 配置 PATH环境变量

现在我们想更加简短地执行 babel 命令：


```
$ babel --version

6.14.0 (babel-core 6.14.0)

```

```
$ babel-node --version

6.14.0

你可能会得到以下错误 command not found 错误：

```

```

$ babel --version

command not found: babel

```
这时候你就需要配置你的命令行环境了。尝试打印 PATH 环境变量：


```
$ echo $PATH

/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:./node_modules/.bin

```

如果你在输出结果中没有找到 ./node_modules/.bin，那么你需要这样修改下面的文件：


```
# 在 ~/.bashrc 中

export PATH=$PATH:./node_modules/.bin

# 在 ~/.bash_profile 中

source ~/.bashrc

```
































