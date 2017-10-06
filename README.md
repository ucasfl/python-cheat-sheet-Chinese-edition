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

4. **str**：在 Python 2 中默认以 ASCII 编码，而在 Python 3 中默认以 Unicode 编码；

   - 字符串可置于单/双/三引号中；
   - 字符串是字符的序列，因此可以像处理其他序列一样处理字符串；
   - 特殊字符可通过 `\` 或者前缀 `r` 实现：

   ```python
   str1 = r'this\f?ff'
   ```

   - 字符串可通过多种方式格式化：

   ```python
   template = '%.2f %s haha $%d';
   str1 = template % (4.88, 'hola', 2)
   ```

5. **NoneType(None)**：Python `null` 值（只有 None 对象的一个实例中存在）。

   - `None` 不是一个保留关键字，而是 **NoneType** 的一个唯一实例。
   - `None` 通常是可选函数参数的默认值：

   ```python
   def func1(a, b, c = None)
   ```

   - `None` 的常见用法：

   ```python
   if variable is None :
   ```

6. **datatime**：Python 内建的 datetime 模块提供了 `datetime`、`data` 以及 `time` 类型。

   - `datetime` 组合了存储于 `date` 和 `time` 中的信息。


```python
#从字符串中创建 datetime
dt1 = datetime.strptime('20091031', '%Y%m%d')
#获取 date 对象
dt1.date()
#获取 time 对象
dt1.time()
#将 datetime 格式化为字符串
dt1.strftime('%m/%d/%Y%H:%M')
#更改字段值
dt2 = dt1.replace(minute = 0, second = 30)
#做差, diff 是一个 datetime.timedelta 对象
diff = dt1 - dt2
```

**注：Python 中的绝大多数对象都是可变的，只有字符串和元组例外。**

## 数据结构

**注：所有的 non-Get 函数调用，比如下面例子中的 `list1.sort()` 都是原地操作，即不会创建新的对象，除非特别声明。**

### 元组

元组是 Python 中任何类型的对象的一个一维、固定长度、不可变的序列。

```python
#创建元组
tup1 = 4, 5, 6 
# or
tup1 = (6, 7, 8)
#创建嵌套元组
tup1 = (4, 5, 6), (7, 8)
#将序列或迭代器转化为元组
tuple([1, 0, 2])
#连接元组
tup1 + tup2
#解包元组
a, b, c = tup1
```

元组运用：

```python
#交换两个变量的值
a, b = b, a
```



### 列表

列表是 Python 中任何类型的对象的一个一维、非固定长度、可变（比如内容可以被修改）的序列。










