#Python学习笔记
[TOC]
#Python 语法
##Python缩进
Python使用缩进来指示代码块。
```
if 5 > 2:
  print("Five is greater than two!")
```
##Python注释
注释以＃开头，Python将其余部分作为注释呈现
```
#This is a comment.
print("Hello, World!")
```
##多行注释
注释以"""开头和结尾，注释内容可以是单行或多行
```
"""This is a 
multiline docstring."""
print("Hello, World!")
```
#Python 变量
Python没有声明变量的命令，首次为其赋值时，会创建变量。
```
x = 5
y = "John"
print(x)
print(y)
```
变量不需要使用任何特定类型声明，甚至可以在设置后更改类型。
```
x = 4 # x is of type int
x = "Sally" # x is now of type str
print(x)
```
##变量名称
变量可以具有短名称（如x和y）或更具描述性的名称（age,carname,total_volume）。Python变量的规则：
- 变量名必须以字母或下划线字符开头
- 变量名称不能以数字开头
- 变量名只能包含字母数字字符和下划线（Az，0-9和_）
- 变量名称区分大小写（age, Age和AGE是三个不同的变量）
>变量区分大小写
##输出变量
print语句通常用于输出变量。要结合文本和变量，Python使用"+"字符：
```
x = "awesome"
print("Python is " + x)
```
还可以使用"+"字符将变量添加到另一个变量：
```
x = "Python is "
y = "awesome"
z =  x + y
print(z)
```
对于数字，"+"作为数学运算符：
```
x = 5
y = 10
print(x + y)
```
>字符串和数字无法使用"+"组合
#Python数字
Python中有三种数字类型
- int
- float
- complex
不同的数字类型会在变量被赋值时创建
在Python中想要确定任一对象的数据类型，使用type()函数
```
print(type(x))
print(type(y))
print(type(z))
```
##Int（Integer）
int是一种整数，可以是正数或者负数，没有小数，也没有长度的限制
Integers：
```
x = 1
y = 35656222554887711
z = -3255522
```
##Float(floating point number)
float是一个数，可以是正数或者负数，包含一位或者多位的小数
```
x = 1.10
y = 1.0
z = -35.59
```
##Complex
复数必须带有"j"作为虚数部分的标志
```
x = 3+5j
y = 5j
z = -5j
```
#Python 转换
##指定变量类型
利用转换可以指定变量的类型。Python使用类来定义数据类型，包括其基本类型。使用构造函数可以完成python中的数据转换
- int（） - 从整数文字构造整数，浮点文字（通过向下舍入到上一个整数）或字符串文字（提供字符串表示整数）
- float（） - 从整数文字，浮点文字或字符串文字构造一个浮点数（提供字符串表示一个浮点数或一个整数）
- str（） - 从各种数据类型构造一个字符串，包括字符串，整数文字和浮点文字
###int()
```
x = int(1)   # x will be 1
y = int(2.8) # y will be 2
z = int("3") # z will be 3
```
###float()
```
x = float(1)     # x will be 1.0
y = float(2.8)   # y will be 2.8
z = float("3")   # z will be 3.0
w = float("4.2") # w will be 4.2
```
###str()
```
x = str("s1") # x will be 's1'
y = str(2)    # y will be '2'
z = str(3.0)  # z will be '3.0'
```
#Python 字符串
python中的字符串文字由单引号或双引号括起，'hello'与"hello"相同。
可以使用打印功能将字符串输出到屏幕。例如：print("hello")。
Python中的字符串是表示unicode字符的字节数组。但是，Python没有字符数据类型，单个字符只是一个长度为1的字符串。方括号可用于访问字符串的元素。
```
a = "Hello, World!"
print(a[1]) #获取下标为1的字符，起始位置为0
```
```
b = "Hello, World!"
print(b[2:5]) #获取从第2位到第5位的字符（不包括第5位）
```
strip()：删除字符串中所有空格
```
a = " Hello, World! "
print(a.strip()) # returns "Hello, World!"
```
len()：返回字符串的长度
```
a = "Hello, World!"
print(len(a))
```
lower()：将所有字符以小写的形式返回
```
a = "Hello, World!"
print(a.lower())
```
upper()：将所有字符以大写的形式返回
```
a = "Hello, World!"
print(a.upper())
```
replace()：替换字符
```
a = "Hello, World!"
print(a.replace("H", "J"))
```
split()：将字符串以指定的符号分隔成多个子字符串
```
a = "Hello, World!"
print(a.split(",")) # returns ['Hello', ' World!']
```
##命令行字符串输入
Python允许命令行输入。通过使用input()方法可以获取用户输入
```
print("Enter your name:")
x = input()
print("Hello, ", x)
```
#Python运算符
运算符用于对变量和值执行操作。
Python具有以下几种运算符：
- 算术运算符
- 赋值运算符
- 比较运算符
- 逻辑运算符
- 身份运算符
- 成员运算符
- 按位运算符
##算术运算符
算术运算符与数值一起使用以执行常见的数学运算：
|运算符|描述|例子|
|:----:|:--:|:--:|
|+|加法|x+y|
|-|减法|x-y|
|*|乘法|x*y|
|/|除法（只取整数部分）|x/y|
|%|取余（只取余数部分）|x%y|
|**|幂运算|x**y|
|//|除法（向下取整）|x//y|
##赋值运算符
赋值运算符用于为变量赋值：
|运算符|例子|等同于|
|:----:|:--:|:--:|
|=	|x = 5	|x = 5|	
|+=	|x += 3	|x = x + 3|	
|-=	|x -= 3	|x = x - 3|	
|*=	|x *= 3	|x = x * 3|
|/=	|x /= 3	|x = x / 3|	
|%=	|x %= 3	|x = x % 3|	
|//=	|x //= 3	|x = x // 3|
|**=	|x **= 3	|x = x ** 3|	
|&=	|x &= 3	|x = x & 3|	
|\|=	|x \|= 3	|x = x \| 3|	
|^=	|x ^= 3	|x = x ^ 3|	
|\>>=	|x >>= 3	|x = x >> 3|	
|<<=	|x <<= 3	|x = x << 3|
##Python比较运算符
比较运算符用于比较两个值：
|运算符|描述|例子|
|:----:|:--:|:--:|
|==	|等于|	x == y	|
|!=	|不等于|	x != y|	
|>|大于|	x > y|	
|<	|小于	|x < y	|
|\>=	|大于或等于|x >= y	|
|<=|小于或等于|x <= y|
##Python逻辑运算符
逻辑运算符用于组合条件语句：
|运算符|描述|例子|
|:----:|:--:|:--:|
|and |如果左右都成立就返回true|x < 5 and  x < 10|	
|or	|左右有一个条件成立就返回true|x < 5 or x < 4	|
|not|反转结果，本来为true返回false|not(x < 5 and x < 10)|
##Python身份运算符
身份运算符用于比较对象，而不是它们是否相等，但如果它们实际上是同一个对象，则具有相同的内存位置：
|运算符|描述|例子|
|:----:|:--:|:--:|
|is|左右是同一个对象就返回true|x is y|	
|is not|左右不是同一个对象返回true|x is not y|
##Python成员运算符
成员运算符用于测试序列是否在对象中呈现：
|运算符|描述|例子|
|:----:|:--:|:--:|
|in|如果在序列中能找到值就返回true|x in y|
|not in|如果在序列中找不到值就返回true|x not in y|
##Python按位运算符
按位运算符用于比较（二进制）数字：
|运算符|描述|例子|
|:----:|:--:|:--:|
|&|按位与：相应位都为1则为1，否则为0|x&y|
|\||按位或：相应位有一个为1就为1，全0为0|x\|y|
|^|按位异或：相应位数字不同为1|x^y|
|~|按位取反，原本为0的变为1|~x|
|<<|左移：运算符右边指定移动的位数，高位丢弃，低位补0|x<<3|
|\>>|右移：运算符右边指定移动的位数，低位丢弃，高位补0|x>>3|
#Python 列表
##Python Collections（数组）
Python编程语言中有四种集合数据类型：
- List是一个有序和可更改的集合。允许重复的成员。
- Tuple是一个有序且不可更改的集合。允许重复的成员。
- Set是一个无序和无索引的集合。没有重复的成员。
- Dictionary是一个无序，可变和索引的集合。没有重复的成员。
##List
列表是一个有序且可更改的集合。在Python中，列表用方括号编写。
```
thislist = ["apple", "banana", "cherry"]
print(thislist)
```
##访问项目
通过参考索引号来访问列表项：
```
thislist = ["apple", "banana", "cherry"]
print(thislist[1])
```
##更改项目值
要更改特定项目的值，请参阅索引号：
```
thislist = ["apple", "banana", "cherry"]
thislist[1] = "blackcurrant"
print(thislist)
```
##循环列表
使用循环遍历列表项for ：
```
thislist = ["apple", "banana", "cherry"]
for x in thislist:
  print(x)
```
##检查项目是否存在
要确定列表中是否存在指定的项，使用in关键字：
```
thislist = ["apple", "banana", "cherry"]
if "apple" in thislist:
  print("Yes, 'apple' is in the fruits list")
```
##列表长度
确定列表中有多少项，使用 len()方法：
```
thislist = ["apple", "banana", "cherry"]
print(len(thislist))
```
##添加项目
要将项添加到列表的末尾，使用append（）方法：
```
thislist = ["apple", "banana", "cherry"]
thislist.append("orange")
print(thislist)
```
要在指定的索引处添加项，使用insert（）方法：
```
thislist = ["apple", "banana", "cherry"]
thislist.insert(1, "orange") #插入到第二个位置
print(thislist)
```
##移除项目
有几种方法可以从列表中删除项目：
```
thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")   #remove()方法删除指定的项目
print(thislist)
```
```
thislist = ["apple", "banana", "cherry"]
thislist.pop()  #pop()方法删除指定的索引（如果未指定索引，则删除最后一项）
print(thislist)
```
```
thislist = ["apple", "banana", "cherry"]
del thislist[0]     #del关键字删除指定索引
print(thislist)
```
```
thislist = ["apple", "banana", "cherry"]
del thislist    #del关键字也可以完全删除列表
```
```
thislist = ["apple", "banana", "cherry"]
thislist.clear()    #clear()方法清空列表
print(thislist)
```
##复制列表
不能使用“list2=list1”来复制列表，list2只是list1的参考，而且对list1的改动会自动映射到list2。
有一些方法可以复制，一种方法是使用内置的List方法 copy()。
```
thislist = ["apple", "banana", "cherry"]
mylist = thislist.copy()
print(mylist)
```
另一种方法是使用内置方法list()。
```
thislist = ["apple", "banana", "cherry"]
mylist = list(thislist)
print(mylist)
```
##list（）构造函数
使用list（）构造函数创建一个新列表。
```
thislist = list(("apple", "banana", "cherry"))  #注意双括号
print(thislist)
```
##列表内置方法
|方法|描述|
|:--:|:--:|
|append()|在列表的最后添加元素|
|clear()|移除列表的所有元素|
|copy()|返回列表的副本|
|count()|统计元素在里表中出现的次数|
|extend()|在现有列表末尾添加新列表|
|index()|返回某个值在列表中第一次出现的下标|
|insert()|在特定的位置插入元素|
|pop()|移除列表中的一个元素（默认最后一个），并返回该元素的值|
|remove()|移除某个值在列表中第一次出现的对应元素|
|reverse()|反转原有列表|
|sort()|列表排序|
#Python 元组
##Tuple
元组是一个有序的和**不可改变**的集合。在Python中，元组是用圆括号编写的。
```
thistuple = ("apple", "banana", "cherry")
print(thistuple)
```
##访问元组项
可以通过参考方括号内的索引号来访问元组项：
```
thistuple = ("apple", "banana", "cherry")
print(thistuple[1]) 
```
##更改元组值
创建元组后，您无法更改其值。元组是**不可改变**的。
##循环遍历元组
使用for循环遍历元组项:
```
thistuple = ("apple", "banana", "cherry")
for x in thistuple:
  print(x)
```
##检查项目是否存在
确定元组中是否存在指定的项，使用in关键字：
```
thistuple = ("apple", "banana", "cherry")
if "apple" in thistuple:
  print("Yes, 'apple' is in the fruits tuple")
```
##元组长度
要确定元组有多少项，使用len()方法：
```
thistuple = ("apple", "banana", "cherry")
print(len(thistuple))
```
##添加项目
创建元组后，您无法向其添加项目。元组是**不可改变**的。
```
thistuple = ("apple", "banana", "cherry")
thistuple[3] = "orange" # 会引起错误
print(thistuple)
```
##删除项目
>注意：无法删除元组中的项目。
元组是**不可更改**的，因此无法从中删除项目，但可以完全删除元组：
```
thistuple = ("apple", "banana", "cherry")
del thistuple   #del关键字可以完全删除的元组：
print(thistuple)    #这会引起一个错误因为该元祖不再存在
```
##tuple（）构造函数
可以使用tuple（）构造函数来创建元组。
```
thistuple = tuple(("apple", "banana", "cherry")) # note the double round-brackets
print(thistuple)
```
##元祖内置方法
|方法|描述|
|:--:|:--:|
|count()|返回某个值在元祖中出现的次数|
|index()|返回某个值在元祖中出现的位置|
#Python 集合（Set）
##Set
Set是无序和无索引的集合。在Python中，Set用大括号写成。
```
thisset = {"apple", "banana", "cherry"}
print(thisset)
```
>注意：Set是无序的，因此项目将以随机顺序显示。
##访问项目
无法通过引用索引来访问Set中的项目，因为Set是无序的，项目没有索引。但是可以使用for循环遍历，或者使用in关键字查看Set中是否存在指定值 。
```
thisset = {"apple", "banana", "cherry"}

for x in thisset:
  print(x)
```
```
thisset = {"apple", "banana", "cherry"}

print("banana" in thisset)
```
##更改项目
创建Set后，您无法更改其项目，但可以添加新项目。
##添加项目
要将一个项目添加到集合，使用**add()**方法。
要向集合中添加多个项目，使用**update()**方法。
```
thisset = {"apple", "banana", "cherry"}
thisset.add("orange")
```
```
thisset = {"apple", "banana", "cherry"}
thisset.update(["orange", "mango", "grapes"])
```
##获取Set的长度
要确定Set中有多少项，使用len()方法。
```
thisset = {"apple", "banana", "cherry"}
print(len(thisset))
```
##移除项目
要删除Set中的项目，使用**remove()**或**discard()**方法。
```
thisset = {"apple", "banana", "cherry"}
thisset.remove("banana")
```
>注意：如果要删除的项目不存在，remove()会引发错误。
```
thisset = {"apple", "banana", "cherry"}
thisset.discard("banana")
```
>注意：如果要删除的项目不存在，discard()不会引发错误。
也可以使用pop()方法删除项目，但集合是无序的，因此不会知道要删除哪一项目。
pop()方法的返回值是已删除的项目。
```
thisset = {"apple", "banana", "cherry"}
x = thisset.pop()
```
>注意：集合是无序的，因此在使用该pop()方法时不知道要删除的项目。
```
thisset = {"apple", "banana", "cherry"}
thisset.clear()     #clear()方法清空集合
```
```
thisset = {"apple", "banana", "cherry"}
del thisset     #del关键字将完全删除该集
```
##set（）构造函数
可以使用set（） 构造函数来创建一个集合。
```
thisset = set(("apple", "banana", "cherry")) # note the double round-brackets
print(thisset)
```
##Set内置方法
|方法|描述|
|:--:|:--:|
|add()|向集合中添加元素|
|clear()|移除集合中的所有元素|
|copy()|复制集合|
|difference()|返回存在于第一个集合却不存在于第二个集合中的元素|
|difference_update()|在原来的集合中移除两个集合中都存在的元素|
|discard()|删除集合中指定的元素|
|intersection()|返回集合的交集|
|intersection_update()|在原来的集合中移除后一个集合中不存在的元素|
|isdisjoint()|若两个集合中存在重复的元素，则返回true|
|issubset()|若集合为后一个集合的子集，则返回true|
|issuperset()|若后一个集合为原始集合的子集，则返回true|
|pop()|随机移除集合中的一个元素并返回被移除的元素|
|remove()|移除指定元素|
|symmetric_difference()|返回两个集合中不重复的元素集合。|
|symmetric_difference_update()|在原始集合中移除两集合重复元素，并将后一个集合的不重复元素填入原始集合|
|union()|返回两个集合的并集|
|update()|向集合中添加集合（也可是元素）|
#Python 字典
##字典
字典是一个无序，可变和具有索引的集合。在Python中，字典用大括号编写，它们具有键和值。
```
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
```
##访问项目
通过在方括号内引用其键名来访问字典的项目：
```
x = thisdict["model"]
```
get()也可以访问到相同的结果：
```
x = thisdict.get("model")
```
##改变值
通过引用其键名来更改特定项的值：
```
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["year"] = 2018
```
##循环遍历字典
可以使用for循环遍历字典。
循环遍历字典时，返回值是字典的键，但也有返回值的方法。
```
for x in thisdict:
  print(x)  #逐个打印字典中的键名
```
```
for x in thisdict:
  print(thisdict[x])    #逐个打印字典中的值
```
```
for x in thisdict.values():
  print(x)  #使用values()函数返回字典的值
```
```
for x, y in thisdict.items():
  print(x, y)   #使用items()函数循环遍历键和值：
```
##检查键是否存在
确定字典中是否存在指定的键，使用in关键字：
```
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
if "model" in thisdict:
  print("Yes, 'model' is one of the keys in the thisdict dictionary")
```
##字典长度
确定字典有多少项（键值对），使用len()方法。
```
print(len(thisdict))
```
##添加项目
通过使用新的索引键并为其分配值，可以将项添加到字典中：
```
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["color"] = "red"
print(thisdict)
```
##删除项目
有几种方法可以从字典中删除项目：
```
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.pop("model")   #pop()方法删除具有指定键名的项
```
```
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.popitem()  #popitem()方法删除最后插入的项目（在3.7之前的版本中，删除随机项目）
```
```
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict["model"]   #del关键字删除指定键名称的项目
```
```
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict    #del关键字也可以删除字典
print(thisdict)     #这会引发错误因为字典已不复存在
```
```
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.clear()    #clear()关键字清空词典
print(thisdict)
```
##复制字典
不能使用“dict2=dict1”来复制列表，dict2只是dict1的参考，而且对list1的改动会自动映射到dict2。
有一些方法可以复制，一种方法是使用内置的Dictionary方法 copy()。
```
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
mydict = thisdict.copy()
```
制作副本的另一种方法是使用内置方法 dict()。
```
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
mydict = dict(thisdict)
```
##dict（）构造函数
```
thisdict =	dict(brand="Ford", model="Mustang", year=1964)
# 注意键并不是字符串
# 注意在赋值中使用等号而不是冒号
print(thisdict)
```
##字典内置方法
|方法|描述|
|:--:|:--:|
|clear()|删除字典内的所有元素|
|copy()|返回字典的副本|
|fromkeys()|创建一个新的字典，以两个序列中的对应值分别作为键和值|
|get()|返回指定键的值（没有就返回默认值）|
|items()|返回可遍历的键值对元祖数组|
|keys()|返回一个键的列表|
|pop()|删除指定键所对应的值|
|popitem()|删除最后插入的项目（在3.7之前的版本中，删除随机项目）|
|setdefault()|get()类似，但如果键不存在于字典中，将会添加键并将值设为default|
|update()|把后一个字典的键值对更新到原始字典中|
|values()|返回字典中值的列表|
#Python If ... Else
##Python条件和If语句
Python支持数学常用的逻辑条件：
- 等于：a == b
- 不等于：a！= b
- 小于：a <b
- 小于或等于：a <= b
- 大于：a> b
- 大于或等于：a> = b

使用if关键字编写“if语句” 。
```
a = 33
b = 200
if b > a:
  print("b is greater than a")
```
##缩进
Python依赖缩进，使用空格来定义代码中的范围。
```
a = 33
b = 200
if b > a:
print("b is greater than a")    # 会引发错误
```
##ELIF(else if)
若前一个if条件不满足就尝试elif
```
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
```
##else
所有if条件均不满足就进入else
```
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
```
可以不使用elif
```
a = 200
b = 33
if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
```
##Short Hand If
如果只有一个语句要执行，则可以将其与if语句放在同一行。
```
if a > b: print("a is greater than b")
```
##Short Hand If ... Else
如果只有一个语句要执行，一个用于if，另一个用于else，则可以将它们全部放在同一行：
```
print("A") if a > b else print("B")
```
还可以在同一行上有多个else语句：
```
print("A") if a > b else print("=") if a == b else print("B")
```
##And
and关键字是一个逻辑运算符，并用于条件语句结合：
```
if a > b and c > a:
  print("Both conditions are True")
```
##Or
or关键字是一个逻辑运算符，并用于条件语句结合：
```
if a > b or a > c:
  print("At least one of the conditions is True")
```
#Python 循环
##Python循环
Python有两个原始循环命令：
- while循环
- for循环
##while循环
使用while循环，只要条件为真，我们就可以执行一组语句。
```
i = 1
while i < 6:
  print(i)
  i += 1
```
>记得增加i，否则循环将永远继续。
##break声明
使用break语句，即使while条件为真，我们也可以停止循环：
```
i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
```
##continue声明
使用continue语句，我们可以停止当前的迭代，并继续下一个：
```
i = 0
while i < 6:
  i += 1 
  if i == 3:
    continue
  print(i)
```
#for循环
for循环被用于迭代一个序列（也就是无论是一个列表，一个元组，一个字典，一组，或一个字符串）。更像是在其他面向对象编程语言中找到的迭代器方法。
使用for循环，我们可以为列表中的每个项目，元组，集合等执行一组语句。
```
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
```
##通过字符串循环
字符串都是可迭代的对象，它们包含一系列字符：
```
for x in "banana":
  print(x)
```
##break声明
使用break语句，我们可以在循环遍历所有项之前停止循环：
```
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x) 
  if x == "banana":
    break
```
```
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    break   #在打印前中断
  print(x)
```
##continue声明
使用continue语句，我们可以停止循环的当前迭代，并继续下一个：
```
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    continue    #不打印"banana"
  print(x)
```
##range（）函数
要循环一组代码指定的次数，我们可以使用range（）函数，range()返回一系列数字（默认从0开始），每次增加默认增加1，然后在指定数结束。
```
for x in range(6):
  print(x)
```
>请注意，range（6）不是0到6的值，而是值0到5。
range()函数默认为0作为初始值，但是也可以通过添加一个参数来指定起始值：range（2,6） ，这意味着从2至6的值（但不包括6）：
```
for x in range(2, 6):
  print(x)
```
range()函数默认步长为1，但是有可能通过增加第三参数指定步长：
```
for x in range(2, 30, 3):
  print(x)
```
##for循环中的else
循环中的else关键字指定for循环结束时要执行的代码块：
```
for x in range(6):
  print(x)
else:
  print("Finally finished!"
```
##嵌套循环
嵌套循环是循环内的循环。

对于“外循环”的每次迭代，“内循环”将执行一次：
```
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
  for y in fruits:
    print(x, y)
```
#Python 函数
函数是一个代码块，仅在调用时运行。

您可以将数据（称为参数）传递到函数中。

函数可以返回数据。
##创建一个函数
在Python中，使用def 关键字定义函数：
```
def my_function():
  print("Hello from a function")
```
##调用函数
要调用函数，请使用函数名称后跟括号：
```
def my_function():
  print("Hello from a function")

my_function()
```
##参数
信息可以作为参数传递给函数。

参数在括号内的函数名后面指定。您可以根据需要添加任意数量的参数，只需用逗号分隔即可。

以下示例具有一个带有一个参数（fname）的函数。当调用该函数时，我们传递一个名字，在函数内部使用它来打印全名：
```
def my_function(fname):
  print(fname + " Refsnes")

my_function("Emil")
my_function("Tobias")
my_function("Linus")
```
##默认参数值
如果我们调用没有参数的函数，它使用默认值：
```
def my_function(country = "Norway"):
  print("I am from " + country)

my_function()
```
##将List作为参数传递
可以将任何数据类型的参数发送到函数（字符串，数字，列表，字典等），并将其视为函数内的相同数据类型。
```
def my_function(food):
  for x in food:
    print(x)
fruits = ["apple", "banana", "cherry"]
my_function(fruits)
```
##返回值
让函数返回值，使用return 语句：
```
def my_function(x):
  return 5 * x

print(my_function(3))
```
##递归
Python也接受函数递归，这意味着定义的函数可以调用自身。

递归是一种常见的数学和编程概念。这意味着函数调用自身。这样做的好处是可以循环访问数据以达到结果。

开发人员应该非常小心递归，因为它可以很容易地编写一个永不终止的函数，或者使用过量内存或处理器能力的函数。但是，正确编写时，递归可能是一种非常有效且数学上优雅的编程方法。

在这个例子中，tri_recursion（）是我们定义为调用自身的函数（“recurse”）。我们使用k变量作为数据，每次递归时递减（-1）。当条件不大于0时（即，当它为0时），递归结束。
```
def tri_recursion(k):
  if(k>0):
    result = k+tri_recursion(k-1)
    print(result)
  else:
    result = 0
  return result

print("\n\nRecursion Example Results")
tri_recursion(6)
```
#Python Lambda
lambda函数是一个小的匿名函数。

lambda函数可以使用任意数量的参数，但只能有一个表达式。
##语法
>lambda arguments : expression
执行表达式并返回结果：

一个lambda函数，它将作为参数传入的数字加10，并打印结果：
```
x = lambda a : a + 10
print(x(5))
```
Lambda函数可以使用任意数量的参数：
```
#将参数a与参数b相乘并打印
x = lambda a, b : a * b
print(x(5, 6))
```
```
#将参数a，b和c相加并打印
x = lambda a, b, c : a + b + c
print(x(5, 6, 2))
```
##为什么使用Lambda函数？
将lambda用作另一个函数内的匿名函数时，会更好地显示lambda的强大功能。

假设有一个带有一个参数的函数定义，并且该参数将乘以未知数字：
```
def myfunc(n):
  return lambda a : a * n
```
使用该函数定义来创建一个总是使发送的数字加倍的函数：
```
def myfunc(n):
  return lambda a : a * n

mydoubler = myfunc(2)

print(mydoubler(11))
```
或者，使用相同的函数定义来创建一个总是使发送的数字增加三倍的函数：
```
def myfunc(n):
  return lambda a : a * n

mytripler = myfunc(3)

print(mytripler(11))
```
或者，在同一程序中使用相同的函数定义来生成两个函数：
```
def myfunc(n):
  return lambda a : a * n

mydoubler = myfunc(2)
mytripler = myfunc(3)

print(mydoubler(11)) 
print(mytripler(11))
```
>在短时间内需要匿名函数时使用lambda函数。
#Python 数组
>注意： Python没有内置的Arrays支持，但可以使用Python Lists。
##数组
数组用于在一个变量中存储多个值：
```
cars = ["Ford", "Volvo", "BMW"]
```
##什么是数组？
数组可以在单个名称下保存多个值，可以通过引用索引号来访问这些值。
##访问数组的元素
可以通过引用索引号来引用数组元素。
```
x = cars[0]
```
```
cars[0] = "Toyota"
```
##数组的长度
使用len()方法返回数组的长度（数组中的元素数）。
```
x = len(cars)
```
>注意：数组的长度总是比最高的数组索引多一个。
##循环数组元素
可以使用for in循环遍历数组的所有元素。
```
for x in cars:
  print(x)
```
##添加数组元素
可以使用append()方法将元素添加到数组中。
```
cars.append("Honda")
```
##删除数组元素
可以使用该pop()方法从数组中删除元素。
```
cars.pop(1)
``` 
可以使用该remove()方法从数组中删除元素。
```
cars.remove("Volvo")
```
>注意：该remove()方法仅删除第一次出现的指定值。
##数组(列表)内置方法
|方法|描述|
|:--:|:--:|
|append()|在列表的最后添加元素|
|clear()|移除列表的所有元素|
|copy()|返回列表的副本|
|count()|统计元素在里表中出现的次数|
|extend()|在现有列表末尾添加新列表|
|index()|返回某个值在列表中第一次出现的下标|
|insert()|在特定的位置插入元素|
|pop()|移除列表中的一个元素（默认最后一个），并返回该元素的值|
|remove()|移除某个值在列表中第一次出现的对应元素|
|reverse()|反转原有列表|
|sort()|列表排序|
>注意： Python没有内置的Arrays支持，但可以使用Python Lists。
#Python 类和对象
##Python类/对象
Python是一种面向对象的编程语言。

Python中的几乎所有东西都是一个对象，具有其属性和方法。

类就像是对象构造函数，或者是用于创建对象的“蓝图”。
##创建一个类
要创建类，使用关键字class：
```
class MyClass:
  x = 5
```
##创建对象
```
p1 = MyClass()
print(p1.x)     #创建一个名为p1的对象，并打印x
```
##__init__()函数
所有类都有一个名为__init __（）的函数，它始终在启动类时执行。

使用__init __（）函数将值赋给对象属性，或者在创建对象时需要执行的其他操作：
```
#创建一个名为Person的类，使用__init __（）函数为name和age赋值：
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

p1 = Person("John", 36)

print(p1.name)
print(p1.age)
```
>注意：__init__()每次使用类创建新对象时，都会自动调用该函数。
##对象方法
对象也可以包含方法。对象中的方法是属于该对象的函数。
```
#插入一个打印问候语的函数，并在p1对象上执行它
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)
p1.myfunc()
```
>注意：该self参数是对类的当前实例的引用，用于访问属于该类的变量。
##self参数
该self参数是对类的当前实例的引用，用于访问属于该类的变量。

它不必命名self，你可以随意调用它，但它必须是类中任何函数的第一个参数：
```
#使用单词mysillyobject和abc代替self：
class Person:
  def __init__(mysillyobject, name, age):
    mysillyobject.name = name
    mysillyobject.age = age

  def myfunc(abc):
    print("Hello my name is " + abc.name)

p1 = Person("John", 36)
p1.myfunc()
```
##修改对象属性
可以修改对象的属性，如下所示：
```
p1.age = 40
```
##删除对象属性
可以使用以下 del关键字删除对象的属性：
```
del p1.age
```
##删除对象
可以使用以下del关键字删除对象：
```
del p1
```
#Python 继承
##Python继承
继承允许我们定义一个继承另一个类的所有方法和属性的类。

父类是继承的类，也称为基类。

子类是从另一个类继承的类，也称为派生类。
##创建父类
任何类都可以是父类，因此语法与创建任何其他类相同：
```
#创建一个名为Person，with firstname和lastnameproperties 的类，以及一个printname方法：
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

x = Person("John", "Doe")
x.printname()
```
##创建一个子类
要创建从其他类继承功能的类，请在创建子类时将父类作为参数发送：
```
#创建一个名为Student的类，它将继承Person类中的属性和方法：
class Student(Person):
  pass
```
>注意：如果不想向该类添加任何其他属性或方法，请使用pass关键字。
```
#使用Student该类创建一个对象，然后执行该printname方法：
x = Student("Mike", "Olsen")
x.printname()
```
##添加__init __()函数
到目前为止，我们已经创建了一个子类，它继承了父类的属性和方法。

我们想要将该\__init__()函数添加到子类（而不是pass关键字）。
>注意：每次使用类创建新对象时，都会自动调用\__init__()函数。
```
class Student(Person):
  def __init__(self, fname, lname):
```
添加\__init__()函数时，子类将不再继承父类的\__init__()函数。
>注意：子类的\__init__()函数覆盖从父类中继承的\__init__()函数。

要保持父类中\__init__()函数的继承，请添加对父\__init__()函数的调用：
```
class Student(Person):
  def __init__(self, fname, lname):
    Person.__init__(self, fname, lname)
```
##添加属性
```
class Student(Person):
  def __init__(self, fname, lname):
    Person.__init__(self, fname, lname)
    self.graduationyear = 2019
```
```
#添加year参数，并在创建对象时传递正确的年份：
class Student(Person):
  def __init__(self, fname, lname, year):
    Person.__init__(self, fname, lname)
    self.graduationyear = year

x = Student("Mike", "Olsen", 2019)
```
##添加方法
```
class Student(Person):
  def __init__(self, fname, lname, year):
    Person.__init__(self, fname, lname)
    self.graduationyear = year

  def welcome(self):
    print("Welcome", self.firstname, self.lastname, "to the class of", self.graduationyear)
```
>如果在子类中添加一个与父类中的函数同名的方法，则将覆盖父方法的继承。
#Python 迭代器
##Python迭代器
迭代器是一个包含可数个值的对象。

迭代器是一个可以迭代的对象，这意味着您可以遍历所有值。

从技术上讲，在Python中，迭代器是一个实现迭代器协议的对象，它由方法
\__iter__() 和\__next__()。
##Iterator vs Iterable
列表，元组，字典和集都是可迭代的对象。它们是可迭代的 容器，您可以从中获取迭代器。

所有这些对象都有一个iter()用于获取迭代器的方法：
```
#从元组返回一个迭代器，并打印每个值：
mytuple = ("apple", "banana", "cherry")
myit = iter(mytuple)

print(next(myit))
print(next(myit))
print(next(myit))
```
甚至字符串都是可迭代的对象，并且可以返回迭代器：
```
mystr = "banana"
myit = iter(mystr)

print(next(myit))
print(next(myit))
print(next(myit))
```
##通过迭代器循环
还可以使用for循环遍历可迭代对象：
```
mytuple = ("apple", "banana", "cherry")

for x in mytuple:
  print(x)
```
```
mystr = "banana"

for x in mystr:
  print(x)
```
for循环实际就创建了迭代器对象，并且执行用于每个循环的next()方法。
##创建一个迭代器
要创建一个对象/类作为迭代器，您必须实现方法\__iter__()和 \__next__()。

正如在Python 类/对象一章中所了解到的，所有类都有一个名为的函数\__init__()，它允许您在创建对象时进行一些初始化。

该\__iter__()方法可以执行操作（初始化等），但必须始终返回迭代器对象本身。

该\__next__()方法也允许执行操作，但必须返回序列中的下一个项目。
```
#创建一个返回数字的迭代器，从1开始，每个序列将增加1（返回1,2,3,4,5等）：
class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self

  def __next__(self):
    x = self.a
    self.a += 1
    return x

myclass = MyNumbers()
myiter = iter(myclass)

print(next(myiter))
print(next(myiter))
print(next(myiter))
```
##StopIteration
如果有足够的next（）语句，或者它在for循环中使用，上面的示例将永远继续 。

为了防止迭代继续进行，我们可以使用StopIteration语句。

在\__next__()方法中，如果迭代完成指定的次数，我们可以添加一个终止条件来引发错误：
```
#20次迭代后停止：
class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self

  def __next__(self):
    if self.a <= 20:
      x = self.a
      self.a += 1
      return x
    else:
      raise StopIteration

myclass = MyNumbers()
myiter = iter(myclass)

for x in myiter:
  print(x)
```
#Python 模块
##什么是模块？
模块可以被视为一个代码库。

这是一个包含了一系列你想要包含在你的应用中的函数的文件。
##创建一个模块
要创建模块，只需将所需代码保存在具有文件扩展名的文件中.py：
```
#将此代码保存在名为的文件中 mymodule.py
def greeting(name):
  print("Hello, " + name)
```
##使用模块
现在可以使用刚刚创建的模块，使用以下import语句：
```
#导入名为mymodule的模块，并调用greeting函数：
import mymodule

mymodule.greeting("Jonathan")
```
>注意：使用模块中的函数时，请使用以下语法：module_name.function_name。
##模块中的变量
模块可以包含已经描述的函数，但也包含所有类型的变量（数组，字典，对象等）：
```
#将此代码保存在文件中 mymodule.py
person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
```
```
#导入名为mymodule的模块，并访问person1字典：
import mymodule

a = mymodule.person1["age"]
print(a)
```
##命名模块
可以根据需要为模块文件命名，但必须具有文件扩展名 .py
##重新命名模块
可以在导入模块时使用as关键字创建别名：
```
import mymodule as mx

a = mx.person1["age"]
print(a)
```
##内置模块
Python中有几个内置模块，可以随时导入。
```
import platform

x = platform.system()
print(x)
```
##dir()函数
有一个内置函数可以列出模块中的所有函数名称（或变量名称）。dir()函数：
```
import platform

x = dir(platform)
print(x)
```
>注意： dir（）函数可用于所有模块，也可用于自己创建的模块。
##从模块导入
可以使用from关键字选择仅导入模块的部分内容。
```
#命名的模块mymodule有一个函数和一个字典：
def greeting(name):
  print("Hello, " + name)

person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
```
```
#仅从模块导入person1字典：
from mymodule import person1

print (person1["age"])
```
>注意：使用from 关键字导入时，请勿在引用模块中的元素时使用模块名称。示例：person1["age"]，而不是~~mymodule.person1["age"]~~
#Python 日期时间
##Python日期
Python中的日期不是它自己的数据类型，但我们可以导入一个名为datetime的模块作为日期对象。
```
import datetime

x = datetime.datetime.now()
print(x)
```
##日期输出
当我们执行上面示例中的代码时，结果将类似：

2019-05-10 11:03:07.104845
日期包含年，月，日，小时，分钟，秒和微秒。

该datetime模块有许多方法可以返回有关日期对象的信息。

以下是一些示例，您将在本章后面详细了解它们：
```
#返回工作日的年份和名称：
import datetime

x = datetime.datetime.now()

print(x.year)
print(x.strftime("%A"))
```
##创建日期对象
要创建日期，我们可以使用模块的datetime()类（构造函数） datetime。

本datetime()类需要三个参数来创建日期：年，月，日。
```
import datetime

x = datetime.datetime(2020, 5, 17)

print(x)
```
datetime()类也需要参数的时间和时区（小时，分钟，秒，微秒，时区），但它们是可选的，并且具有一个默认值0，（时区默认为None）。
##strftime()方法
该datetime对象具有将日期对象格式化为可读字符串的方法。

调用该方法strftime()，并使用一个参数 format来指定返回字符串的格式：
```
#显示月份名称：
import datetime

x = datetime.datetime(2018, 6, 1)

print(x.strftime("%B"))
```
所有合法格式代码的参考：
|指令|描述|例子|
|:--:|:--:|:--:|
|%a|	Weekday, short version	|Wed|	
|%A|	Weekday, full version	|Wednesday|	
|%w|	Weekday as a number 0-6, 0 is Sunday	|3|
|%d|	Day of month 01-31	|31|	
|%b|	Month name, short version	|Dec|	
|%B|	Month name, full version	|December|	
|%m|	Month as a number 01-12	|12|	
|%y|	Year, short version, without century	|18|	
|%Y|	Year, full version	|2018|	
|%H|	Hour 00-23	|17|	
|%I|	Hour 00-12	|05|	
|%p|	AM/PM	|PM|	
|%M|	Minute 00-59	|41|	
|%S|	Second 00-59	|08|	
|%f|	Microsecond 000000-999999	|548513|	
|%z|	UTC offset	|+0100|	
|%Z|	Timezone	|CST|	
|%j|	Day number of year 001-366	|365|	
|%U|	Week number of year, Sunday as the first day of week, 00-53	|52|	
|%W|	Week number of year, Monday as the first day of week, 00-53	|52|	
|%c|	Local version of date and time	|Mon Dec 31 17:41:00 2018|	
|%x|	Local version of date	|12/31/18|	
|%X|	Local version of time	|17:41:00|	
|%%|	A % character	|%|
#Python JSON
JSON是用于存储和交换数据的语法。

JSON是用JavaScript对象表示法编写的文本。
##Python中的JSON
Python有一个名为的内置包json，可用于处理JSON数据。
```
import json
```
##解析JSON - 从JSON转换为Python
如果有JSON字符串，则可以使用json.loads()方法对其进行解析 。
>结果将是一个Python字典。
```
import json

# JSON字符串:
x =  '{ "name":"John", "age":30, "city":"New York"}'

# 解析JSON:
y = json.loads(x)

# 结果是一个Python字典:
print(y["age"])
```
##从Python转换为JSON
```
import json

# Python对象 (字典):
x = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

# 转换成JSON:
y = json.dumps(x)

# 结果是JSON字符串:
print(y)
```
可以将以下类型的Python对象转换为JSON字符串：
- dict
- list
- tuple
- string
- int
- float
- True
- False
- None
```
#将Python对象转换为JSON字符串，并打印值：
import json

print(json.dumps({"name": "John", "age": 30}))
print(json.dumps(["apple", "bananas"]))
print(json.dumps(("apple", "bananas")))
print(json.dumps("hello"))
print(json.dumps(42))
print(json.dumps(31.76))
print(json.dumps(True))
print(json.dumps(False))
print(json.dumps(None))
```
从Python转换为JSON时，Python对象将转换为JSON（JavaScript）等效项：
|Python|JSON|
|:--:|:--:|
|dict|Object|
|list|Array|
|tuple|Array|
|str|String|
|int|Number|
|float|Number|
|True|true|
|False|false|
|None|null|
```
#转换包含所有合法数据类型的Python对象：
import json

x = {
  "name": "John",
  "age": 30,
  "married": True,
  "divorced": False,
  "children": ("Ann","Billy"),
  "pets": None,
  "cars": [
    {"model": "BMW 230", "mpg": 27.5},
    {"model": "Ford Edge", "mpg": 24.1}
  ]
}

print(json.dumps(x))
```
##格式化结果
上面的示例打印了一个JSON字符串，但它不是很容易阅读，没有缩进和换行符。

json.dumps()方法具有参数，使其更容易读取结果：
```
#使用indent参数定义缩进的数量：
json.dumps(x, indent=4)
```
还可以定义分隔符，默认值为（“，”，“：”），这意味着使用逗号和空格分隔每个对象，使用冒号和空格将键与值分开：
```
#使用该separators参数更改默认分隔符：
json.dumps(x, indent=4, separators=(". ", " = "))
```
##结果排序
json.dumps()方法具有在结果中对键进行排序的参数：
```
#使用sort_keys参数指定是否对结果进行排序：
json.dumps(x, indent=4, sort_keys=True)
```
#Python RegEx
RegEx或正则表达式是形成搜索模式的字符序列。

RegEx可用于检查字符串是否包含指定的搜索模式。
##RegEx模块
Python有一个内置的包re，可以用来处理正则表达式。

导入re模块：
```
import re
```
##Python中的RegEx
导入re模块后，可以开始使用正则表达式：
```
#搜索字符串以查看它是否以“The”开头并以“Spain”结尾：
import re

txt = "The rain in Spain"
x = re.search("^The.*Spain$", txt)
```
##RegEx函数
re模块提供了一组函数，允许我们搜索字符串以进行匹配：
|功能|描述|
|:--:|:--:|
|findall|在字符串中找到正则表达式所匹配的所有子串，并返回一个列表，如果没有找到匹配的，则返回空列表。|
|search|扫描整个字符串并返回第一个成功的匹配。|
|split|方法按照能够匹配的子串将字符串分割后返回列表|
|sub|替换字符串中的匹配项|
##元字符
元字符是具有特殊含义的字符：
|字符|描述|例子|
|:--:|:--:|:--:|
|[]|A set of characters|"[a-m]"	
|\\ |Signals a special sequence (can also be used to escape special characters)|"\d"	
|.|Any character (except newline character)|"he..o"	
|^|Starts with|"^hello"	
|\$|Ends with|"world$"	
|\*|Zero or more occurrences|"aix*"	
|\+|One or more occurrences|"aix+"	
|{}|Exactly the specified number of occurrences|"al{2}"	
|\||Either or|"falls\|stays"|	
|()|Capture and group|
##特殊序列
一个特殊的序列\后跟下面列表中的一个字符，具有特殊含义：
|字符|描述|例子|
|:--:|:--:|:--:|
|\A|	Returns a match if the specified characters are at the beginning of the string	|"\AThe"|	
|\b|	Returns a match where the specified characters are at the beginning or at the end of a word	|"r\bain","rain\b"|	
|\B|	Returns a match where the specified characters are present, but NOT at the beginning (or at the end) of a word	|"r\Bain","rain\B"|	
|\d|	Returns a match where the string contains digits (numbers from 0-9)	|"\d"|	
|\D|	Returns a match where the string DOES NOT contain digits	|"\D"|	
|\s|	Returns a match where the string contains a white space character	|"\s"|	
|\S|	Returns a match where the string DOES NOT contain a white space character	|"\S"|	
|\w|	Returns a match where the string contains any word characters (characters from a to Z, digits from 0-9, and the underscore _ character)	|"\w"|	
|\W|	Returns a match where the string DOES NOT contain any word characters	|"\W"|	
|\Z|	Returns a match if the specified characters are at the end of the string	|"Spain\Z"|
##集
集合是一对方括号内的一组字符 []，具有特殊含义：
|集合|描述|
|:--:|:--:|
|[arn]|	Returns a match where one of the specified characters (a, r, or n) are present|	
|[a-n]|	Returns a match for any lower case character, alphabetically between a and n|	
|[^arn]|	Returns a match for any character EXCEPT a, r, and n	
|[0123]|	Returns a match where any of the specified digits (0, 1, 2, or 3) are present|	
|[0-9]|	Returns a match for any digit between 0 and 9|	
|[0-5][0-9]|	Returns a match for any two-digit numbers from 00 and 59|	
|[a-zA-Z]|	Returns a match for any character alphabetically between a and z, lower case OR upper case|	
|[+]|	In sets, +, *, ., \|, (), $,{} has no special meaning, so [+] means: return a match for any + character in the string|
##findall（）函数
findall()函数返回包含所有匹配项的列表。
```
import re

str = "The rain in Spain"
x = re.findall("ai", str)
print(x)
```
该列表按照找到的顺序包含匹配项。

如果未找到匹配项，则返回空列表：
```
import re

str = "The rain in Spain"
x = re.findall("Portugal", str)
print(x)
```
##search（）函数
search()函数在字符串中搜索匹配项，如果匹配则返回匹配的对象。

如果有多个匹配，则仅返回匹配的第一个匹配项：
```
#在字符串中搜索第一个空格字符：
import re

str = "The rain in Spain"
x = re.search("\s", str)

print("The first white-space character is located in position:", x.start())
```
如果未找到匹配项，则返回None：
```
import re

str = "The rain in Spain"
x = re.search("Portugal", str)
print(x)
```
##split（）函数
split()函数返回一个列表，其中字符串在每次匹配时被拆分：
```
import re

str = "The rain in Spain"
x = re.split("\s", str)
print(x)
```
可以通过指定maxsplit 参数来控制出现次数 ：
```
#仅在第一次出现时拆分字符串：
import re

str = "The rain in Spain"
x = re.split("\s", str, 1)
print(x)
```
##sub（）函数
sub()函数将匹配替换为您选择的文本：
```
#用数字9替换每个空格字符：
import re

str = "The rain in Spain"
x = re.sub("\s", "9", str)
print(x)
```
可以通过指定count 参数来控制替换次数 ：
```
#替换前两次出现：
import re

str = "The rain in Spain"
x = re.sub("\s", "9", str, 2)
print(x)
```     
##匹配对象
匹配对象是包含有关搜索和结果的信息的对象。
>注意：如果没有匹配项，将返回None，而不是匹配对象。
```
#执行将返回匹配对象的搜索：
import re

str = "The rain in Spain"
x = re.search("ai", str)
print(x) #这会打印一个对象
``` 
匹配到的对象具有用于检索有关搜索的信息的属性和方法，结果如下：

.span()返回包含匹配的开始和结束位置的元组。
.string返回传递给函数的字符串
.group()返回匹配的字符串部分
```
#打印第一个匹配事件的位置（开始和结束位置）。

正则表达式查找以大写“S”开头的任何单词：
import re

str = "The rain in Spain"
x = re.search(r"\bS\w+", str)
print(x.span())
```
```
#打印传递给函数的字符串：
import re

str = "The rain in Spain"
x = re.search(r"\bS\w+", str)
print(x.string)
```
```
#打印匹配的字符串部分。

正则表达式查找以大写“S”开头的任何单词：
import re

str = "The rain in Spain"
x = re.search(r"\bS\w+", str)
print(x.group())
```
>注意：如果没有匹配项，将返回None，而不是匹配对象。
#Python PIP
##什么是PIP？
PIP是Python包或模块的管理器。
>注意：如果您使用的是Python 3.4或更高版本，则默认情况下会包含PIP。
##什么是包？
包中包含模块所需的所有文件。

模块是您可以包含在项目中的Python代码库。
##检查PIP是否已安装
将命令行导航到Python脚本目录的位置，然后键入以下内容：
```
C:\Users\Your Name\AppData\Local\Programs\Python\Python36-32\Scripts>pip --version
```
##安装PIP
如果您没有安装PIP，可以从此页面下载并安装它：https://pypi.org/project/pip/
##下载包
下载包非常容易。

打开命令行界面并告诉PIP下载所需的软件包。

将命令行导航到Python脚本目录的位置，然后键入以下内容：
```
#下载名为“camelcase”的软件包：
C:\Users\Your Name\AppData\Local\Programs\Python\Python36-32\Scripts>pip install camelcase
```
##使用包
安装包后，即可使用。
```
#导入并使用“camelcase”：
import camelcase

c = camelcase.CamelCase()

txt = "hello world"

print(c.hump(txt))
``` 
##查找包
在https://pypi.org/上找到更多软件包。
##删除包
使用uninstall命令删除包：
```
#卸载名为“camelcase”的包：
C:\Users\Your Name\AppData\Local\Programs\Python\Python36-32\Scripts>pip uninstall camelcase
```
PIP包管理器将要求您确认是否要删除camelcase包：
```
Uninstalling camelcase-02.1:
  Would remove:
    c:\users\Your Name\appdata\local\programs\python\python36-32\lib\site-packages\camecase-0.2-py3.6.egg-info
    c:\users\Your Name\appdata\local\programs\python\python36-32\lib\site-packages\camecase\*
Proceed (y/n)?
```
按y，包将被删除。
##列出包
使用list命令列出系统上安装的所有软件包：
```
C:\Users\Your Name\AppData\Local\Programs\Python\Python36-32\Scripts>pip list
```
结果：
```
Package         Version
-----------------------
camelcase       0.2
mysql-connector 2.1.6
pip             18.1
pymongo         3.6.1
setuptools      39.0.1
```
#Python Try Except
try块允许您测试代码块以查找错误。

except块可让您处理错误。

finally无论try-和except块的结果如何，都允许您执行代码。
##异常处理
当我们调用它时发生错误或异常时，Python通常会停止并生成错误消息。

可以使用以下try语句处理这些异常：
```
#try块将生成异常，因为x未定义：
try:
  print(x)
except:
  print("An exception occurred")
```
由于try块引发错误，因此将执行except块。

如果没有try块，程序将崩溃并引发错误：
```
#此语句将引发错误，因为x未定义：
print(x)
```
#许多异常
可以根据需要定义任意数量的异常块，例如，如果要为特殊类型的错误执行特殊的代码块：
```
#如果try块引发NameError则打印一条消息,而引发其他错误时打印另一条消息：
try:
  print(x)
except NameError:
  print("Variable x is not defined")
except:
  print("Something else went wrong")
```
##ELSE
如果没有引发错误，您可以使用else关键字来定义要执行的代码块：
```
#在此示例中，try块不会生成任何错误：
try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong")
```
##finally
无论try块是否引发错误，都将执行finally块（如果已指定）。
```
try:
  print(x)
except:
  print("Something went wrong")
finally:
  print("The 'try except' is finished")
```
这对于关闭对象和清理资源非常有用：
```
#尝试打开并写入不可写的文件：
try:
  f = open("demofile.txt")
  f.write("Lorum Ipsum")
except:
  print("Something went wrong when writing to the file")
finally:
  f.close()
```
程序可以继续，文件对象已经关闭。
#Python 文件处理
文件处理是任何Web应用程序的重要组成部分。

Python有几个用于创建，读取，更新和删除文件的功能。
##文件处理
在Python中使用文件的关键功能是 open()函数。

该open()函数有两个参数; 文件名和模式。

打开文件有四种不同的方法（模式）：
```
"r" - 读取 - 默认值。打开文件进行读取，如果文件不存在则报错

"a" - 附加 - 打开要附加的文件，如果文件不存在则创建该文件

"w" - 写入 - 打开文件进行写入，如果文件不存在则创建文件

"x" - 创建 - 创建指定的文件，如果文件存在则返回错误
```
可以指定文件是应该作为二进制文件还是文本模式处理
```
"t" - 文本 - 默认值。文字模式

"b" - 二进制 - 二进制模式（例如图像）
```
##语法
要打开文件进行读取，只需指定文件名即可：
```
f = open("demofile.txt")
```
相等于
```
f = open("demofile.txt", "rt")
```
因为"r"对于读取， "t"对于文本是默认值，您不需要指定它们。
>注意：确保文件存在，否则您将收到错误消息。
#Python 文件读取
##在服务器上打开文件
假设我们有以下文件，位于与Python相同的文件夹中：

demofile.txt

>Hello! Welcome to demofile.txt
This file is for testing purposes.
Good Luck!

要打开文件，请使用内置open()函数。

open()函数返回一个文件对象，该对象具有 read()读取文件内容的方法：
```
f = open("demofile.txt", "r")
print(f.read())
```
##只读文件的一部分
默认情况下，该read()方法返回整个文本，但您也可以指定要返回的字符数：
```
#返回文件的前5个字符：
f = open("demofile.txt", "r")
print(f.read(5))
```
##读行
可以使用以下readline()方法返回一行：
```
#阅读文件的一行：
f = open("demofile.txt", "r")
print(f.readline())
```
通过调用readline()两次，您可以阅读前两行：
```
#阅读文件的两行：
f = open("demofile.txt", "r")
print(f.readline())
print(f.readline())
```
通过循环遍历文件的行，您可以逐行读取整个文件：
```
#逐行循环遍历文件：
f = open("demofile.txt", "r")
for x in f:
  print(x)
```
##关闭文件
完成文件处理后应该关闭文件：
```
#完成后关闭文件：
f = open("demofile.txt", "r")
print(f.readline())
f.close()
```
>注意：您应该在完成文件处理后关闭文件，在某些情况下，由于缓冲，在关闭文件之前，对文件所做的更改可能不会显示。
#Python 写入/创建文件
##写入现有文件
要写入现有文件，必须向open()函数添加参数 ：

"a" - 附加 - 将附加到文件的末尾

"w" - 写入 - 将覆盖任何现有内容
```
#打开文件“demofile2.txt”并将内容附加到文件中：
f = open("demofile2.txt", "a")
f.write("Now the file has more content!")
f.close()

#open and read the file after the appending:
f = open("demofile2.txt", "r")
print(f.read())
```
```
#打开文件“demofile3.txt”并覆盖内容：
f = open("demofile3.txt", "w")
f.write("Woops! I have deleted the content!")
f.close()

#open and read the file after the appending:
f = open("demofile3.txt", "r")
print(f.read())
```
>注意： “w”方法将覆盖整个文件。
##创建一个新文件
要在Python中创建新文件，请使用open()以下参数之一的方法：

"x" - 创建 - 将创建一个文件，如果文件存在则返回错误

"a" - 附加 - 如果指定的文件不存在，将创建一个文件

"w" - 写入 - 如果指定的文件不存在，将创建一个文件
```
#创建一个名为“myfile.txt”的空文件：
f = open("myfile.txt", "x")
```
```
如果文件不存在，就会创建一个新文件：
f = open("myfile.txt", "w")
```
#Python 删除文件
##删除文件
要删除文件，必须导入OS模块，然后运行其 os.remove()功能：
```
#删除文件“demofile.txt”：
import os
os.remove("demofile.txt")
```
##检查文件是否存在：
为避免出现错误，您可能需要在尝试删除文件之前检查该文件是否存在：
```
#检查文件是否存在，然后将其删除：
import os
if os.path.exists("demofile.txt"):
  os.remove("demofile.txt")
else:
  print("The file does not exist")
```
##删除文件夹
要删除整个文件夹，请使用以下os.rmdir()方法：
```
#删除文件夹“myfolder”：
import os
os.rmdir("myfolder")
```
>注意：您只能删除空文件夹。
#Python MySQL
Python可以在数据库应用程序中使用。

MySQL最受欢迎的数据库之一。
##MySQL数据库
为了能够试验本教程中的代码示例，您应该在计算机上安装MySQL。

您可以在https://www.mysql.com/downloads/下载免费的MySQL数据库 。

##安装MySQL驱动程序
Python需要MySQL驱动程序才能访问MySQL数据库。

在本教程中，我们将使用驱动程序“MySQL Connector”。

我们建议您使用PIP安装“MySQL Connector”。

PIP很可能已经安装在Python环境中。

将命令行导航到PIP的位置，然后键入以下内容：
```
#下载并安装“MySQL Connector”：
C:\Users\Your Name\AppData\Local\Programs\Python\Python36-32\Scripts>python -m pip install mysql-connector
```
##测试MySQL连接器
要测试安装是否成功，或者您是否已安装“MySQL Connector”，请创建一个包含以下内容的Python文件：
```
#demo_mysql_test.py：
import mysql.connector
```
##创建连接
首先创建与数据库的连接。

使用MySQL数据库中的用户名和密码：
```
#demo_mysql_connection.py：
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword"
)

print(mydb)
```
#Python MySQL 创建数据库
##创建数据库
要在MySQL中创建数据库，请使用“CREATE DATABASE”语句：
```
#创建一个名为“mydatabase”的数据库：
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword"
)

mycursor = mydb.cursor()

mycursor.execute("CREATE DATABASE mydatabase")
```
##检查数据库是否存在
您可以通过使用“SHOW DATABASES”语句列出系统中的所有数据库来检查数据库是否存在：
```
#返回系统数据库的列表：
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword"
)

mycursor = mydb.cursor()

mycursor.execute("SHOW DATABASES")

for x in mycursor:
  print(x)
```
或者您可以在建立连接时尝试访问数据库：
```
#尝试连接数据库“mydatabase”：
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)
```
#Python MySQL 创建表
##创建表
要在MySQL中创建表，请使用“CREATE TABLE”语句。

确保在创建连接时定义数据库的名称
```
#创建一个名为“customers”的表：
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("CREATE TABLE customers (name VARCHAR(255), address VARCHAR(255))")
```
##检查表是否存在
您可以通过使用“SHOW TABLES”语句列出数据库中的所有表来检查表是否存在：
```
#返回系统数据库的列表：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("SHOW TABLES")

for x in mycursor:
  print(x)
```
##主键
创建表时，还应该为每条记录创建一个具有唯一键的列。

这可以通过定义PRIMARY KEY来完成。

我们使用语句“INT AUTO_INCREMENT PRIMARY KEY”，它将为每条记录插入一个唯一的编号。从1开始，每个记录增加1。
```
#创建表时创建主键：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("CREATE TABLE customers (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(255), address VARCHAR(255))")
```
如果表已存在，请使用ALTER TABLE关键字：
```
#在现有表上创建主键：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("ALTER TABLE customers ADD COLUMN id INT AUTO_INCREMENT PRIMARY KEY")
```
#Python MySQL 插入表
##插入表格
要填充MySQL中的表，请使用“INSERT INTO”语句。
```
#在“customers”表中插入记录：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "INSERT INTO customers (name, address) VALUES (%s, %s)"
val = ("John", "Highway 21")
mycursor.execute(sql, val)

mydb.commit()

print(mycursor.rowcount, "record inserted.")
```
>重要！：注意声明： mydb.commit() 需要进行更改，否则不会对表进行任何更改。
##插入多行
要在表中插入多行，请使用该 executemany()方法。

该executemany()方法的第二个参数是元组列表，包含要插入的数据：
```
#使用数据填写“customers”表：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "INSERT INTO customers (name, address) VALUES (%s, %s)"
val = [
  ('Peter', 'Lowstreet 4'),
  ('Amy', 'Apple st 652'),
  ('Hannah', 'Mountain 21'),
  ('Michael', 'Valley 345'),
  ('Sandy', 'Ocean blvd 2'),
  ('Betty', 'Green Grass 1'),
  ('Richard', 'Sky st 331'),
  ('Susan', 'One way 98'),
  ('Vicky', 'Yellow Garden 2'),
  ('Ben', 'Park Lane 38'),
  ('William', 'Central st 954'),
  ('Chuck', 'Main Road 989'),
  ('Viola', 'Sideway 1633')
]

mycursor.executemany(sql, val)

mydb.commit()

print(mycursor.rowcount, "was inserted.")
```
##获取插入的ID
您可以通过询问光标对象来获取刚插入的行的ID。

>注意：如果多插入一行，则返回最后插入行的id。
```
#插入一行，然后返回ID：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "INSERT INTO customers (name, address) VALUES (%s, %s)"
val = ("Michelle", "Blue Village")
mycursor.execute(sql, val)

mydb.commit()

print("1 record inserted, ID:", mycursor.lastrowid)
```
#Python MySQL 查询数据
##从表中选择
要从MySQL中的表中进行选择，请使用“SELECT”语句：
```
#从“customers”表中选择所有记录，并显示结果：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("SELECT * FROM customers")

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```
>注意：我们使用该fetchall()方法，该方法从最后执行的语句中获取所有行。
##选择列
要仅选择表中的某些列，请使用“SELECT”语句，后跟列名称：
```
#仅选择名称和地址列：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("SELECT name, address FROM customers")

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```
##使用fetchone（）方法
如果您只对一行感兴趣，则可以使用该 fetchone()方法。

该fetchone()方法将返回结果的第一行：
```
#只获取一行：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("SELECT * FROM customers")

myresult = mycursor.fetchone()

print(myresult)
```
#Python MySQL WHERE
##带过滤选择
从表中选择记录时，可以使用“WHERE”语句筛选选择：
```
#选择地址为“Park Lane 38”的记录：结果：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT * FROM customers WHERE address ='Park Lane 38'"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```
##通配符
您还可以选择以给定字母或短语开头，包含或结束的记录。

使用%表示通配符：
```
#选择地址中包含“way”一词的记录：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT * FROM customers WHERE address LIKE '%way%'"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```
##防止SQL注入
当用户提供查询值时，您应该转义值。

这是为了防止SQL注入，这是一种常见的网络黑客技术，可以破坏或滥用您的数据库。

mysql.connector模块具有转义查询值的方法：
```
#使用placholder %s 方法转义查询值：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT * FROM customers WHERE address = %s"
adr = ("Yellow Garden 2", )

mycursor.execute(sql, adr)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```
#Python MySQL Order By
##对结果进行排序
使用ORDER BY语句按升序或降序对结果进行排序。

ORDER BY关键字默认对结果进行升序排序。要按降序对结果进行排序，请使用DESC关键字。
```
#按名称的字母顺序对结果进行排序：结果：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT * FROM customers ORDER BY name"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```
##DESC命令
使用DESC关键字按降序对结果进行排序。
```
#按名称按字母顺序对结果进行排序：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT * FROM customers ORDER BY name DESC"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```
#Python MySQL Delete From By
##删除记录
您可以使用“DELETE FROM”语句从现有表中删除记录：
```
#删除地址为“Mountain 21”的任何记录：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "DELETE FROM customers WHERE address = 'Mountain 21'"

mycursor.execute(sql)

mydb.commit()

print(mycursor.rowcount, "record(s) deleted")
```
>重要！：注意声明： mydb.commit()。需要进行更改，否则不会对表进行任何更改。
>请注意DELETE语法中的WHERE子句： WHERE子句指定应删除哪些记录。如果省略WHERE子句，则将删除所有记录！
##防止SQL注入
在delete语句中，转义任何查询的值都是一种很好的做法。

这是为了防止SQL注入，这是一种常见的网络黑客技术，可以破坏或滥用您的数据库。

mysql.connector模块使用占位符%s来转义delete语句中的值：
```
#使用占位符%s 方法转义值：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "DELETE FROM customers WHERE address = %s"
adr = ("Yellow Garden 2", )

mycursor.execute(sql, adr)

mydb.commit()

print(mycursor.rowcount, "record(s) deleted")
```
#Python MySQL Drop Table
##删除表格
您可以使用“DROP TABLE”语句删除现有表：
```
#删除“客户”表：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "DROP TABLE customers"

mycursor.execute(sql)
```
##仅在存在时丢弃
如果要删除的表已被删除，或者由于任何其他原因不存在，则可以使用IF EXISTS关键字以避免出错。
```
#
删除表“customers”（如果存在）：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "DROP TABLE IF EXISTS customers"

mycursor.execute(sql)
```
#Python MySQL Update Table
##更新表
您可以使用“UPDATE”语句更新表中的现有记录：
```
#覆盖“Valley 345”到“Canyoun 123”的地址栏：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "UPDATE customers SET address = 'Canyon 123' WHERE address = 'Valley 345'"

mycursor.execute(sql)

mydb.commit()

print(mycursor.rowcount, "record(s) affected")
```
>重要！：注意声明： mydb.commit()。需要进行更改，否则不会对表进行任何更改。
>请注意UPDATE语法中的WHERE子句： WHERE子句指定应更新的记录。如果省略WHERE子句，则所有记录都将更新！
##防止SQL注入
在update语句中，转义任何查询的值都是一种很好的做法。

这是为了防止SQL注入，这是一种常见的网络黑客技术，可以破坏或滥用您的数据库。

mysql.connector模块使用占位符%s来转义delete语句中的值：
```
#使用placholder %s 方法转义值：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "UPDATE customers SET address = %s WHERE address = %s"
val = ("Valley 345", "Canyon 123")

mycursor.execute(sql, val)

mydb.commit()

print(mycursor.rowcount, "record(s) affected")
```
#Python MySQL Limit
##限制结果
您可以使用“LIMIT”语句限制从查询返回的记录数：
```
#选择“customers”表中的5个第一条记录：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("SELECT * FROM customers LIMIT 5")

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```
##从另一个位置开始
如果要从第三条记录开始返回五条记录，可以使用“OFFSET”关键字：
```
#从位置3开始，返回5条记录：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("SELECT * FROM customers LIMIT 5 OFFSET 2")

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```
#Python MySQL Join
Join两个或更多表
您可以使用JOIN语句，根据它们之间的相关列组合两个或多个表中的行。

考虑您有“用户”表和“产品”表：
```
#用户
{ id: 1, name: 'John', fav: 154},
{ id: 2, name: 'Peter', fav: 154},
{ id: 3, name: 'Amy', fav: 155},
{ id: 4, name: 'Hannah', fav:},
{ id: 5, name: 'Michael', fav:}
#制品
{ id: 154, name: 'Chocolate Heaven' },
{ id: 155, name: 'Tasty Lemons' },
{ id: 156, name: 'Vanilla Dreams' }
```
可以使用用户的fav字段和产品 id字段来组合这两个表。
```
#加入用户和产品，查看用户最喜欢的产品名称：

import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  passwd="yourpassword",
  database="mydatabase"
)

mycursor = mydb.cursor()

sql = "SELECT \
  users.name AS user, \
  products.name AS favorite \
  FROM users \
  INNER JOIN products ON users.fav = products.id"

mycursor.execute(sql)

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```
>注意：您可以使用JOIN来代替INNER JOIN。他们都会给你相同的结果。
##LEFT JOIN
在上面的示例中，Hannah和Michael被排除在结果之外，这是因为INNER JOIN仅显示匹配的记录。

如果要显示所有用户，即使他们没有喜欢的产品，也请使用LEFT JOIN语句：
```
#选择所有用户及其喜爱的产品：

sql = "SELECT \
  users.name AS user, \
  products.name AS favorite \
  FROM users \
  LEFT JOIN products ON users.fav = products.id"
```
##right join
如果您想要返回所有产品以及将它们作为自己喜欢的用户，即使没有用户将它们作为自己喜欢的用户，也请使用RIGHT JOIN语句：
```
#选择所有产品以及将其作为收藏的用户：

sql = "SELECT \
  users.name AS user, \
  products.name AS favorite \
  FROM users \
  RIGHT JOIN products ON users.fav = products.id"
```
>注意：没有最喜欢的产品的汉娜和迈克尔不包括在结果中。
#Python MongoDB
Python可以在数据库应用程序中使用。

最受欢迎的NoSQL数据库之一是MongoDB。
##MongoDB
MongoDB将数据存储在类似JSON的文档中，这使得数据库非常灵活和可伸缩。

为了能够试验本教程中的代码示例，您需要访问MongoDB数据库。

您可以在https://www.mongodb.com下载免费的MongoDB数据库 。
##PyMongo
Python需要一个MongoDB驱动程序来访问MongoDB数据库。

在本教程中，我们将使用MongoDB驱动程序“PyMongo”。

我们建议您使用PIP安装“PyMongo”。

PIP很可能已经安装在Python环境中。

将命令行导航到PIP的位置，然后键入以下内容：
```
#下载并安装“PyMongo”：

C:\Users\Your Name\AppData\Local\Programs\Python\Python36-32\Scripts>python -m pip install pymongo
```
##测试PyMongo
要测试安装是否成功，或者您是否已安装“pymongo”，请创建一个包含以下内容的Python页面：
```
#demo_mongodb_test.py：

import pymongo
```