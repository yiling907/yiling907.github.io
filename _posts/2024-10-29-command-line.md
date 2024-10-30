---
title: Command Line
date: 2024-10-29 10:30:09 +0800
categories: [Blogging]
tags: [command]
---

# 概念

1. 控制台：控制台（console）是允许你与计算机互动的**物理设备，键盘鼠标屏幕。**
2. 终端：终端是一个文本输入和输出环境。它是作为一个**包装器（wrapper）** 的**程序**，允许我们输入计算机处理的命令。（是输入输出的窗口）
3. shell：shell 是一个**程序**，作为命令行解释器。它**处理命令**并**输出结果**。它解释和处理用户输入的命令。shell 运行在终端上。
    1. 在大多数 Linux 和 Mac 操作系统中，默认的 shell 是 Bash。
    2. 而在 Windows 中则是 Powershell。
    3. 其他一些常见的 shell 的例子是 Zsh 和 Fish。
4. **命令行（CLI）：**这实际上与终端（terminal）是一样的，在我看来，这些术语可以互换使用。

# 优势

1. 高效率
2. 自动化
3. 有时 CLI 将是我们能够与计算机互动的唯一方式。例如，当你需要与云平台服务器互动时。在大多数情况下，你不会有一个 GUI，只有一个 CLI 来运行命令。

# 不同的shell

使用命令判断当前使用的是哪个shel

```jsx
echo $0

bash aliases（别名）// 重命名shell脚本名称
```

## Shell命令分类

1. 系统命令：操作系统默认自带的
2. 第三方命令：用户在实际使用过程中使用apt-get install或yum install命令安装的第三方工具
3. 内建命令：这些是在[shell](https://www.zhaixue.cc/shell/shell-intro.html)内部实现的，

执行命令本质：当用户在[shell](https://www.zhaixue.cc/shell/shell-intro.html)交互环境下敲击命令的名字时，[shell](https://www.zhaixue.cc/shell/shell-intro.html)就会到PATH指定的这些路径下去寻找这个可执行文件，创建一个子进程，将可执行文件的代码加载到子进程的地址空间执行。

命令所在路径与命令类型有关

### 环境变量优先级

类型：

1. 系统环境变量：在系统范围内定义（如 `/etc/environment`, `/etc/profile` 等），对所有用户有效。
2. 用户环境变量：通常在用户的配置文件中定义（如 `.bashrc`, `.bash_profile`, `.zshrc` 等），这些变量仅对特定用户有效。
3. 临时环境变量：在当前会话中设置的变量（如通过 `export` 命令），在会话结束后失效。

优先级：

1. 临时变量 > 用户级变量 > 系统级变量
2. 在脚本中定义的变量优先于外部环境变量（仅在脚本内有效）。

相关指令：

`.bashrc`, `.bash_profile`, `.zshrc`

1. 查看当前使用的 Shell：echo $SHELL
2. 查看当前生效的所有的环境变量：printenv 或者 env
3. 查看当前生效的PATH：echo $PATH
4. 环境变量生效：source ~/.bashrc
5. 查看启动时生效的配置文件：shopt | grep login

登录shel：

当你通过终端或远程连接（如 SSH（登录服务器 虚拟机））登录到系统时，启动的 Shell 称为登录 Shell。

# 参考：

[面向初学者的命令行教程——如何像专业人士一样使用终端](https://www.freecodecamp.org/chinese/news/command-line-for-beginners/)

[shell 管道 - shell 简明教程 | 宅学部落](https://www.zhaixue.cc/shell/shell-pipe.html)