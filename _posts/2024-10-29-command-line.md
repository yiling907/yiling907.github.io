---
title:Command Line
date: 2024-10-29 10:30:09 +0800
categories: [Blogging]
tags: [command]
---

[面向初学者的命令行教程——如何像专业人士一样使用终端](https://www.freecodecamp.org/chinese/news/command-line-for-beginners/)

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
