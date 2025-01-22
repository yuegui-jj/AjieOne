### Python

#### 一、基础语法：

##### 1.字符串：

（1）字符串可以用 + 运算符连接在一起，用 * 运算符重复。

*e.g.  a = “xy”，b = “z”,a+b = “xyz”，a * 3 = “xyxyxy”*

（2）Python 中的字符串有两种索引方式，从左往右以 **0** 开始，从右往左以 **-1** 开始。

（3）Python 中的字符串不能改变。

详见：[python字符串为什么不能修改_Python中的字符串的不可改变以及间接修改方法-CSDN博客](https://blog.csdn.net/weixin_39611043/article/details/110829061)

（4）字符串切片 **str[start:end]**，其中 start（包含）是切片开始的索引，end（不包含）是切片结束的索引。

（5）字符串的切片可以加上步长参数 step，语法格式如下：**str[start:end:step]**

（6）格式化字符串：

| 字符 | 功能                                                         |
| ---- | ------------------------------------------------------------ |
| <sp> | 在正数前面显示空格                                           |
| #    | 在八进制数前面显示零('0')，在十六进制前面显示'0x'或者'0X'(取决于用的是'x'还是'X') |
| 0    | 显示的数字前面填充'0'而不是默认的空格                        |
| %    | '%%'输出一个单一的'%'                                        |

（7）常用内建函数

| 序号 | 方法及描述                                                   |
| :--- | :----------------------------------------------------------- |
| 1    | [capitalize()](https://www.runoob.com/python3/python3-string-capitalize.html) 将字符串的第一个字符转换为大写 |
| 2    | [center(width, fillchar)](https://www.runoob.com/python3/python3-string-center.html)返回一个指定的宽度 width 居中的字符串，fillchar 为填充的字符，默认为空格。 |
| 3    | [count(str, beg= 0,end=len(string))](https://www.runoob.com/python3/python3-string-count.html) 返回 str 在 string 里面出现的次数，如果 beg 或者 end 指定则返回指定范围内 str 出现的次数 |
| 4    | [bytes.decode(encoding="utf-8", errors="strict")](https://www.runoob.com/python3/python3-string-decode.html) Python3 中没有 decode 方法，但我们可以使用 bytes 对象的 decode() 方法来解码给定的 bytes 对象，这个 bytes 对象可以由 str.encode() 来编码返回。 |
| 5    | [encode(encoding='UTF-8',errors='strict')](https://www.runoob.com/python3/python3-string-encode.html) 以 encoding 指定的编码格式编码字符串，如果出错默认报一个ValueError 的异常，除非 errors 指定的是'ignore'或者'replace' |
| 6    | [endswith(suffix, beg=0, end=len(string))](https://www.runoob.com/python3/python3-string-endswith.html) 检查字符串是否以 suffix 结束，如果 beg 或者 end 指定则检查指定的范围内是否以 suffix 结束，如果是，返回 True,否则返回 False。 |
| 7    | [expandtabs(tabsize=8)](https://www.runoob.com/python3/python3-string-expandtabs.html) 把字符串 string 中的 tab 符号转为空格，tab 符号默认的空格数是 8 。 |
| 8    | [find(str, beg=0, end=len(string))](https://www.runoob.com/python3/python3-string-find.html) 检测 str 是否包含在字符串中，如果指定范围 beg 和 end ，则检查是否包含在指定范围内，如果包含返回开始的索引值，否则返回-1 |
| 9    | [index(str, beg=0, end=len(string))](https://www.runoob.com/python3/python3-string-index.html) 跟find()方法一样，只不过如果str不在字符串中会报一个异常。 |
| 10   | [isalnum()](https://www.runoob.com/python3/python3-string-isalnum.html) 检查字符串是否由字母和数字组成，即字符串中的所有字符都是字母或数字。如果字符串至少有一个字符，并且所有字符都是字母或数字，则返回 True；否则返回 False。 |
| 11   | [isalpha()](https://www.runoob.com/python3/python3-string-isalpha.html) 如果字符串至少有一个字符并且所有字符都是字母或中文字则返回 True, 否则返回 False |
| 12   | [isdigit()](https://www.runoob.com/python3/python3-string-isdigit.html) 如果字符串只包含数字则返回 True 否则返回 False.. |
| 13   | [islower()](https://www.runoob.com/python3/python3-string-islower.html) 如果字符串中包含至少一个区分大小写的字符，并且所有这些(区分大小写的)字符都是小写，则返回 True，否则返回 False |
| 14   | [isnumeric()](https://www.runoob.com/python3/python3-string-isnumeric.html) 如果字符串中只包含数字字符，则返回 True，否则返回 False |
| 15   | [isspace()](https://www.runoob.com/python3/python3-string-isspace.html) 如果字符串中只包含空白，则返回 True，否则返回 False. |
| 16   | [istitle()](https://www.runoob.com/python3/python3-string-istitle.html) 如果字符串是标题化的(见 title())则返回 True，否则返回 False |
| 17   | [isupper()](https://www.runoob.com/python3/python3-string-isupper.html) 如果字符串中包含至少一个区分大小写的字符，并且所有这些(区分大小写的)字符都是大写，则返回 True，否则返回 False |
| 18   | [join(seq)](https://www.runoob.com/python3/python3-string-join.html) 以指定字符串作为分隔符，将 seq 中所有的元素(的字符串表示)合并为一个新的字符串 |
| 19   | [len(string)](https://www.runoob.com/python3/python3-string-len.html) 返回字符串长度 |
| 20   | [ljust(width[, fillchar\])](https://www.runoob.com/python3/python3-string-ljust.html) 返回一个原字符串左对齐,并使用 fillchar 填充至长度 width 的新字符串，fillchar 默认为空格。 |
| 21   | [lower()](https://www.runoob.com/python3/python3-string-lower.html) 转换字符串中所有大写字符为小写. |
| 22   | [lstrip()](https://www.runoob.com/python3/python3-string-lstrip.html) 截掉字符串左边的空格或指定字符。 |
| 23   | [maketrans()](https://www.runoob.com/python3/python3-string-maketrans.html) 创建字符映射的转换表，对于接受两个参数的最简单的调用方式，第一个参数是字符串，表示需要转换的字符，第二个参数也是字符串表示转换的目标。 |
| 24   | [max(str)](https://www.runoob.com/python3/python3-string-max.html) 返回字符串 str 中最大的字母。 |
| 25   | [min(str)](https://www.runoob.com/python3/python3-string-min.html) 返回字符串 str 中最小的字母。 |
| 26   | [replace(old, new [, max\])](https://www.runoob.com/python3/python3-string-replace.html) 把 将字符串中的 old 替换成 new,如果 max 指定，则替换不超过 max 次。 |
| 27   | [rfind(str, beg=0,end=len(string))](https://www.runoob.com/python3/python3-string-rfind.html) 类似于 find()函数，不过是从右边开始查找. |
| 28   | [rindex( str, beg=0, end=len(string))](https://www.runoob.com/python3/python3-string-rindex.html) 类似于 index()，不过是从右边开始. |
| 29   | [rjust(width,[, fillchar\])](https://www.runoob.com/python3/python3-string-rjust.html) 返回一个原字符串右对齐,并使用fillchar(默认空格）填充至长度 width 的新字符串 |
| 30   | [rstrip()](https://www.runoob.com/python3/python3-string-rstrip.html) 删除字符串末尾的空格或指定字符。 |
| 31   | [split(str="", num=string.count(str))](https://www.runoob.com/python3/python3-string-split.html) 以 str 为分隔符截取字符串，如果 num 有指定值，则仅截取 num+1 个子字符串 |
| 32   | [splitlines([keepends\])](https://www.runoob.com/python3/python3-string-splitlines.html) 按照行('\r', '\r\n', \n')分隔，返回一个包含各行作为元素的列表，如果参数 keepends 为 False，不包含换行符，如果为 True，则保留换行符。 |
| 33   | [startswith(substr, beg=0,end=len(string))](https://www.runoob.com/python3/python3-string-startswith.html) 检查字符串是否是以指定子字符串 substr 开头，是则返回 True，否则返回 False。如果beg 和 end 指定值，则在指定范围内检查。 |
| 34   | [strip([chars\])](https://www.runoob.com/python3/python3-string-strip.html) 在字符串上执行 lstrip()和 rstrip() |
| 35   | [swapcase()](https://www.runoob.com/python3/python3-string-swapcase.html) 将字符串中大写转换为小写，小写转换为大写 |
| 36   | [title()](https://www.runoob.com/python3/python3-string-title.html) 返回"标题化"的字符串,就是说所有单词都是以大写开始，其余字母均为小写(见 istitle()) |
| 37   | [translate(table, deletechars="")](https://www.runoob.com/python3/python3-string-translate.html) 根据 table 给出的表(包含 256 个字符)转换 string 的字符, 要过滤掉的字符放到 deletechars 参数中 |
| 38   | [upper()](https://www.runoob.com/python3/python3-string-upper.html) 转换字符串中的小写字母为大写 |
| 39   | [zfill (width)](https://www.runoob.com/python3/python3-string-zfill.html) 返回长度为 width 的字符串，原字符串右对齐，前面填充0 |
| 40   | [isdecimal()](https://www.runoob.com/python3/python3-string-isdecimal.html) 检查字符串是否只包含十进制字符，如果是返回 true，否则返回 false。 |

代码示例：

```python
str = '123456789'

print(str)  # 输出字符串
print(str[0:-1])  # 输出第一个到倒数第二个的所有字符
print(str[0])  # 输出字符串第一个字符
print(str[2:5])  # 输出从第三个开始到第六个的字符（不包含）
print(str[2:])  # 输出从第三个开始后的所有字符
print(str[1:5:2])  # 输出从第二个开始到第五个且每隔一个的字符（步长为2）
print(str * 2)  # 输出字符串两次
print(str + '你好')  # 连接字符串

print('------------------------------')
print('hello\nrunoob')  # 使用反斜杠(\)+n转义特殊字符
print(r'hello\nrunoob')  # 在字符串前面添加一个 r，表示原始字符串，不会发生转义
```

运行结果：

```
123456789
12345678
1
345
3456789
24
123456789123456789
123456789你好
------------------------------
hello
runoob
hello\nrunoob
```

##### 2.print输出：

**print** 默认输出是换行的，如果要实现不换行需要在变量末尾加上 **end=""**：

代码示例：

```python
x = "a"
y = "b"
# 换行输出
print(x)
print(y)

print('---------')
# 不换行输出
print(x, end=" ")
print(y, end=" ")
print()
```

结果运行：

```
a
b
---------
a b
```

##### 3.import 与 from...import

（1）在 python 用 **import** 或者 **from...import** 来导入相应的模块。

（2）将整个模块(somemodule)导入，格式为： **import somemodule**

（3）从某个模块中导入某个函数,格式为： **from somemodule import somefunction**

（4）从某个模块中导入多个函数,格式为： **from somemodule import firstfunc, secondfunc, thirdfunc**

（5）将某个模块中的全部函数导入，格式为： **from somemodule import \***

代码示例：

```python
import sys
print('================Python import mode==========================')
print ('命令行参数为:')
for i in sys.argv:
    print (i)
print ('\n python 路径为',sys.path)
```

```python
from sys import argv, path  # 导入特定的成员
print('================python from import===================================')
print('path:', path)  # 因为已经导入path成员，所以此处引用时不需要加sys.path
```

##### 4.Number（数字）

(1)内置的 type() 函数可以用来查询变量所指的对象类型。

(2)还可以用 isinstance 来判断:

```python
>>> a = 111
>>> isinstance(a, int)
True
```

(3)isinstance 和 type 的区别在于：

type()不会认为子类是一种父类类型;isinstance()会认为子类是一种父类类型。

```python
>>> class A:
...     pass
... 
>>> class B(A):
...     pass
... 
>>> isinstance(A(), A)
True
>>> type(A()) == A 
True
>>> isinstance(B(), A)
True
>>> type(B()) == A
False
```

(4)bool 是 int 的子类，True 和 False 可以和数字相加，**True==1、False==0**(数值比较) 会返回 **True**，但可以通过* **is** *（地址比较）来判断类型。

```python
>>> issubclass(bool, int) 
True
>>> True==1
True
>>> False==0
True
>>> True+1
2
>>> False+1
1
>>> 1 is True
False
>>> 0 is False
False
```

(5)可以使用del语句删除一些对象引用,详见：[python中del函数的用法总结_python del-CSDN博客](https://blog.csdn.net/m0_46483236/article/details/115976800)

(6)**complex(x, y)** 将 x 和 y 转换到一个复数，实数部分为 x，虚数部分为 y。x 和 y 是数字表达式。

(7)变量在使用前必须先"定义"（即赋予变量一个值），否则会出现错误;

(8)在交互模式中，最后被输出的表达式结果被赋值给变量 **_** 。e.g.

```python
>>> tax = 12.5 / 100
>>> price = 100.50
>>> price * tax
12.5625
>>> price + _
113.0625
>>> round(_, 2)
113.06
```

(7)相关函数：

①数字函数：

[abs(x)函数][1]、[ceil(x)函数][2]、[exp(x)][3]、[fabs(x)函数][4]、[floor(x)函数][5]、[log()函数][6]、[log10(x)函数][7]、[max()函数][8]、[min()函数][9]、[modf(x)函数][10]、pow(x,y)函数、[round( x [, n]  )函数][11]、sqrt(x)函数

[1]: https://www.runoob.com/python3/python3-func-number-abs.html
[2]:  https://www.runoob.com/python3/python3-func-number-ceil.html
[3]:  https://www.runoob.com/python3/python3-func-number-exp.html
[4]: https://www.runoob.com/python3/python3-func-number-fabs.html
[5]:https://www.runoob.com/python3/python3-func-number-floor.html
[6]:https://www.runoob.com/python3/python3-func-number-log.html
[7]:https://www.runoob.com/python3/python3-func-number-log10.html
[8]:https://www.runoob.com/python3/python3-func-number-max.html
[9]:https://www.runoob.com/python3/python3-func-number-min.html
[10]:https://www.runoob.com/python3/python3-func-number-modf.html
[11]:https://www.runoob.com/python3/python3-func-number-round.html

②随机数函数：

| 函数                                                         | 描述                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [choice(seq)](https://www.runoob.com/python3/python3-func-number-choice.html) | 从序列的元素中随机挑选一个元素                               |
| [randrange ([start,\] stop [,step])](https://www.runoob.com/python3/python3-func-number-randrange.html) | 从指定范围内，按指定基数递增的集合中获取一个随机数，基数默认值为 1 |
| [random()](https://www.runoob.com/python3/python3-func-number-random.html) | 随机生成下一个实数，它在[0,1)范围内。                        |
| [seed(x)](https://www.runoob.com/python3/python3-func-number-seed.html) | 改变随机数生成器的种子seed。                                 |
| [shuffle(lst)](https://www.runoob.com/python3/python3-func-number-shuffle.html) | 将序列的所有元素随机排序                                     |
| [uniform(x, y)](https://www.runoob.com/python3/python3-func-number-uniform.html) | 随机生成下一个实数，它在[x,y]范围内                          |

③三角函数：

[acos(x)](https://www.runoob.com/python3/python3-func-number-acos.html)、[asin(x)](https://www.runoob.com/python3/python3-func-number-asin.html)、[atan(x)](https://www.runoob.com/python3/python3-func-number-atan.html)、[atan2(y, x)](https://www.runoob.com/python3/python3-func-number-atan2.html)、[cos(x)](https://www.runoob.com/python3/python3-func-number-cos.html)、[hypot(x, y)](https://www.runoob.com/python3/python3-func-number-hypot.html)、[sin(x)](https://www.runoob.com/python3/python3-func-number-sin.html)、[tan(x)](https://www.runoob.com/python3/python3-func-number-tan.html)、[degrees(x)](https://www.runoob.com/python3/python3-func-number-degrees.html)、[radians(x)](https://www.runoob.com/python3/python3-func-number-radians.html)

##### 5.数值运算：

（1）Python可以同时为多个变量赋值，如a, b = 1, 2。

（2）一个变量可以通过赋值指向不同类型的对象。

（3）数值的除法包含两个运算符：**/** 返回一个浮点数，**//** 返回一个整数；有乘方运算**。

（4）在混合计算时，Python会把整型转换成为浮点数。

##### 6.bool（布尔类型）

（1）bool 是 int 的子类，因此布尔值可以被看作整数来使用，其中 True 等价于 1。

（2）可以使用 `bool()` 函数将其他类型的值转换为布尔值。以下值在转换为布尔值时为 `False`：`None`、`False`、零 (`0`、`0.0`、`0j`)、空序列（如 `''`、`()`、`[]`）和空映射（如 `{}`）。其他所有值转换为布尔值时均为 `True`。

##### 7.List[列表]

（1）列表写在方括号之间，元素用逗号隔开，一个列表中的元素类型可以不同。

（2）和字符串一样，列表可以被索引和切片。

（3）列表可以使用 **+**、***** 操作符进行操作。

（4）列表中的元素是可以改变的。

（5）Python 列表截取可以接收第三个参数，参数作用是截取的步长。

（6）可对列表的数据项进行修改或更新，也可使用 append() 方法来添加列表项，使用 del 语句来删除列表中的元素。

示例：

```python
list = ['Google', 'Runoob', 1997, 2000]
print ("第三个元素为 : ", list[2])
list[2] = 2001
print ("更新后的第三个元素为 : ", list[2])

list1 = ['Google', 'Runoob', 'Taobao']
list1.append('Baidu')
print ("更新后的列表 : ", list1)
del list[2]
print ("删除第三个元素 : ", list)
```

结果：

```
第三个元素为 :  1997
更新后的第三个元素为 :  2001
更新后的列表 :  ['Google', 'Runoob', 'Taobao', 'Baidu']
删除第三个元素 : ['Google', 'Runoob', 'Baidu']
```

（7）列表可以嵌套，类似多维数组；

（8）可import  **operator** 模块的 **eq** 方法对列表进行比较

（9）相关函数与方法：

| 序号 | 函数                                                         |
| :--- | :----------------------------------------------------------- |
| 1    | [len(list)](https://www.runoob.com/python3/python3-att-list-len.html) 列表元素个数 |
| 2    | [max(list)](https://www.runoob.com/python3/python3-att-list-max.html) 返回列表元素最大值 |
| 3    | [min(list)](https://www.runoob.com/python3/python3-att-list-min.html) 返回列表元素最小值 |
| 4    | [list(seq)](https://www.runoob.com/python3/python3-att-list-list.html) 将元组转换为列表 |

| 序号 | 方法                                                         |
| :--- | :----------------------------------------------------------- |
| 1    | [list.append(obj)](https://www.runoob.com/python3/python3-att-list-append.html) 在列表末尾添加新的对象 |
| 2    | [list.count(obj)](https://www.runoob.com/python3/python3-att-list-count.html) 统计某个元素在列表中出现的次数 |
| 3    | [list.extend(seq)](https://www.runoob.com/python3/python3-att-list-extend.html) 在列表末尾一次性追加另一个序列中的多个值（用新列表扩展原来的列表） |
| 4    | [list.index(obj)](https://www.runoob.com/python3/python3-att-list-index.html) 从列表中找出某个值第一个匹配项的索引位置 |
| 5    | [list.insert(index, obj)](https://www.runoob.com/python3/python3-att-list-insert.html) 将对象插入列表 |
| 6    | [list.pop([index=-1])](https://www.runoob.com/python3/python3-att-list-pop.html) 移除列表中的一个元素（默认最后一个元素），并且返回该元素的值 |
| 7    | [list.remove(obj)](https://www.runoob.com/python3/python3-att-list-remove.html) 移除列表中某个值的第一个匹配项 |
| 8    | [list.reverse()](https://www.runoob.com/python3/python3-att-list-reverse.html) 反向列表中元素 |
| 9    | [list.sort( key=None, reverse=False)](https://www.runoob.com/python3/python3-att-list-sort.html) 对原列表进行排序 |
| 10   | [list.clear()](https://www.runoob.com/python3/python3-att-list-clear.html) 清空列表 |
| 11   | [list.copy()](https://www.runoob.com/python3/python3-att-list-copy.html) 复制列表 |

tip:  **del** a[:] => a==[];  del a =>  删除实体变量a

##### 8.Tuple（元组,）

(1)与字符串一样，元组的元素不能修改.虽然tuple的元素不可改变，但它可以包含可变的对象，比如list列表。

(2)元组也可以被索引和切片，方法与列表一样。

(3)注意构造包含 0 或 1 个元素的元组的特殊语法规则。

(4)元组也可以使用 **+** 操作符进行拼接。

##### 9.Set{集合}

(1)Python 中的集合（Set）是一种无序、可变的数据类型，用于存储唯一的元素。

(2)集合中的元素不会重复，并且可以进行交集、并集、差集等常见的集合操作。

(3)创建一个空集合必须用 **set()** 而不是 **{ }**，因为 **{ }** 是用来创建一个空字典。

创建格式：

```python
parame = {value01,value02,...}
或者
set(value)
```

代码示例：

```python
sites = {'Google', 'Taobao', 'Runoob', 'Facebook', 'Zhihu', 'Baidu'}
print(sites)   # 输出集合，重复的元素被自动去掉

# 成员测试
if 'Runoob' in sites :
    print('Runoob 在集合中')
else :
    print('Runoob 不在集合中')

# set可以进行集合运算
a = set('abracadabra')
b = set('alacazam')

print(a)
print(a - b)     # a 和 b 的差集
print(a | b)     # a 和 b 的并集
print(a & b)     # a 和 b 的交集
print(a ^ b)     # a 和 b 中不同时存在的元素
```

运行结果：

```
{'Zhihu', 'Baidu', 'Taobao', 'Runoob', 'Google', 'Facebook'}
Runoob 在集合中
{'b', 'c', 'a', 'r', 'd'}
{'r', 'b', 'd'}
{'b', 'c', 'a', 'z', 'm', 'r', 'l', 'd'}
{'c', 'a'}
{'z', 'b', 'm', 'r', 'l', 'd'}
```

##### 10.Dictionary {字典}

(1)列表是有序的对象集合，字典是无序的对象集合。两者之间的区别在于：字典当中的元素是通过键来存取的，而不是通过偏移存取。

(2)字典是一种映射类型，字典用 **{ }** 标识,是一个无序的 **键(key) : 值(value)** 的集合，它的元素是键值对。

(3)键(key)必须使用不可变类型,且在同一个字典中，键(key)必须是唯一的(不重复)。

构造方法：

```python
dict = {}
dict['one'] = "1 - 菜鸟教程"
dict[2] = "2 - 菜鸟工具"

tinydict = {'name': 'runoob','code':1, 'site': 'www.runoob.com'}

print (dict['one'])       # 输出键为 'one' 的值
print (dict[2])           # 输出键为 2 的值
print (tinydict)          # 输出完整的字典
print (tinydict.keys())   # 输出所有键
print (tinydict.values()) # 输出所有值
```

结果：

```
1 - 菜鸟教程
2 - 菜鸟工具
{'name': 'runoob', 'code': 1, 'site': 'www.runoob.com'}
dict_keys(['name', 'code', 'site'])
dict_values(['runoob', 1, 'www.runoob.com'])
```

(4)构造函数 dict() 可以直接从键值对序列中构建字典：

```python
>>> dict([('Runoob', 1), ('Google', 2), ('Taobao', 3)])
{'Runoob': 1, 'Google': 2, 'Taobao': 3}
>>> {x: x**2 for x in (2, 4, 6)}
{2: 4, 4: 16, 6: 36}
>>> dict(Runoob=1, Google=2, Taobao=3)
{'Runoob': 1, 'Google': 2, 'Taobao': 3}
```

##### 11.bytes 类型

(1)创建方式：

```python
x = bytes("hello", encoding="utf-8")
y = b"hello"
```

(2)bytes 类型也支持许多操作和方法，如切片、拼接、查找、替换等等。同时，由于 bytes 类型是不可变的，因此在进行修改操作时需要创建一个新的 bytes 对象。

#### 二、运算符

##### 1.海象运算符     :=

+ 这个运算符的主要目的是在表达式中同时进行赋值和返回赋值的值。

代码示例：

```python
# 传统写法
n = 10
if n > 5:
    print(n)

# 使用海象运算符
if (n := 10) > 5:
    print(n)
```

##### 2.位运算符：

（1）按位与运算符&：参与运算的两个值,如果两个相应位都为1,则该位的结果为1,否则为0；

（2）按位或运算符|：只要对应的二个二进位有一个为1时，结果位就为1。

（3）按位异或运算符^：当两对应的二进位相异时，结果为1;

（4）按位取反运算符：对数据的每个二进制位取反,即把1变为0,把0变为1。**~x** 类似于 **-x-1**

（5）左移动运算符：运算数的各二进位全部左移若干位，由"<<"右边的数指定移动的位数，高位丢弃，低位补0。

（6）

```python
x = True
y = False
z = False

if x or y and z:
    print("yes")
else:
    print("no")
```

#### 三.循环

##### 1.循环语句：

(1).可以结合 range() 和 len() 函数以遍历一个序列的索引

```python
>>>a = ['Google', 'Baidu', 'Runoob', 'Taobao', 'QQ']
>>> for i in range(len(a)):
...     print(i, a[i])
... 
0 Google
1 Baidu
2 Runoob
3 Taobao
4 QQ
```

(2)可以使用 range() 函数来创建一个列表:

```python
>>>list(range(5))
[0, 1, 2, 3, 4]
```

##### 2.推导式：

(1)列表推导式：

实例：过滤掉长度小于或等于3的字符串列表，并将剩下的转换成大写字母：

```python
>>> names = ['Bob','Tom','alice','Jerry','Wendy','Smith']
>>> new_names = [name.upper()for name in names if len(name)>3]
>>> print(new_names)
['ALICE', 'JERRY', 'WENDY', 'SMITH']
```

计算 30 以内可以被 3 整除的整数：

```python
>>> multiples = [i for i in range(30) if i % 3 == 0]
>>> print(multiples)
[0, 3, 6, 9, 12, 15, 18, 21, 24, 27]
```

(2)字典推导式：

使用字符串及其长度创建字典：

```python
listdemo = ['Google','Runoob', 'Taobao']
# 将列表中各字符串值为键，各字符串的长度为值，组成键值对
>>> newdict = {key:len(key) for key in listdemo}
>>> newdict
{'Google': 6, 'Runoob': 6, 'Taobao': 6}
```

提供三个数字，以三个数字为键，三个数字的平方为值来创建字典：

```python
>>> dic = {x: x**2 for x in (2, 4, 6)}
>>> dic
{2: 4, 4: 16, 6: 36}
>>> type(dic)
<class 'dict'>
```

(3)集合推导式:

判断不是abc的字符并输出：

```python
>>> a = {x for x in 'abracadabra' if x not in 'abc'}
>>> a
{'d', 'r'}
>>> type(a)
<class 'set'>
```

(4)元组推导式（生成器表达式）:

​	元组推导式和列表推导式的用法也完全相同，只是元组推导式是用 **()** 圆括号将各部分括起来，而列表推导式用的是中括号 **[]**，另外元组推导式返回的结果是一个生成器对象。

生成一个包含数字 1~9 的元组：

```python
>>> a = (x for x in range(1,10))
>>> a
<generator object <genexpr> at 0x7faf6ee20a50>  # 返回的是生成器对象
>>> tuple(a)       # 使用 tuple() 函数，可以直接将生成器对象转换成元组
(1, 2, 3, 4, 5, 6, 7, 8, 9)
```

#### 四、函数

##### 1、语法：

示例：

```python
def area(width, height):
    return width * height
def print_welcome(name):
    print("Welcome", name)

print_welcome("Runoob")
w = 4
h = 5
print("width =", w, " height =", h, " area =", area(w, h))
```

```
Welcome Runoob
width = 4  height = 5  area = 20
```

##### 2、参数传递：

在 python 中，类型属于对象，对象有不同类型的区分，变量是没有类型的

e.g.

```python
a=[1,2,3]
a="Runoob"
```

以上代码中，**[1,2,3]** 是 List 类型，**"Runoob"** 是 String 类型，而变量 a 是没有类型，它仅仅是一个对象的引用（一个指针），可以是指向 List 类型对象，也可以是指向 String 类型对象。

##### 3.可更改(mutable)与不可更改(immutable)对象

(1)在 python 中，strings, tuples, 和 numbers 是不可更改的对象，而 list,dict 等则是可以修改的对象。

- **不可变类型：**变量赋值 **a=5** 后再赋值 **a=10**，这里实际是新生成一个 int 值对象 10，再让 a 指向它，而 5 被丢弃，不是改变 a 的值，相当于新生成了 a。
- **可变类型：**变量赋值 **la=[1,2,3,4]** 后再赋值 **la[2]=5** 则是将 list la 的第三个元素值更改，本身la没有动，只是其内部的一部分值被修改了。

(2)python 函数的参数传递：

- **不可变类型：**类似 C++ 的值传递，如整数、字符串、元组。如 fun(a)，传递的只是 a 的值，没有影响 a 对象本身。如果在 fun(a) 内部修改 a 的值，则是新生成一个 a 的对象。
- **可变类型：**类似 C++ 的引用传递，如 列表，字典。如 fun(la)，则是将 la 真正的传过去，修改后 fun 外部的 la 也会受影响

##### 4.不定长参数

能处理比当初声明时更多的参数，声明时不会命名。

(1)传递参数为元祖

基本语法如下：

```python
def functionname([formal_args,] *var_args_tuple ):
   "函数_文档字符串"
   function_suite
   return [expression]
```

如果在函数调用时没有指定参数，它就是一个空元组。也可以不向函数传递未命名的变量。如下实例：

```python
# 可写函数说明
def printinfo(arg1, *vartuple):
   "打印任何传入的参数"
   print("输出: ")
   print(arg1)
   for var in vartuple:
      print(var)
   return

# 调用printinfo 函数
printinfo(10)
printinfo(70, 60, 50)
```

```
输出:
10
输出:
70
60
50
```

(2)传递参数为字典：

是参数带两个星号 ***\***，基本语法如下：

```python
def functionname([formal_args,] **var_args_dict ):
   "函数_文档字符串"
   function_suite
   return [expression]
```

实例：

```python
# 可写函数说明
def printinfo(arg1, **vardict):
   "打印任何传入的参数"
   print("输出: ")
   print(arg1)
   print(vardict)

# 调用printinfo 函数
printinfo(1, a=2, b=3)
```

```
输出: 
1
{'a': 2, 'b': 3}
```

(3)声明函数时，参数中星号 ***** 可以单独出现，例如:

```python
def f(a, b, *, c):
   return a + b + c
```

如果单独出现星号 *****，则星号 ***** 后的参数必须用关键字传入,否则会报错：

```python
>>> def f(a,b,*,c):
...     return a+b+c
... 
>>> f(1,2,3)   # 报错
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: f() takes 2 positional arguments but 3 were given
>>> f(1,2,c=3) # 正常
6
```

##### 5、匿名函数

(1)Python 使用 **lambda** 来创建匿名函数,而不再使用 **def** 语句定义。

- **lambda** 只是一个表达式，而不是一个代码块，函数体比 **def** 简单很多。仅能在 lambda 表达式中封装有限的逻辑进去。
- lambda 函数拥有自己的命名空间，且不能访问自己参数列表之外或全局命名空间里的参数。
-  lambda 函数的目的是调用小函数时不占用栈内存从而减少函数调用的开销，提高代码的执行速度。

(2)语法:

lambda 函数的语法只包含一个语句，如下：

```pyt
lambda [arg1 [,arg2,.....argn]]:expression
```

示例：

```python
sum = lambda arg1, arg2: arg1 + arg2
# 调用sum函数
print("相加后的值为 : ", sum(10, 20))
print("相加后的值为 : ", sum(20, 20))
```

```
相加后的值为 :  30
相加后的值为 :  40
```

(3)用法提示：可以将匿名函数封装在一个函数内，这样可以使用同样的代码来创建多个匿名函数。以下实例将匿名函数封装在 myfunc 函数中，通过传入不同的参数来创建不同的匿名函数：

```python
def myfunc(n):
   return lambda a: a * n

mydoubler = myfunc(2)
mytripler = myfunc(3)

print(mydoubler(11))
print(mytripler(11))
```

```
22
33
```

(4)通常在需要函数作为参数传递的情况下使用，例如在 map()、filter()、reduce() 等函数中。

例1：与内置函数如 map()、filter() 和 reduce() 一起使用，以便在集合上执行操作

```python
numbers = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, numbers))
print(squared)  # 输出: [1, 4, 9, 16, 25]
```

map(function, iterable,...):对可迭代对象(func后)中的每个元素应用一个函数(func)，并返回一个包含结果的新的迭代器。

例2：与 filter() 一起，筛选偶数：

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)  # 输出：[2, 4, 6, 8]
```

filter(function, iterable):用于过滤可迭代对象iterable中的元素，只保留满足特定条件function的元素，返回一个新的迭代器。

例3：使用 reduce() 和 lambda 表达式计算一个序列的累积乘积：reduce() 函数通过遍历 numbers 列表，并使用 lambda 函数将累积的结果不断更新，最终得到了 **1 \* 2 \* 3 \* 4 \* 5 = 120** 的结果。

```python
from functools import reduce

numbers = [1, 2, 3, 4, 5]

# 使用 reduce() 和 lambda 函数计算乘积
product = reduce(lambda x, y: x * y, numbers)

print(product)  # 输出：120
```

##### 6.强制位置参数：

函数形参语法 / 用来指明函数形参必须使用指定位置参数，不能使用关键字参数的形式。

在以下的例子中，形参 a 和 b 必须使用指定位置参数，c 或 d 可以是位置形参或关键字形参，而 e 和 f 要求为关键字形参:

```python
def f(a, b, /, c, d, *, e, f):
    print(a, b, c, d, e, f)
```

```
f(10, 20, 30, d=40, e=50, f=60)       #正确形式
f(10, b=20, c=30, d=40, e=50, f=60)   # b 不能使用关键字参数的形式
f(10, 20, 30, 40, 50, f=60)           # e 必须使用关键字参数的形式
```

#### 五、数据结构

##### （一）将列表当做栈使用：

可以使用列表（list）来实现栈（先入后出）的功能，列表提供了一些方法，使其非常适合用于栈操作，特别是 **append()** 和 **pop()** 方法。append() 方法可以把一个元素添加到栈顶，不指定索引的 pop() 方法可以把一个元素从栈顶释放出来。

###### 栈操作：

首先创建一个空栈：`stack = []`

（1）**压入（Push）**: 使用 append() 方法将一个元素添加到栈的顶端。

```python
stack.append(1)
stack.append(2)
stack.append(3)
print(stack)  # 输出: [1, 2, 3]
```

（2）**弹出（Pop）**: 使用 pop() 方法移除并返回栈顶元素。

```python
top_element = stack.pop()
print(top_element)  # 输出: 3
print(stack)        # 输出: [1, 2]
```

（3）**查看栈顶元素（Peek/Top）**: 返回栈顶元素而不移除它。

```python
top_element = stack[-1]
print(top_element)  # 输出: 2
```

（4）**检查是否为空（IsEmpty）**: 检查栈是否为空。

```python
is_empty = len(stack) == 0
print(is_empty)  # 输出: False
```

（5）**获取栈的大小（Size）**: 使用 len() 函数获取栈中元素的数量。

```python
size = len(stack)
print(size)  # 输出: 2
```

##### （二）将列表当作队列使用

列表可以用作队列（先进先出），但并不是最优的选择。

###### 1、使用 collections.deque 实现队列：

 collections.deque，它是双端队列，可以在两端高效地添加和删除元素，非常适合用于实现队列。

示例：

```python
from collections import deque

#创建一个空队列
queue = deque()

#向队尾添加元素:
queue.append('a')
queue.append('b')
queue.append('c')
print("队列状态：",queue)

#从队首移除元素：
first_emement=queue.popleft()
print("移除的元素：",first_emement)
print("队列状态：",queue)

#查看队首元素（不移除）
front_element=queue[0]
print("队首元素：",front_element)

#检查队列是否为空
is_empty=len(queue)==0
print("队列是否为空：",is_empty)

#获取队列大小
size=len(queue)
print("队列大小:",size)
```

###### 2、使用列表实现队列：

虽然 deque更高效，但如果坚持使用列表来实现队列，也可以实现

（1）**创建队列**：

```python
queue = []
```

（2）**使用 append() 方法向队尾添加元素**：

```python
queue.append('a')
queue.append('b')
queue.append('c')
print("队列状态:", queue)  # 输出: 队列状态: ['a', 'b', 'c']
```

（3）使用 pop(0) 方法**从队首移除元素**：

```python
first_element = queue.pop(0)
print("移除的元素:", first_element)  # 输出: 移除的元素: a
print("队列状态:", queue)            # 输出: 队列状态: ['b', 'c']
```

（4）**查看队首元素（不移除）**：直接访问列表的第一个元素

```python
front_element = queue[0]
print("队首元素:", front_element)    # 输出: 队首元素: b
```

（5） **检查队列是否为空**：

```python
is_empty = len(queue) == 0
print("队列是否为空:", is_empty)     # 输出: 队列是否为空: False
```

（6）**获取队列大小**：

```python
size = len(queue)
print("队列大小:", size)            # 输出: 队列大小: 2
```

##### （三）列表推导式

直接看例子：

例1：

```python
>>> [[x, x**2] for x in vec]
[[2, 4], [4, 16], [6, 36]]
```

例2：对序列里每一个元素逐个调用某方法：

```python
>>> freshfruit = ['  banana', '  loganberry ', 'passion fruit  ']
>>> [weapon.strip() for weapon in freshfruit]
['banana', 'loganberry', 'passion fruit']
```

例3：用 if 子句作为过滤器：

```python
>>> [3*x for x in vec if x > 3]
[12, 18]
>>> [3*x for x in vec if x < 2]
[]
```

例4：

```python
>>> vec1 = [2, 4, 6]
>>> vec2 = [4, 3, -9]
>>> [x*y for x in vec1 for y in vec2]
[8, 6, -18, 16, 12, -36, 24, 18, -54]
>>> [x+y for x in vec1 for y in vec2]
[6, 5, -7, 8, 7, -5, 10, 9, -3]
>>> [vec1[i]*vec2[i] for i in range(len(vec1))]
[8, 12, -54]
```

例5：使用复杂表达式或嵌套函数：

```python
>>> [str(round(355/113, i)) for i in range(1, 6)]
['3.1', '3.14', '3.142', '3.1416', '3.14159']
```

##### （四）字典

###### 遍历技巧：

（1）在字典中遍历时，关键字和对应的值可以使用 items() 方法同时解读出来：

```python
>>> knights = {'gallahad': 'the pure', 'robin': 'the brave'}
>>> for k, v in knights.items():
...     print(k, v)
...
gallahad the pure
robin the brave
```

（2）在序列中遍历时，索引位置和对应值可以使用 enumerate() 函数同时得到：

```python
>>> for i, v in enumerate(['tic', 'tac', 'toe']):
...     print(i, v)
...
0 tic
1 tac
2 toe
```

（3）同时遍历两个或更多的序列，可以使用 zip() 组合：

```python
>>> questions = ['name', 'quest', 'favorite color']
>>> answers = ['lancelot', 'the holy grail', 'blue']
>>> for q, a in zip(questions, answers):
...     print('What is your {0}?  It is {1}.'.format(q, a))
...
What is your name?  It is lancelot.
What is your quest?  It is the holy grail.
What is your favorite color?  It is blue.
```

（4）要按顺序遍历一个序列，使用 sorted() 函数返回一个已排序的序列，并不修改原值:

```python
>>> basket = ['apple', 'orange', 'apple', 'pear', 'orange', 'banana']
>>> for f in sorted(set(basket)):
...     print(f)
...
apple
banana
orange
pear
```

#### 六、输入输出

##### 1.str.format() 的基本使用：

```python
>>> print('{}网址： "{}!"'.format('菜鸟教程', 'www.runoob.com'))
菜鸟教程网址： "www.runoob.com!"
>>> print('{0} 和 {1}'.format('Google', 'Runoob'))
Google 和 Runoob
>>> print('{1} 和 {0}'.format('Google', 'Runoob'))
Runoob 和 Google
```

2.可选项 **:** 和格式标识符可以跟着字段名。 这就允许对值进行更好的格式化，在 **:** 后传入一个整数, 可以保证该域至少有这么多的宽度。 用于美化表格时很有用。

```python
>>> table = {'Google': 1, 'Runoob': 2, 'Taobao': 3}
>>> for name, number in table.items():
...     print('{0:10} ==> {1:10d}'.format(name, number))
... 
Google     ==>          1
Runoob     ==>          2
Taobao     ==>          3
```

##### 2.读写文件：

open() 将会返回一个 file 对象：

```python
open(filename, mode)
```

示例：

```python
# 打开一个文件
f = open("/tmp/foo.txt", "w")
f.write( "Python 是一个非常好的语言。\n是的，的确非常好!!\n" )
# 关闭打开的文件
f.close()
```

##### 3.文件对象的方法：

（1）f.read()：

```python
# 打开一个文件
f = open("/tmp/foo.txt", "r")
str = f.read()
print(str)

# 关闭打开的文件
f.close()
```

（2）f.readline() ：

会从文件中读取单独的一行，换行符为 '\n'。f.readline() 如果返回一个空字符串, 说明已经已经读取到最后一行。

```python
# 打开一个文件
f = open("/tmp/foo.txt", "r")
str = f.readline()
print(str)

# 关闭打开的文件
f.close()
```

（3）f.readlines() ：

将返回该文件中包含的所有行，如果设置可选参数 sizehint, 则读取指定长度的字节, 并且将这些字节按行分割。

```python
# 打开一个文件
f = open("/tmp/foo.txt", "r")
str = f.readlines()
print(str)

# 关闭打开的文件
f.close()
```

结果：['Python 是一个非常好的语言。\n', '是的，的确非常好!!\n']

（4）迭代一个文件对象然后读取每行:：

```python
# 打开一个文件
f = open("/tmp/foo.txt", "r")
for line in f:
    print(line, end='')

# 关闭打开的文件
f.close()
```

（5）f.write(string)： 将 string 写入到文件中, 然后返回写入的字符数（长度）

```python
# 打开一个文件
f = open("/tmp/foo.txt", "w")
num = f.write( "Python 是一个非常好的语言。\n是的，的确非常好!!\n" )
print(num)
# 关闭打开的文件
f.close()
```

如果要写入一些不是字符串的东西, 那么将需要先进行转换:

```python
value = ('www.runoob.com', 14)
s = str(value)
f.write(s)
```

（6）f.tell()： 用于返回文件当前的读/写位置（即文件指针的位置）。

（7）f.seek()：改变文件指针当前的位置, 可使用 f.seek(offset, from_what) 函数，f.seek(offset, whence) 用于移动文件指针到指定位置。

offset 表示相对于 whence 参数的偏移量，from_what 的值（默认为0，即文件开头）, 如果是 0 表示开头, 如果是 1 表示当前位置, 2 表示文件的结尾。

#### 七、错误和异常

##### 1、异常处理

（1）try/except捕捉异常：

- 如果在执行 try 子句的过程中发生了异常，那么 try 子句余下的部分将被忽略。如果异常的类型和 except 之后的名称相符，那么对应的 except 子句将被执行。
- 如果一个异常没有与任何的 except 匹配，那么这个异常将会传递给上层的 try 中。

```python
try:
	执行代码
except:
	发生异常时执行的代码
```

+ 一个 try 语句可能包含多个except子句，分别来处理不同的特定的异常。最多只有一个分支会被执行。一个except子句可以同时处理多个异常，这些异常将被放在一个括号里成为一个元组：

```python
except (RuntimeError, TypeError, NameError):
    pass
```

+ 最后一个except子句可以忽略异常的名称，它将被当作通配符使用。

示例：

```python
import sys

try:
    f = open('myfile.txt')
    s = f.readline()
    i = int(s.strip())
except OSError as err:
    print("OS error: {0}".format(err))
except ValueError:
    print("Could not convert data to an integer.")
except:
    print("Unexpected error:", sys.exc_info()[0])
    raise
```

（2）try/except...else：**try/except** 语句还有一个可选的 **else** 子句，必须放在所有的 except 子句之后。else 子句将在 try 子句没有发生任何异常的时候执行，可以避免一些意想不到，而 except 又无法捕获的异常，而且还能处理子句中调用的函数（甚至间接调用的函数）里抛出的异常。

```python
try:
	执行代码
except:
	发生异常时执行的代码
else:
    没有异常时执行的代码
```

（3）try-finally 语句：无论是否发生异常都将执行最后的代码。

```python
try:
	执行代码
except:
	发生异常时执行的代码
else:
    没有异常时执行的代码
finally:
   不管有没有异常都会执行的代码 
```

##### 2.抛出异常：

使用 raise 语句抛出一个指定的异常：raise 唯一的一个参数指定了要被抛出的异常。它必须是一个异常的实例或者是异常的类（也就是 Exception 的子类）。

```python
raise [Exception [, args [, traceback]]]
```

示例：

```python
x = 10
if x > 5:
    raise Exception('x 不能大于 5。x 的值为:{}'.format(x))
```

结果：

```
Traceback (most recent call last):
  File "test.py", line 3, in <module>
    raise Exception('x 不能大于 5。x 的值为: {}'.format(x))
Exception: x 不能大于 5。x 的值为: 10
```

##### 3.用户自定义异常

（1）基本用法：可以创建一个新的异常类来拥有自己的异常。异常类继承自 Exception 类，可以直接继承，或者间接继承

```python
>>>class MyError(Exception):
    def __init__(self, value):
        self.value = value
    def __str__(self):
        return repr(self.value)

>> > try:
    raise MyError(2 * 2)
    #使用 raise 语句故意引发一个 MyError 异常
except MyError as e:
    #这里的 e 是捕获到的 MyError 异常对象
    print('My exception occurred, value:', e.value)

My exception occurred, value: 4
>> > raise MyError('oops!')
#再次使用 raise 语句引发 MyError 异常
Traceback(most recent call last):
File "<stdin>", line 1, in ?
__main__.MyError: 'oops!'
```

（2）通常做法：当创建一个模块有可能抛出多种不同的异常时，一种通常的做法是为这个包建立一个基础异常类，然后基于这个基础类为不同的错误情况创建不同的子类

```python
class Error(Exception):
    """Base class for exceptions in this module."""
    pass

class InputError(Error):
    """Exception raised for errors in the input.
    Attributes:
        expression -- input expression in which the error occurred
        message -- explanation of the error
    """
    def __init__(self, expression, message):
        self.expression = expression
        self.message = message

class TransitionError(Error):
    """Raised when an operation attempts a state transition that's not allowed.
    Attributes:
        previous -- state at beginning of transition
        next -- attempted new state
        message -- explanation of why the specific transition is not allowed
    """
    def __init__(self, previous, next, message):
        self.previous = previous
        self.next = next
        self.message = message
```

##### 4.预定义的清理行为

一些对象定义了标准的清理行为，无论系统是否成功的使用了它，一旦不需要它了，那么这个标准的清理行为就会执行。

e.g.尝试打开一个文件，然后把内容打印到屏幕上:

```python
for line in open("myfile.txt"):
    print(line, end="")
```

当执行完毕后，文件会保持打开状态，并没有被关闭。**关键词 with** 语句就可以保证诸如文件之类的对象在使用完之后一定会正确的执行他的清理方法:

```python
with open("myfile.txt") as f:
    for line in f:
        print(line, end="")
```

#### 八.面向对象

##### 1.类定义:

类实例化后，可以使用其属性，创建一个类之后，可以通过类名访问其属性。

```python
class ClassName:
    <statement-1>
 ……
    <statement-N>
```

##### 2.类对象：

（1）支持两种操作：属性引用和实例化。

属性引用使用和 Python 中所有的属性引用一样的标准语法：**obj.name**。类对象创建后，类命名空间中所有的命名都是有效属性名。

示例：

```python
class MyClass:
    """一个简单的类实例"""
    i = 12345
    def f(self):
        return 'hello world'

# 实例化类
x = MyClass()
# 访问类的属性和方法
print("MyClass 类的属性 i 为：", x.i)
print("MyClass 类的方法 f 输出为：", x.f())
```

```python
MyClass 类的属性 i 为： 12345
MyClass 类的方法 f 输出为： hello world
```

（2）类定义了 __init__() 方法，类的实例化操作会自动调用 __init__() 方法：

```python
class Complex:
    def __init__(self, realpart, imagpart):
        self.r = realpart
        self.i = imagpart
x = Complex(3.0, -4.5) #自动调用了
print(x.r, x.i)   # 输出结果：3.0 -4.5
```

##### 3.self 代表类的实例，而非类

类的方法与普通的函数只有一个特别的区别——它们必须有一个额外的**第一个参数名称**, 按照惯例它的名称是 self。

示例：

```python
class MyClass:
    def __init__(self, value):
        self.value = value

    def display_value(self):
        print(self.value)

# 创建一个类的实例
obj = MyClass(42) 
# 调用实例的方法
obj.display_value() # 输出 42
```

##### 4.类的方法

在类的内部，使用 **def** 关键字来定义一个方法，与一般函数定义不同，类方法必须包含参数 self, 且为第一个参数，self 代表的是类的实例。

```python
# 类定义
class people:
    # 定义基本属性
    name = ''
    age = 0
    # 定义私有属性,私有属性在类外部无法直接进行访问
    __weight = 0
    # 定义构造方法
    def __init__(self, n, a, w):
        self.name = n
        self.age = a
        self.__weight = w
    def speak(self):
        print("%s 说: 我 %d 岁。" % (self.name, self.age))

# 实例化类
p = people('runoob', 10, 30)
p.speak()
```

##### 5.继承:

子类（派生类）的定义:会继承父类（基类 ）的属性和方法。

class DerivedClassName(BaseClassName):

```python
    <statement-1>
……
    <statement-N>
```

实例中的基类必须与派生类定义在一个作用域内。除了类，还可以用表达式，基类定义在另一个模块中时这一点非常有用:

```python
class DerivedClassName(modname.BaseClassName):
```

示例：

```python
# 类定义
class people:
    # 定义基本属性
    name = ''
    age = 0
    # 定义私有属性,私有属性在类外部无法直接进行访问
    __weight = 0
    # 定义构造方法
    def __init__(self, n, a, w):
        self.name = n
        self.age = a
        self.__weight = w
    def speak(self):
        print("%s 说: 我 %d 岁。" % (self.name, self.age))

# 单继承示例
class student(people):
    grade = ''
    def __init__(self, n, a, w, g):
        # 调用父类的构函
        people.__init__(self, n, a, w)
        self.grade = g
    # 覆写父类的方法
    def speak(self):
        print("%s 说: 我 %d 岁了，我在读 %d 年级" % (self.name, self.age, self.grade))

s = student('ken', 10, 60, 3)
s.speak()
```

##### 6.多继承：

多继承的类定义：

class DerivedClassName(Base1, Base2, Base3):

```python
<statement-1>
……
<statement-N>
```

tips:注意圆括号中父类的顺序，若是父类中有相同的方法名，而在子类使用时未指定，python从左至右搜索 即方法在子类中未找到时，从左到右查找父类中是否包含方法。

```python
# 类定义
class people:
    # 定义基本属性
    name = ''
    age = 0
    # 定义私有属性,私有属性在类外部无法直接进行访问
    __weight = 0
    # 定义构造方法
    def __init__(self, n, a, w):
        self.name = n
        self.age = a
        self.__weight = w
    def speak(self):
        print("%s 说: 我 %d 岁。" % (self.name, self.age))

# 单继承示例
class student(people):
    grade = ''
    def __init__(self, n, a, w, g):
        # 调用父类的构函
        people.__init__(self, n, a, w)
        self.grade = g
    # 覆写父类的方法
    def speak(self):
        print("%s 说: 我 %d 岁了，我在读 %d 年级" % (self.name, self.age, self.grade))

# 另一个类，多继承之前的准备
class speaker():
    topic = ''
    name = ''
    def __init__(self, n, t):
        self.name = n
        self.topic = t
    def speak(self):
        print("我叫 %s，我是一个演说家，我演讲的主题是 %s" % (self.name, self.topic))

# 多继承
class sample(speaker, student):
    a = ''
    def __init__(self, n, a, w, g, t):
        student.__init__(self, n, a, w, g)
        speaker.__init__(self, n, t)

test = sample("Tim", 25, 80, 4, "Python")
test.speak()  # 方法名同，默认调用的是在括号中参数位置排前父类的方法
```

##### 7.方法重写:

父类方法的功能不能满足需求，可在子类重写父类的方法

```python
class Parent:  # 定义父类
    def myMethod(self):
        print('调用父类方法')

class Child(Parent):  # 定义子类
    def myMethod(self):
        print('调用子类方法')

c = Child()  # 子类实例
c.myMethod()  # 子类调用重写方法
super(Child, c).myMethod()  # 用子类对象调用父类已被覆盖的方法(super() 函数是用于调用父类(超类)的一个方法。)
```

##### 8.类属性与方法:

(1)类的私有属性:

**__private_attrs**：两个下划线开头，声明该属性为私有，不能在类的外部被使用或直接访问。在类内部的方法中使用时 **self.__private_attrs**。

实例：

```python
class JustCounter:
    __secretCount = 0  # 私有变量
    publicCount = 0  # 公开变量
    def count(self):
        self.__secretCount += 1
        self.publicCount += 1
        print(self.__secretCount)

counter = JustCounter()
counter.count()
counter.count()
print(counter.publicCount)
print(counter.__secretCount)  # 报错，实例不能访问私有变量
```

（2）类的私有方法：

**__private_method**：两个下划线开头，声明该方法为私有方法，只能在类的内部调用 ，不能在类的外部调用。**self.__private_methods**。

实例：

```python
class Site:
    def __init__(self, name, url):
        self.name = name  # public
        self.__url = url  # private
    def who(self):
        print('name  : ', self.name)
        print('url : ', self.__url)
    def __foo(self):  # 私有方法
        print('这是私有方法')
    def foo(self):  # 公共方法
        print('这是公共方法')
        self.__foo()

x = Site('菜鸟教程', 'www.runoob.com')
x.who()  # 正常输出
x.foo()  # 正常输出
x.__foo()  # 报错
```

##### 9.运算符重载

```python
class Vector:
    def __init__(self, a, b):
        self.a = a
        self.b = b
    def __str__(self):
        return 'Vector (%d, %d)' % (self.a, self.b)
    def __add__(self, other):
        return Vector(self.a + other.a, self.b + other.b)

v1 = Vector(2, 10)
v2 = Vector(5, -2)
print(v1 + v2)
```

#### 九.作用域

1.当内部作用域想修改外部作用域的变量时，就要用到 global 和 nonlocal 关键字

e.g.

```python
num = 1
def fun1():
    global num  # 需要使用 global 关键字声明,修改全局变量 num,否则视为未定义的局部变量
    print(num) 
    num = 123
    print(num)
fun1()
print(num)
```

2.如果要修改嵌套作用域（enclosing 作用域，外层非全局作用域）中的变量则需要 nonlocal 关键字:

```python
def outer():
    num = 10
    def inner():
        nonlocal num   # nonlocal关键字声明
        num = 100
        print(num)
    inner()
    print(num)
outer()
```
