# 1.TypeScript
This is a repository for me to record the process of learning TypeScript.

## 初识

TypeScript 是 JavaScript 的一个超集，支持 ECMAScript 6 标准。

TypeScript 由微软开发的自由和开源的编程语言。

TypeScript 设计目标是开发大型应用，它可以编译成纯 JavaScript，编译出来的 JavaScript 可以运行在任何浏览器上。

## JavaScript 与 TypeScript 的区别

TypeScript 是 JavaScript 的超集，扩展了 JavaScript 的语法，因此现有的 JavaScript 代码可与 TypeScript 一起工作无需任何修改，TypeScript 通过类型注解提供编译时的静态类型检查。

TypeScript 可处理已有的 JavaScript 代码，并只对其中的 TypeScript 代码进行编译。

# 2.安装

## NPM 安装 TypeScript

如果你的本地环境已经安装了 npm 工具，可以使用以下命令来安装。

使用国内镜像：

```
npm install -g cnpm --registry=https://registry.npmmirror.com
```

安装 typescript：

```
npm install -g typescript
```

安装完成后我们可以使用 **tsc** 命令来执行 TypeScript 的相关代码，以下是查看版本号：

```
$ tsc -v
Version 3.2.2
```

然后我们新建一个 app.ts 的文件，代码如下：

```
var message:string = "Hello World"  console.log(message)
```

通常我们使用 **.ts** 作为 TypeScript 代码文件的扩展名。

然后执行以下命令将 TypeScript 转换为 JavaScript 代码：

```
tsc app.ts
```

这时候在当前目录下（与 app.ts 同一目录）就会生成一个 app.js 文件，代码如下：

```
var message = "Hello World"; console.log(message);
```

使用 node 命令来执行 app.js 文件：

```
$ node app.js 
Hello World
```

# 3.解决VSCODE报错

1. 解决VSCODE"因为在此系统上禁止运行脚本"报错，以管理员身份运行vscode;

2. 执行：get-ExecutionPolicy，显示Restricted，表示状态是禁止的;

3. 执行：

```
set-ExecutionPolicy RemoteSigned
```

4. 这时再执行get-ExecutionPolicy，就显示RemoteSigned;

# 4.VSCODE自动编译TS

初始化 生成tsconfig.json文件 

```
tsc --init
```

打开tsconfig.json设置生成js地址

```
"outFile": "./", 
```

快捷键 Ctrl+shift+B 选择监视模式 进行编译（每次有更新就会编译）

# 5.愉快地写代码……
