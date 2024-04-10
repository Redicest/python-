# python基础学习整理
这是近期对于python学习内容的整理，基本为基础知识，可能会有后续添加
## 注释
行注释：#
块注释：''' '''
## 数值

1. 随机数
```
#range(a,b)创建a~(b-1)的一组数，用list()转换为列表
my_list=list(range(1,6))
print(my_list)

[1, 2, 3, 4, 5]
```
2. 统计计算
```
#min()找最小，max()找最大，sum()求和
digits=[1,2,3,4,5,6,7,8,9,0]
min_num=min(digits)
max_num=max(digits)
sum_num=num(digits)
print(f"{min_num} {max_num} {sum_num}")

0 9 45
```
## 字符串
#### 示例：
```
my_string='Hello Hello Hello'
```
#### 规则： 
1. 字符串可相加
```
str1='Help '
str2='me'
str3=str1+str2
print(str3)

Help me
```
#### 函数：
以my_string作为字符串变量示例 my_string='9'
1. my_string.upper()全大写
2. my_string.lower()全小写
3. my_string.strip()消除字符串两端空白(rstrip()/lstrip()消除左右两端空白)
4. my_string.removeprefix('https')消除前缀
5. num=int(my_string)/num=float(my_string)字符串转数值

## 列表
#### 示例
```
my_list=['bicycle',9,'blue']
```
#### 规则
以list=['car','bird','fire']作为列表示例
1. 访问
```
#索引调用(从0开始)
element1=list[0]
print(element1)

car
```

```
#末尾索引(从-1开始)
element1=list[-1]
print(element1)

fire
```
2. 修改
```
#索引修改
list[1]=cat
print(list)

['car', 'cat', 'fire']
```
3. 添加
```
#append末尾追加
list.append('duty')
print(list)

['car', 'bird', 'fire', 'duty']
```

```
#insert插入
list.insert(1,'hello')
print(list)

['car', 'hello', 'bird', 'fire']
```
4. 删除
```
#del删除
del list[0]
print(list)

['bird', 'fire']
```

```
#pop末尾弹出
element1=list(pop)
print(element1)

fire


#pop任意弹出
element1=list(1)
print(element1)

bird
```

```
#remove移除列表中第一个特定值
list.remove('bicycle')
print(list)

[9, 'blue']
```
5. 排序
```
#sort首字母永久排序
list.sort(reverse=False)
print(list)

['bird', 'car', 'fire']
```

```
#sorted首字母临时排序
print(list.sorted(reverse=False))
print(list)

['bird', 'car', 'fire']
['car', 'bird', 'fire']
```

```
#reverse反转列表顺序
list.reverse()
print(list)

['fire', 'bird', 'car']
```
6. 长度
```
num=len(list)
print(num)

3
```
7. 切片
```
#指定索引下标获得列表的一部分(不是指向而是复制)
list2=list[]
```
## 切片
注：指定索引下标获得列表的一部分(不是指向而是复制)
#### 示例
```
list1=['color', 'density', 'weight', 'strength']
list2=list1[1:2]
print(list2)

['density', 'weight']
```
#### 规则
以list=['color','density','weight','strength']为示例列表
1. 不同的下标指定
```
#两头索引指定片段
list2=list[1:2]
print(list2)

['density', 'weight']
```

```
#一头索引
list2=list[0:2]
print(list2)

['color', 'density', 'weight']
```
2. 列表复制
```
#用完整切片进行复制
list2=list[:]
print(list2)

['color', 'density', 'weight', 'strength']
```
## 元组
#### 示例
```
paper=('white', 'soft')
```
#### 规则
注：元组为不可变列表，只可整体重新赋值而不可修改元素
## 字典
#### 示例：
```
user={'username':'Peter', 'gender'='male','age'=22}
```
#### 规则
以user={'username':'Peter', 'gender'='male','age'=22}作为字典示例
1. 访问
```
#键名调用
element1=user['username']
print(element1)

'Peter'
```

```
#get()访问
element1=user.get('username')
print(element1)

Peter
```
2. 修改
```
#键名修改
user['username]='Keven'
print(user)

{'username':'Keven', 'gender'='male','age'=22}
```
3. 添加
```
#直接后置添加
user['job']='student'
print(user)

{'username':'Peter', 'gender'='male', 'age'=22, 'job'='student'}
```
4. 删除
```
#del删除
del user['gender']
print(user)

{'username':'Peter', 'age'=22, 'job'='student'}
```
5. 遍历
```
#dirc.items()遍历键值对
for key,value in user.items()
    print(key)
    print(f"{value}\n")

username
Peter

age
22

job
student
```

```
#dirc.keys()遍历键
for key in user.keys()
    print(user[key])

Peter
male
22


#sorted()按顺序遍历键
for key in sorted(user.keys())
    print(user[key])

22
male
Peter
```

```
#dirc.values()遍历值
for value in user.values()
    print(value)

Peter
male
22
```
## 集合
set()强制转换为集合
## for循环
以list=['car','bird','fire']作为列表示例
#### 示例：
```
for element in list:
    print(element)

car
bird
fire
```
#### 规则：
```
#element为变量名，aggregation为集合(列表，元组，字典，...)，用element对该集合进行遍历
for element in aggregation：
```
## while循环
#### 示例：
```
while a<1:
```
#### 循环操作
```
#break跳出循环
```

```
#continue进入下次循环
```
## if语句
#### 示例：
```
if a==b:
```
#### 判断条件：
1. 基本判断
```
#字符串/数值等的>,<,>=,<=,==,!=
```
2. 多条件检查
```
#and全真过，or但个过
```
3. 是否在列表中
```
#in判断
if element in list:
```
## 输入输出
```
#input()输入
message=input('Please input your name')
```
## 函数
#### 示例：
```
def function(my_string):
    print(my_string)
```
#### 规则：
以一下函数作为示例
```
def function(my_string):
    print(my_string)
```
1. 参数传递
```
#位置实参，按照顺序传递(和一般传递相同)
```

```
#关键字实参
function(my_string='hhhhhhhhhhh')
```

```
#*传递任意数量实参
def function0(*my_string):
    print(my_string)

function0('s')
function0('s','h','a','k','e')

('s',)
('s', 'h', 'a', 'k', 'e')
```
2. 默认值
```
#在定义函数给实参定义默认值(一定要写在没有默认值的实参的前面)
def function1(my_string1,my_string2='hhhhhhhh'):
    print(my_string1)
    print(my_string2)

function1('wwwww')

wwwww
hhhhhhhh
```
## 模块导入
#### 示例：
```
import lib1
```
#### 规则：
以lib1作为导入模块,function1为其中一个函数

1. 导入模块
```
#导入全部模块
import lib1
```

```
#导入特定函数
from lib1 import function1
```

```
#as指定别名
import lib1 as lib
from lib1 import function1 as function
```

```
#导入模块全部函数
from lib1 import *
```
2. 模块及函数调用
```
#调用函数
注：通过函数名/别名直接调用
```

```
#模块调用
lib1.function1()
```
## 类
#### 示例：
```
#以创建Dog为例
class Dog:
    def __init__(self,name,age):
        self.name = name
        self.age = age
    species='Dog'
    def sit():
        print(f"{self.name} is now sitting")
```
#### 规则：
1. self参数
```
#创建类必有的第一个参数，实际不需要调用
 在类定义中所有参数都需要有self.前缀
 同样，类中定义的所有的函数都需要有self作为第一个参数
def sit():
print(f"{self.name} is now sitting")
```
2. 初始化
```
#__init__()初始化
def __init__(self,name,age):
    self.name = name
    self.age = age
```
3. 继承
```
#继承的用法
class Spicaldog(Dog):#指明父类
    def __init__(self,name,age,color):
        super().__init__(self,name,age)#super()调用父类初始化方法
        self.color=color
    def getInf(self):
        return f"{self.name} {self.age} {self.color}"
```
4. 组合
```
#组合的用法
在__init__方法中使用
self.class1=Class1()进行实例化
```
5. 导入类
```
#导入单(多)个类
from class1 import Class1, Class2
```
## 读写文件
#### 规则：
1. 读取文件
```
#读取文件的流程
from pathlib import Path #导入Path类

path=Path(C:/documents/test.txt) #创建路径path
contents=path.read_text() #用read_text()函数读取字符串
```

```
#用.splitlines()对读取到的字符串进行分行，返回2层列表嵌套
lines=contents.splitlines()
```
2. 写入文件
```
#写入文件流程
from pathlib import Path #导入Path类

path=Path("C:/documents/test.txt") #创建路径
path.write_text("Hello") #写入数据
```
3. json格式的存储和读取,json.dumps()和json.loads()
```
#json.dumps()进行字符串->json格式转换
from pathlib import Path
import json

numbers=[2,3,4,5,8]
numbers=json.dumps(numbers)
print(numbers)

[2, 3, 4, 5, 8]
```

```
#json.loads()进行json->字符串格式转换
from pathlib import Path
import json

path=Path("C:/documents/test.json")
contents=path.read_text()
contents=json.loads(contents)
print(contents)

...
```
## 异常处理
```
#try-except-else对可能出现问题的代码块进行防范
from pathlib import Path

path=Path(C:/documents/test.txt)
try:
    contents=path.read_text()
except:
    print("You haven't created the file)
```
## pip第三方包安装
1. 第三方包安装
```
$ python -m pip install --user package_name
```