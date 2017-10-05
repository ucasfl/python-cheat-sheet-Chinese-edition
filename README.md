Python 速查表中文版
===
[TOC]

本手册是 [Python cheat sheet](http://datasciencefree.com/python.pdf) 的中文翻译版。原作者：Arianne Colton and Sean Chen(data.scientist.info@gmail.com)

## 惯例

- Python 对大小写敏感；
- Python 的索引从 0 开始（所有编程语言均如此）；
- Python 使用空白符（制表符或空格）来缩进代码，而不是使用花括号。

## 获取帮助

- 获取主页帮助： `help`
- 获取函数帮助： `help(str.replace)`
- 获取模块帮助： `help(re)`

## 模块（亦称库）

模块只是一个简单地以 `.py` 为后缀的文件。

- 列出模块内容：`dir(module1)`
- 导入模块：`import module1 *`
- 调用模块中的函数：`module1.func1()`

**注：`import` 语句会创建一个新的名字空间，并且在该名字空间内执行 `.py` 文件中的所有语句。如果你想把模块内容导入到当前名字空间，请使用 `from module1 import *` 语句。**

## 数值类类型

查看变量的数据类型：`type(variable)`

### 六种经常使用的数据类型

1. **int/long**：过大的 `int` 类型会被自动转化为 `long` 类型。
2. **float**：64 位，Python 中没有 `double` 类型。
3. **bool**：真或者假。
4. ...









