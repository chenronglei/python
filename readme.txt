selenium  https://github.com/chenronglei/SELENIUM  chenronglei@163.com/608806crl

pip安装太慢，可以用下面方法解决：
pip install XXX -i https://pypi.tuna.tsinghua.edu.cn/simple


linux系统在线安装 apt install tree



中谷Python中文视频教程（全38集）

01.走进Python
1.Python特征
a.简单易学  b.解释性&编译性  c.面向对象  d.高级语言，无需考虑管理内存  e.可扩展性及可嵌入式  d.开源、免费   f.可移植性   g.丰富的库

02. 开始编程吧
交换模式、文本模式

执行脚本 
a.   python 1.py  
b    ./1.py        #必须赋予可执行权限   +  python脚本路径  #! /usr/bin/python  （python3使用类似 #! /usr/bin/python3.5 ）

    问题:在windows系统下写的python脚本，在linux下赋予权限chmod +x xxx.py 以后，执行./xxx.py运行提示：bash: /usr/bin/autocrorder: /usr/bin/python^M: bad 
interpreter: No such file or directory
    分析：这是不同系统编码格式引起的：在windows系统中编辑的.sh .py文件可能有不可见字符，所以在Linux系统下执行会报以上异常信息。一般是因为windows行结尾和
linux行结尾标识不同造成的。
   解决:在Linux中转换：
        第一种方法:
        a.利用如下命令查看文件格式
           :set ff 或 :set fileformat
        b.利用如下命令修改文件格式
            :set ff=unix 或 :set fileformat=unix
        第二种方法:
            dos2unix xxx.py


SyntaxError  语法错误
exit() 退出交换模式

文件类型
a,源代码 .py
1.py

b.字节代码  .pyc         #源文件编译生成.pyc文件 
需要引入模块  
import py_compile
py_complie.compile('1.py')
python 2.py                  #生成 1.pyc文件

c. 优化代码 .pyo
python -O -m py_compile 1.py   #生成 1.pyo文件

b,c执行更快，但a使用方便

03.变量
变量可以以字母、数字、下划线组成，但不能以纯数字或数字开头
变量是计算机内存中的一块区域，变量是内存数据的标签
NameError 变量、函数等没有定义

查看变量在内存中的地址
id(a)

04.运算符（表达式）
赋值运算符   =  +=   -=   *=    /=     %=

算术运算符  + - * /    
 //  整除法
 %
 3.0/2    小数除法
 **     指数  

关系运算符
<  > <=  >= !=    ==
True
False


逻辑运算符
and
or 
not


算术优先级高于赋值运算

交互输入
a=raw_input()  字符串
a=int(raw_input())  数字
a=int(raw_input(“please input num1:”))  提示输入


05.数据类型（数字和字符串）
测试数据类型 tpye()

数字
整形、长整型(123L)、浮点型(1.0)、复数(3.14j)

字符串
''              ""    """ """
三重引号可以定义doc文档，一段代码的注释，换行
单引号、双引号没有本质区别， 注意内容有单引号，必须使用双引号
如果内容中有单、双引号，可以加转义字符 \
字符串换行可以使用 \n,也可以使用三重引号
main = """tom:
				 i am jack
				 goodbye
			"""
a= 'abcde'
a[0]+a[1]  'ab'
a[1:4]       'bcd'切片 
a[1:4:2]     'bd'  分别是起始值、结束值（不包括自己）、步长
a[-1:-4:-1]   'edc'   起始值-1表示最后一个值，步长-1表示从右往左取值

取前面5个stmp[:5]
取后面5个stmp[-5:]
从前面开始取，不包括最后两个stmp[:-2]
从第1个取到第2个stmp[0:2]
从前面开始取，不包括前面两个stmp[2:]

元组
列表
字典 

06.元组
字符串、元组、列表都是序列。，
序列的2个主要特征：索引操作符、切片操作符

序列的基本操作
len
+     连接2个序列
*      重复出现 str1*5
in     判断元素是否在序列中 ‘c' in str1(字典的键值用in判断)
max()
min()
cmp(str1,str2)   比较序列是否相同，相等等于0，str1>str2,返回1   str1<str2,返回-1    (字母大于数字)


不能修改整数、字符串、元组中的值（重新赋值不是修改，占用内存空间已变，不是在原空间上进行修改）

t=（“milo",30,"male')）

创建单个元素的元组
t=(1,)

元组中的元素可以是整数、字符串、列表等

批量赋值
>>> a,b,c=(1,2,3)
>>> a
1
>>> b
2
>>> c
3

07.列表
列表元素可以是数字、字符串、元组
可以修改元素值

创建单个元素的列表
t=[1]

listmile=['zou',30,'male']
listmile[0]='lucy'
修改列表单个元素值，列表存储空间不变

列表中增加元素
listmile.append("12345578")

列表中删除元素（多个的话，删除第一个出现的）
listmile.remove("12345578")
del(listmile[0])

删除列表
del(listmile)

IndexError索引错误，超过索引值

查看帮助
help(list.append)
q退出

列表是一个类，类实例化就是对象，通过对象的属性和方法进行操作

08.字典
zip(list1,list2) 将list1,list2的值一一隐射成元组

字典是可变的，但字典的键必须使用不可变的对象,;字典是无序的
dic={'name':0,1:1,2:2}
dic['name']=0
dic[1]=2

遍历字典
for i in dic:
    print i
	print dic[i]
	
字典增加元素
dic['tel']='12345678'

字典修改元素
dic['tel']='1234569'

字典删除元素
del(dic['tel'])
dic.pop('tel')  弹出

字典删除所有元素
dic.clear()

删除字典
del(dic)   #del可以删除所有变量

dic.get(key,default=None)  返回key的value,如果不存在，返回None
dic1.get('name1','error')      返回key的value,如果不存在，返回'error'

dic1.keys()                  返回字典中键，以列表的形式
>>> dic1.items()
[('name', 'lucy'), ('sex', 'female')]

dic1.items()                 返回键值对元组的列表
>>> dic1.keys()
['name', 'sex']

dic1.values()                返回字典中值，以列表的形式

len(dic1)                       返回字典长度


09.流程控制(if语句)
if expression:
    statement(s)     #使用4个空格或tab代替缩进
	
IndentationError  缩进报错

非空的量是True
0，None，空是False

if expression:
    statement(s) 
elif  expression:
    statement(s) 
else:
    statement(s) 
	
10.流程控制（逻辑）
and or not
尽量不用嵌套

11.流程控制(for语句)
遍历字符串、列表、元组
for x in "abcd":
    print "lucy",x
	
range(i,j,步进值) i为初始值，不选的话是0，j是终止值
for x in range(100) 

12.流程控制（遍历序列和字典）
s = "abcd"
for  x  in range(len(s)):
    print s[x]

遍历字典的2种方式：
d = {1:11,2:12}	
for x in dic1:
	print dic1[x]
	
for  k,v in d.items():
	print k,v
	
	
13.流程控制（循环控制）

d = {1:11,2:12}	
for x in dic1:
	print dic1[x]
	if x == 2:
		pass                        #代码桩，不做任何操作
	if x == 5:
		exit()                        #跳出整个程序
else:                                #for循环正常结束会执行else;Ctrl+c强制终止、break，不会执行else
	print "ending"

#停顿一秒	
import time
time.sleep(1)    

14.流程控制（while)
while循环，为真一直执行

x= ""
while x != 'q':                           #输入不为q执行
	print 'lucy'
	x = raw_input("please input q for quit")
	if not x:                                 #不输入退出
		break
else:                                         #正常结束执行else；break跳出不执行else
	print 'ending...'
	
15.函数（定义和调用）
函数可以在程序的不同的地方多次执行，不需要重复编写
自定义函数、预定义的Python函数

def 函数（参数列表）:
函数名字有多个单词，第二个单词开始首字母大写

16.函数（形参实参默认参数）
定义函数时是形参，调用函数时是实参
#coding:utf8              linux是utf8编码输入中文，windows是gbk编码

缺省参数（默认参数）,不传值使用默认参数，传值使用传的值
def machine(x,y='奶油'):              #缺省参数从右向左编写，从左向右有语法错误（SyntaxError: non-default argument follows default argument）
    print "produce",x,"元",y,"口味的冰激凌"
	
machine(10)
machine(x=10,'巧克力')


17.函数（变量作用域）
局部变量和全局变量
函数里声明全局变量，要调用函数才生效  global   
vi中显示行号   vi /etc/vimrc行尾增加:set number(shift+G 直接到行尾)
vi中不显示行号   vi /etc/vimrc行尾增加:set nonumber(shift+G 直接到行尾)

18.函数及return返回值
默认返回None
return执行后，函数终止
可以返回任何值，数字、字符串、列表等

sum([1,2,3,4,5])    15
sum((1,2,3,4,5))    15

19.函数冗余参数
多类型传值
t=('name','milo')
def f(x,y):
	print "%s :%s"  % (x,y)             #格式化输出

>>>f(*t)                                              #声明*t是一个元组,元组的元素个数与函数形参数量一致
name : milo

 #字典中的key与函数形参一一对应，名称一样
>>> def f(name,age):
... 	print "%s : %s" % (name,age)
... 
>>> d
{'age': 30, 'name': 'lucy'}
>>> f(**d)
lucy : 30


传值冗余
def f(x,*args):
	print x
	print args
>>> f(1)
1
()
>>> f(1,2,3)
1
(2, 3)

def f(x,*args,**kwargs):
	print x
	print args
	print kwargs
	
>>> f(1)
1
()
{}
>>> f(1,2,3)
1
(2, 3)
{}
>>> f(x=1)
1
()
{}
>>> f(x=1,y=2)
1
()
{'y':2}

20.函数lambda匿名函数
lambda函数是一种快速定义单行的最小 函数,没有函数名字

def f(x,y):
	return x*y
	
g=lambda x,y:x*y
g(2,3)

使用reduce进行5的阶乘计算
>>> l = range(1,6)
>>> def f(x,y):
... 	return x*y
... 
>>> reduce(f,l)
120

直接使用lambda函数
>>> reduce(lambda x,y:x*y,l)
120

21.Switch实现
python没有提供switch语句，可以使用字典实现

from __future__ import division  #除法按小数

def jia(x,y):
    print x+y
    return x+y

def jian(x,y):
    return x-y

def cheng(x,y):
    print x*y
    return x*y

def chu(x,y):
    return x/y
	
d = {'+':jia,'-':jian,'*':cheng,'/':chu}

def f(x,o,y):
    print d.get(o)(x,y)

f(2,"/",3)

22.内建函数
abs(-2)     求绝对值
max([1,2,3,4,5])   求最大值
min                     最小值
len()                    求序列的长度
divmod(5,2)         求商和模
pow(2,3)              2的三次方
round(2)              整数转成浮点数
callable()              测试函数是否是可调用
isinstance(l,list)     判断类型
cmp('lucy','lili')                    判断2个对象是否一致
range(10)                           获取序列
xrange(10)                          获取序列的生成器，比range效率高

类型转换函数
type()
int()
long()
float()
str()
list()
tuple()

>>> l=[1,2,3,4,5]
>>> tuple(l)
(1, 2, 3, 4, 5)


23.内建函数（字符串处理）
str.capitalize()                  首字母大写
str.upper()                         字母大写
str.lower()                         字母小写
str.replace('hello','good')    hello转换成good

str.split('.')                          f
分割，默认以空格分割,
>>> ip 
'192.168.1.123'
>>> ip.split('.')
['192', '168', '1', '123']
>>> ip.split('.',1)           #1表示只进行一次分割
['192', '168.1.123']


查看帮助
help(str.replace)


使用string进行操作
import string
string.replace(s,'hello','good')  hello转换成good  python2
str.replace(s,'hello','good')  hello转换成good  python3

序列处理函数
len()
max()
min()

filter()             #返回值为True的保存下来
>>> def f(x):
...     if x>5:
...         return True
... 
>>> f(10)
True
>>> l = range(10)
>>> filter(f,l)
[6, 7, 8, 9]

zip()
map()
reduce()

24.内建函数（序列处理）
zip()                          #以最短的合并，注意python3中zip函数接受任意多个可迭代对象作为参数,将对象中对应的元素打包成一个tuple,然后返回一个可迭代的zip对象.       
>>> name = ['mile','zou','tom']
>>> age=[20,30,40]
>>> tel=['133','156','189']
>>> test=[1,2]
>>> zip(name,age,tel)
[('mile', 20, '133'), ('zou', 30, '156'), ('tom', 40, '189')]
>>> zip(name,age,tel,test)
[('mile', 20, '133', 1), ('zou', 30, '156', 2)]




map()                         #以最长的合并 ，没有以None填充 。注意python3中map函数返回一个map对象，使用list(map())，返回结果
>>> map(None,name,age,tel)
>>> map(None,name,age,tel,test)
[('mile', 20, '133', 1), ('zou', 30, '156', 2), ('tom', 40, '189', None)]
[('mile', 20, '133'), ('zou', 30, '156'), ('tom', 40, '189')]

>>> a=[1,3,5]
>>> b=[2,4,6]
>>> def mf(x,y):
...     return x+y
... 
>>> map(mf,a,b)
[3, 7, 11]



reduce()
>>> l= range(1,101)
>>> def f(x,y):
...     return x+y
... 
>>> reduce(f,l)
5050

或
>>> reduce(lambda x,y:x+y,l)
5050

filter也可以使用lambda
filter(lambda x:x%2==0 , l)

25.包和模块
模块是python组织代码的基本方式
当.py脚本被导入(import)到其他脚本中运行时，我们将其称为模块

模块名与脚本的文件名相同
switch.py:
from __future__ import division  #除法按小数

def jia(x,y):
    print x+y
    return x+y

def jian(x,y):
    return x-y

def cheng(x,y):
    print x*y
    return x*y

def chu(x,y):
    return x/y
	
d = {'+':jia,'-':jian,'*':cheng,'/':chu}

def f(x,o,y):
    print d.get(o)(x,y)

if  __name__  ==  "__main__"                        #执行python switch.py显示__main__,,下面继续执行    new.py调用显示switch，下面的不执行
	f(2,"/",3)

new.py:
import switch
switch.jia(1,2)
或
from switch import jia
jia.(1,2)

python导入模块的顺序：
当前目录下查找
lib目录下

查找python相关文件  rpm -ql python
linux查找.py文件   find / -name '*.py'

Python的模块可以按目录组织为包
创建包的步骤：
创建一个名字为包名字的文件夹
在该文件夹下创建一个__init__.py文件
根据需要在目录下放置脚本

import csvtpy.switch           #csvtpy是包名，switch是脚本名（模块）
print csvtpy.switch.jia(1,2)   


26.正则表达式（初始）
正则表达式是一种小型、专业化的编程语言

使用正则表达式，需要导入re模块


字符匹配
普通字符
>>> import re
>>> s = r'abc'
>>> re.findall(s,"123abc12abc")
['abc', 'abc']

元字符
. ^ $ * + ? {} [] \ | ()

[] 制定一个字符集，匹配其中的一个字符
>>> s = r 'a[a-z]c'
>>> re.findall(s,"abc a1c azc")
['abc', 'alc', 'azc']
s = r 'a[^ab]c'   # 在[]中^表示取反
元字符在[]中不起作用
[0-9]        #所有数字
[a-zA-Z0-9]  #所有字母和数字

^ 匹配行首
>>> re.findall(r'^hello','hello 12 hello hello2')
['hello']


$ 匹配行尾
>>> re.findall(r'hello$','hello 12 hello 2hello')
['hello']



27.正则表达式（元字符）

\        
a.想要匹配元字符，需要在元字符前加 \
>>> re.findall(r'\^abc','^abc b^abc')
b.  \后面加不同的字符可以表示不同的特殊含义
\d     表示任意的数字字符，相当于[0-9]
\D     表示任何非数字字符   [^0-9]
\w     表示任意的字母数字字符 ，相当于[0-9a-zA-Z]
\W     表示任意的非字母数字字符 ，相当于[^0-9a-zA-Z]
\s     表示任意空白字符，相当于[\t\n\r\f\v]                       #用户名注册会用到
\S     表示任意非空白字符，相当于[^\t\n\r\f\v]


.       匹配任意字符，除了换行符
*      重复  前面一个字符0次到多次

r'^010-\d{8}'              {}匹配前面一个字符重复8次

+      重复  前面一个字符1次到多次    

？     重复  前面一个字符0次或1次
       实现最小匹配
>>> re.findall(r'ab+','abbbbbbbbbbbbbbbbbbbbbbbbbbbbbb')                      #贪婪匹配
['abbbbbbbbbbbbbbbbbbbbbbbbbbbbbb']
>>> re.findall(r'ab+?','abbbbbbbbbbbbbbbbbbbbbbbbbbbbbb')                     #最小匹配
['ab']


{} 重复  前面一个字符重复次数
{1,3}   重复1到3次
{3}     重复3次


28.正则表达式（常用函数）
编译
>>> p_tel=re.compile(r'010-?\d{8}')
>>> p_tel.findall('010-12345678')
['010-12345678']

不区分大小写
>>> p_csvt=re.compile(r'csvt',re.I)
>>> p_csvt.findall('csvt CSvt1')
['csvt', 'CSvt']

#match开头匹配到(非开头匹配到的不算)，返回一个对象，否则返回空
>>> p_csvt.match('csvt CSvt1')          
<_sre.SRE_Match object at 0x7fe4d18ce648>       
>>> p_csvt.match('cs1vt C2Svt1')
>>> p_csvt.match('cs1vt CSvt1')

>>> x= p_csvt.match('csvt CSvt1')   #返回match匹配的字符串
>>> x.group()
'csvt'
实际使用中是将Match返回的对象保存在一个变量里，然后检查它是否为None



#search任意位置匹配到，返回一个对象，否则返回空
#findall()  返回所有匹配到的子串，并以列表形式返回
#finditer()  返回所有匹配到的子串，并以迭代器形式返回，以next()方法查看里面的值是match对象


re.sub         #进行替换，与replace对比可以进行正则，replace只能对具体字符
>>> rs=r'c..t'
>>> re.sub(rs,'python','csvt caat cvvt ccccct')
'python python python ccpython'
>>> re.subn(rs,'python','csvt caat cvvt ccccct')
('python python python ccpython', 4)          #统计匹配次数


split 切割
>>> ip = '1.2.3.4'
>>> ip.split('.')
['1', '2', '3', '4']

>>> s = '123+456-789*000'    
>>> re.split(r'[\+\-\*]',s)    #正则切割，+-* 是特殊字符，加\转义
['123', '456', '789', '000']


29.正则表达式（re属性分组）
便宜标志
S  使.匹配包括换行在内的所有字符
I  忽略大小写
M  进行多行匹配
>>> s = """
... hello csvt
... csvt hello
... hello csvt hello
... csvt hehe
... """
>>> r = r'^csvt'
>>> re.findall(r,s)
[]
>>> re.findall(r,s,re.M)
['csvt', 'csvt']



X    正则表达式忽略多行中的行符
>>> tel = r"""
... \d{3,4}
... -?
... \d{8}
... """
>>> re.findall(tel,'010-12345678')
[]
>>> re.findall(tel,'010-12345678',re.X)
['010-12345678']


分组
>>> email = r'\w{3}@\w+(\.com|\.cn)'
>>> re.findall(email,'zzz@csvt.com')    #分组优先返回分组当中的的数据
['.com']


30.爬虫
获取源代码的模块
import urllib
urllib.urlopen(url)

进行图片下载 
urllib.urlretrieve(img,'1.jpg')         #下载图片并起名是1.jpg
urllib.request.urlretrieve(img,'1.jpg')    #下载图片并起名是1.jpg (python3)

定义正则，如果内容有双引号，外面则用单引号;特殊字符用\转义;需要使用?进行最小匹配


  30.py (python2)
#!/usr/bin/python
import re
import urllib

def getHtml(url):
    page = urllib.urlopen(url)
    html = page.read()
    return html

def getImg(html):
    res = r'middleURL\"\:\"(.*?\.jpg)\"'
    res_c = re.compile(res)
    imglist = re.findall(res_c,html)
    x = 1
    for img in imglist:
        urllib.urlretrieve(img,'%d.jpg' % x)                      #根据图片地址进行下载
        x+=1

url='https://image.baidu.com/search/index?tn=baiduimage&ipn=r&ct=201326592&cl=2&lm=-1&st=-1&fm=index&fr=&hs=0&xthttps=111111&sf=1&fmq=&pv=&ic=0&nc=1&z=&se=1&showtab=0&fb=0&width=&height=&face=0&istype=2&ie=utf-8&word=minieye&oq=minieye&rsp=-1'
html = getHtml(url)
getImg(html)

      30.py (python3)
import urllib.request
import re

def Open(url):
    page = urllib.request.urlopen(url)
    html = page.read()
    #bytes解码成string
    return html.decode('UTF-8')

def Down(html):
    img = re.compile(r'https://.+?\.jpg')
    list1 = re.findall(img,html)
    print(list1)
    x = 1
    for i in list1:
        urllib.request.urlretrieve(i,'%s.jpg' % x)
        #下面这句是将文件下载到指定的目录下
        #urllib.request.urlretrieve(img,'E:\\python\\38\\30\\%s.jpg' % x)
        x += 1

url = 'https://image.baidu.com/search/index?tn=baiduimage&ipn=r&ct=201326592&cl=2&lm=-1&st=-1&fm=index&fr=&hs=0&xthttps=111111&sf=1&fmq=&pv=&ic=0&nc=1&z=&se=1&showtab=0&fb=0&width=&height=&face=0&istype=2&ie=utf-8&word=minieye&oq=minieye&rsp=-1'
html = Open(url)
Down(html)


31.深拷贝和浅拷贝
python对内存的利用
浅拷贝是对引用的拷贝（只拷贝父对象）
深拷贝是对对象资源的拷贝
import copy


#多个变量对一个内存对象的引用，一个变量修改，其他的都修改，且变量的内存id是一致的
>>> a = [1,2,3,'a','b','c']
>>> b= a
>>> b
[1, 2, 3, 'a', 'b', 'c']
>>> a.append('d')
>>> a
[1, 2, 3, 'a', 'b', 'c', 'd']
>>> b
[1, 2, 3, 'a', 'b', 'c', 'd']
>>> b.append(4)
>>> a
[1, 2, 3, 'a', 'b', 'c', 'd', 4]
>>> b
[1, 2, 3, 'a', 'b', 'c', 'd', 4]

#对变量的copy，是在内存上重新开辟一个空间，变量改变，变量的copy不变
>>> import copy
>>> a = [1,2,3,['a','b','c']]
>>> b=a
>>> c = copy.copy(a)
>>> 
>>> id(a)
139907157826304
>>> id(b)
139907157826304
>>> id(c)                            #变量的copy的id是不一样的
139907157426472
>>> id(a[0])                         #浅拷贝的子元素的id不变，只是对父对象进行了copy
13816152
>>> id(c[0])
13816152

>>> a.append('d')                    #父对象进行了拷贝，修改父对象，浅拷贝的对应不会修改       
>>> a
[1, 2, 3, ['a', 'b', 'c'], 'd']
>>> b
[1, 2, 3, ['a', 'b', 'c'], 'd']
>>> c
[1, 2, 3, ['a', 'b', 'c']]


>>> id(a[3])
139907157826232
>>> id(c[3])
139907157826232
>>> a[3].append('d')                #子对象没有进行拷贝，修改子对象（数字、字符串、元组不能修改，列表可以修改,），浅拷贝的对应也会修改
>>> a
[1, 2, 3, ['a', 'b', 'c', 'd'], 'd']
>>> c
[1, 2, 3, ['a', 'b', 'c', 'd']]




#  深拷贝，父对象和子对象都进行了copy
>>> d=copy.deepcopy(a)
>>> a
[1, 2, 3, ['a', 'b', 'c', 'd'], 'd']
>>> d
[1, 2, 3, ['a', 'b', 'c', 'd'], 'd']
>>> id(a)
139907157826304
>>> id(d)                 #父对象进行了拷贝
139907157426256
>>> id(a[3])
139907157826232
>>> id(d[3])              #子对象进行了拷贝
139907157826088
>>> id(a[0])            
13816152
>>> id(c[0])              #子对象中不可变元素不能拷贝   
13816152


32.文件之文件读写
python进行文件读写的函数是open或file类
mode:
r   只读
r+  读写
w   写入，先删除原文件，再重新写入，如果文件没有则创建
w+  读写，先删除原文件，再重新写入，如果文件没有则创建
a   写入，在文件末尾增加新的内容，文件不存在，创建
a+  读写，在文件末尾增加新的内容，文件不存在，创建

>>> fi = open('test.txt')
>>> fi
<open file 'test.txt', mode 'r' at 0x7f49f908d540>
>>> fi.read()                #读文件
'123\n'
>>> fi.close()               #关闭文件
或
>>> f1 = file('test.txt')
>>> f1
<open file 'test.txt', mode 'r' at 0x7f49f908d5d0>
>>> f1.read()
'123\n'
>>> f1.close()



>>> f1=open('test.txt','w')
>>> f1.write('lucy')            #写文件到缓存
>>> f1.close()                  #只有关闭后，才能看到文件的写入


>>> f1 = open('test.txt','r+')
>>> f1.read()                   #读取后将指针指到最后，没有read操作，指针在开始位置
'lucy'
>>> f1.write('lili')
>>> f1.close()                  #关闭后查看，显示lucylili

>>> f1 = open('test.txt','r+')
>>> f1.write('tom')
>>> f1.close()                  #关闭后查看，显示tomy（没有read操作，指针在开始位置进行写操作并覆盖原来的）



33.文件之文件对象的方法
FileObject.read()    返回字符串

test.txt  ：
lucy
tom
lili

readline     每次读取一行
>>> f1 = open('test.txt')
>>> f1.readline()
'lucy\n'
>>> f1.readline()
'tom\n'
>>> f1.readline()
'lili\n'
>>> f1.readline()   #  超出范围返回空
''
>>> 


>>> for i in open('test.txt'):
...     print i
... 
lucy

tom

lili


readlines     读取所有原因，但以列表形式返回每行数据
>>> f1 = open('test.txt')
>>> f1.readlines()
['lucy\n', 'tom\n', 'lili\n']


next          返回当前行，并将文件指针到下一行
>>> f1 = open('test.txt')
>>> f1.next()
'lucy\n'
>>> f1.next()
'tom\n'
>>> f1.next()
'lili\n'
>>> f1.next()         #超出范围，会停止报错，这是比readline优化的地方
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
StopIteration


write
writelines(List)  多行写，效率比write高，少量写可以用 write

>>> l = ['one\n','two\n','three\n']
>>> f1 = open('test.txt','a')
>>> f1.write(l)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: expected a string or other character buffer object
>>> f1.writelines(l)
>>> f1.close()

seek(偏移量，选项）
--选项0，表示将文件指针指向从文件头部到偏移量字节处
--选项1，表示文件指针指向从文件当前位置，向后移动偏移量字节
--选项2，表示文件指针指向文件尾部，向前移动偏移量字节
seek(0,0)  文件指针移到开头
seek(0,2)  文件指针移到结尾

f1.seek(0,0)

flush()   提交更新


a.t  :
hello world
hello hello world


统计a.t文件中hello的数量
find.py
#!/usr/bin/python
import re

res = r'hello'
f = open('a.t','r')
list1 = re.findall(res,f.read())
print len(list1)
f.close()


把a.t中的hello替换为csvt,并保存结果到文件a2.t中
tihuan.py :
#!/usr/bin/python
import re

f1 = open('a.t','r')
s =  f1.read()
res = r'hello'
s_new = re.sub(res,'csvt',s)
f1.close()
f2 = open('a2.t','w')
f2.write(s_new)
f2.close()
或
#!/usr/bin/python
import re

f1 = open('a.t','r')
f2 = open('a2.t','w')
s =  f1.readlines()
for x in s:
    f2.write(x.replace('hello','csvt'))
f1.close()
f2.close()


把a.t中的hello替换为csvt,并保存结果到文件a.t中
tihuan1.py :
#!/usr/bin/python
import re

f1 = open('a.t','r')
s =  f1.read()
res = r'hello'
s_new = re.sub(res,'csvt',s)
f1.close()
f1 = open('a.t','w')
f1.write(s_new)
f1.close()


34.文件之OS模块
目录操作就是通过python来实现目录的创建，修改和遍历等功能

import os
目录操作需要调用os模块，比如os.mkdir('/root/csct')

>>> import os
>>> os.mkdir('test')   #创建目录

创建多级目录  mkdir -p a/b/c
>>> os.makedirs('a/b/c')  
# tree a
a
└── b
    └── c

删除目录
os.rmdir('test')

删除多级目录a
os.removedirs('a/b/c')

删除文件
os.remove()


显示当前目录下文件（仅返回第一层文件或文件夹）
os.listdir（'.')
显示根目录下文件
os.listdir（'/')


显示当前目录路径
os.getcwd()

切换目录
os.chdir('/')
>>> os.chdir('/')
>>> os.listdir('.')
['sys', 'media', 'dev', 'sbin', 'lost+found', 'mnt', 'home', 'run', 'tmp', 'snap', 'opt', 'var', 'bin', 'usr', 'lib64', 'lib', 'srv', 'etc', 'initrd.img', 'root', 'vmlinuz', 'proc', 'boot']
>>> os.getcwd()
'/'

35.目录遍历之杀毒软件

os.path.join(path1,path2)   路径合并
os.path.isdir(path)         判断是否是目录
os.path.isfile(file)         判断是否是文件



返回指定目录下所有文件的绝对路径
#!/usr/bin/python
import os
paths = []
def path(name):
    for x in os.listdir(name):
        path2 = os.path.join(name,x)               #path2 = name + '/' +x    这个方法也行
        if os.path.isdir(path2):                   #使用递归的方法
            path(path2)
        else:
            paths.append(path2)
    return paths

print path('/root/python/file/testdir')


os.walk(path) 

>>> os.walk('/root/python/file/testdir')      #生成生成器
<generator object walk at 0x7f04375e77d0>   
>>> g = os.walk('/root/python/file/testdir')
>>> g.next()              #注意python3中执行next(g)
('/root/python/file/testdir', ['jpg'], ['f1', 'f2', 'f3'])    #返回元组，分别返回当前路径、当前目录下路径、当前目录下文件
>>> g.next()
('/root/python/file/testdir/jpg', [], ['getjpg.py'])
>>> g.next()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
StopIteration

>>> g = os.walk('/root/python/file/testdir')
>>> for path,d,filelist in g:
...     for filename in filelist:
...         os.path.join(path,filename)
... 
'/root/python/file/testdir/f1'
'/root/python/file/testdir/f2'
'/root/python/file/testdir/f3'
'/root/python/file/testdir/jpg/getjpg.py'



遍历目录，将目录下文件名字包含f的文件删除
# tree testdir
testdir
├── f1
├── f2
├── f3
└── jpg
    ├── f22
    └── getjpg.py


递归的方法：
#!/usr/bin/python
import os
paths = []
def path(name):
    for x in os.listdir(name):
        path2 = os.path.join(name,x)
        if os.path.isdir(path2):
            path(path2)
        else:
            if 'f' in x:
                os.remove(path2)
            paths.append(path2)
    return paths

print path('/root/python/file/testdir')



walk的方法：
>>> g = os.walk('/root/python/file/testdir')
>>> 
>>> for path,d,filelist in g:
...     for filename in filelist:
...         allfile = os.path.join(path,filename)
...         if 'f' in filename:
...             os.remove(allfile)




将目录下文件内容包含123的文件删除
#!/usr/bin/python
import os
paths = []
def path(name):
    for x in os.listdir(name):
        path2 = os.path.join(name,x)
        if os.path.isdir(path2):
            path(path2)
        else:
            f1 = open(path2,'r')
            if '123' in f1.read():
                os.remove(path2)
            paths.append(path2)
            f1.close()
    return paths

print path('/root/python/file/testdir')


36.异常处理
异常抛出机制，为程序开发人员提供一种发现错误，进行恢复处理


try:
    f = open('abc.txt')
    print hello
except IOError as msg:                        #根据实际报错，捕获异常
    print 'IOError'
except NameError,msg:                      #可以捕获多个异常
    pass
finally:
     f.close()                             #不管是否出错，finally下的内容都会执行,一般是文件关闭，释放锁，数据库链接返回给连接池。finally下也可以增加if\try等复杂语句

raise抛出异常，可以自己定义错误信息，但一定要是存在的错误类型
x = 'hello'
if x == 'hello':
    raise Error("x is equal hello!!!")

Traceback (most recent call last):
  File "36.py", line 18, in <module>
    raise NameError("x is equal hello!!!")
NameError: x is equal hello!!!

常见的Python异常
IOError                输入输出异常，基本是无法打开文件
ImportError            无法引入模块或包
IndentationError       语法错误，代码没有正确对齐
IndexError             下标超出索引编辑
KeyError               键值在字典中不存在
NameError              变量没有定义
SyntaxError            代码逻辑语法错误，不能执行
ValueError             传入一个不被期望的值  




except NoSuchElementException as e:                #这个e是异常类NoSuchElementException的一个实例
    print (e)

37.MySQLdb

http://www.linuxidc.com/Linux/2016-07/133128.htm  安装mysql
在mysql界面创建数据，在python进行增删改查

登陆mysql(ubuntu,密码root)
mysql -u root -p
mysql> show databases;        #查看当前数据库
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
4 rows in set (0.00 sec)

mysql> use mysql;              #更改数据库
mysql> show tables;            #查看当前数据库下表

mysql> desc python;            #查看表结构

mysql> insert into python values(1,'lucy',21);            #插入数据

mysql> insert into python values(2,'lili',22),(3,'tom',23); 


mysql> create table python(id INT NOT NULL,name VARCHAR(40) NOT NULL,age INT NOT NULL);   #创建表

mysql> create database view;    创建数据库


            
 
  
安装MySQL-python   http://www.jb51.net/article/87364.htm  
(注:python3不支持MySQLdb，用mysql.connector替代)

python3连接数据库如下：
import mysql.connector
conn = mysql.connector.connect(user='root', password='root',host='127.0.0.1', database='mysql')
cursor = conn.cursor()
#下面这个可以解决 InternalError("Unread result found")问题
cursor = conn.cursor(buffered=True)

python2连接数据库如下:
>>> import MySQLdb
>>> conn = MySQLdb.connect(user='root',passwd='root',host='127.0.0.1')     #连接数据库
>>> cur = conn.cursor()                                                    #需要使用游标操作数据库
>>> conn.select_db('mysql')                                                #更改库
>>> cur.execute("insert into python value('2','lili',20)")                 #增加数据
1L
>>> conn.commit()                                                          #提交生效

>>> sqli = "insert into python value(%s,%s,%s)"                            #格式化增加数据
>>> cur.execute(sqli,(3,'tom',25))
1L

>>> sqlim = "insert into python values(%s,%s,%s)"                          #格式化增加多行
>>> cur.executemany(sqlim,[(4,'jim',23),(5,'lilei',26)])                   #
2L

>>> cur.execute("delete from python where id = 2")                         #删除一行
1L
>>> cur.execute("update  python set name = 'lucy2' where id = 3")          #修改一行


>>> cur.execute("select * from python")                                    #查询数据
4L
>>> cur.fetchone()
(1L, 'lucy', 21L)
>>> cur.fetchone()
(3L, 'lucy2', 25L)

>>> cur.scroll(0,'absolute')                                               #游标移到开头
>>> cur.fetchone()
(1L, 'lucy', 21L)

>>> cur.scroll(0,'absolute')                      
>>> cur.fetchmany(4)                                                       #取出全部4条数据
((1L, 'lucy', 21L), (3L, 'lucy2', 25L), (4L, 'jim', 23L), (5L, 'lilei', 26L))    

>>> cur.fetchmany(cur.execute("select * from python"))                     #一条命令取出全部4条数据
((1L, 'lucy', 21L), (3L, 'lucy2', 25L), (4L, 'jim', 23L), (5L, 'lilei', 26L)) 


cur.close()                                                                #关闭游标
conn.close()                                                               #关闭连接

查看mysql的端口
show global variables like 'port'


删除数据库或数据库表失败(卡死)，使用下面的命令查看什么进程阻塞了
mysql> show full processlist;
kill + id杀死对应的进程

38.面向对象之类和对象
类和对象是面向对象的重要概念
类是事物的抽象，对象是类的一个实例


>>> class Test:
...     first = 123
...     second = 456
...     def f(self):                          #类中函数最少一个形参self,不需要传值，其实是传的是类自身
...         return 'test'
... 

>>> milo = Test()                             #定义对象
>>> milo.f()
'test'
>>> milo.first
123


>>>help(list)                                 #列表也是一个类
Help on class list in module __builtin__:

class list(object)
 |  list() -> new empty list
 |  list(iterable) -> new list initialized from iterable's items


Add:
1. try except else
try：执行可能会出错的试探性语句，即这里面的语句是可以导致致命性错误使得程序无法继续执行下去
except：如果try里面的语句无法正确执行，那么就执行except里面的语句，这里面可以是错误信息或者其他的可执行语句
else：如果try里面的语句可以正常执行，那么就执行else里面的语句（相当于程序没有碰到致命性错误）

2.如何为assert断言语句添加异常参数
assert expression [, arguments]
assert (add == 5),"Integer addition result error!"

3.概括的讲，装饰器的作用就是为已经存在的对象添加额外的功能。
它可以让其他函数在不需要做任何代码变动的前提下增加额外功能，装饰器的返回值也是一个函数对象。

4.在python下，获取当前执行主脚本的方法有两个：sys.argv[0]和__file__
获取主文件路径的最佳方法是用sys.argv[0]，内建变量__file__ 也可用来获得模块所在的路径。

5.os.path.dirname(path) 
返回path所在的目录或文件的上一层目录。

6.S.join()
用于将序列中的元素以指定的字符连接生成一个新的字符串

str = "-";
seq = ("a", "b", "c"); # 字符串序列
print str.join( seq );
以上实例输出结果如下：
a-b-c

7.json.dumps()和json.loads()是json格式处理函数（可以这么理解，json是字符串）
import json
　　(1)json.dumps()函数是将一个Python数据类型列表进行json格式的编码（可以这么理解，json.dumps()函数是将字典转化为字符串）
　　(2)json.loads()函数是将json格式数据转换为字典（可以这么理解，json.loads()函数是将字符串转化为字典）
       (3)json.dump()函数将字典转换成json并写入json文件
>>> d = dict(name='Bob',age=20,score=88)
>>> f = open('dump.json','w')
>>> json.dump(d,f)
>>> f.close()
       (4)json.load()函数从json文件中读取字符串并反序列化成字典
>>> f = open('dump.json','r')
>>> json.load(f) 
{'name': 'Bob', 'age': 20, 'score': 88}
      

8. 命令行神器 Click
init_case.py

__author__ = 'muhongyun <muhongyun@minieye.cc>'
__version__ = '0.1.0'
__progname__ = 'init_case'

@click.command(name='handle-case')
@click.help_option('-h', '--help')
#查看版本
@click.version_option(__version__, '-v', '--version', prog_name=__progname__, message='%(prog)s version %(version)s')
@click.option('-p', '--para-file', type=str, default='', help='指定脚本参数文件 (default: none)')
@click.option('-c', '--case-path', type=str, default='', help='直接cli输入case路径')
def cli(**options):
    #打印options字典
    print('options:', options)
    ...
if __name__ == '__main__':
    cli()

#查看版本
PS E:\python\3.6\click> python3 init_case.py -v
init_case version 0.1.0
#打印默认字典结果，注意特例para-file会自动转成para_file
options: {'para_file': '', 'case_path': ''}



Click 的使用大致有两个步骤：
使用 @click.command()装饰一个函数，使之成为命令行接口； 
使用 @click.option()等装饰函数，为其添加命令行选项等,为函数提供参数。 
它的一种典型使用形式如下：

import click

@click.command()
@click.option('--count', default=1, help='Number of greetings.')
@click.option('--name', prompt='Your name', help='The person to greet.')
def hello(count, name):
    """Simple program that greets NAME for a total of COUNT times."""
    for x in range(count):
        click.echo('Hello %s!' % name)

if __name__ == '__main__':
    hello()

$ python hello.py --help   # click 帮我们自动生成了 `--help` 用法
Usage: hello.py [OPTIONS]

  Simple program that greets NAME for a total of COUNT times.

Options:
  --count INTEGER  Number of greetings.
  --name TEXT      The person to greet.
  --help           Show this message and exit.


Argument 参数
Argument 的作用类似 Option，但没有 Option 那么全面的功能。
和 Option 一样，Argument 最基础的应用就是传递一个简单变量值：
import click
@click.command()
@click.argument('filename')
'''
作用与下面的一致
def touch(**arguments):
    print(arguments['count'])
'''
def touch(filename):
    click.echo(filename)
if __name__ == '__main__':
    touch()
    
python do_click.py name1
执行结果
name1



9.
self.xxx是全局的，xxx是局部的对于该方法有效
python中类方法的属性需要加self，也就是self.xxx，这个是方法的属性！
类方法的变量不加self，也就是xxx，这个是方法的局部变量，不能被调用，只能在该方法内部使用！

10、执行脚本时指定参数  python3 1.py /home/1.json
1.py 
import os
import sys

def cli(argv):
    '''
    '''
    print(argv)
    if len(argv) != 2:
        print("EN: need parameter file")
    file = argv[1]
    if not os.path.exists(file):
        print("EN: not exists parameter file")
    fp = open(file, 'r+')
    para_content = json.loads(fp.read())
    fp.close()
    print("Are you ok:")
    print(para_content)
    time.sleep(2)
    unpack_video_log(para_content['video_path'])

if __name__ == '__main__':
    cli(sys.argv)

使用argparse指定参数
#do_argparse.py
import argparse

def run(ip, origin_save, result_save, path):
    pass
if __name__ == "__main__":
    #crl:添加参数解析
    parser = argparse.ArgumentParser()
    #crl:z增加参数
    parser.add_argument("--ip", help="ip address",type=str)
    parser.add_argument("--origin", help="是否保存原始图片，默认不保存",type=str)
    parser.add_argument("--result", help="是否保存处理后图片，默认不保存",type=str)
    parser.add_argument("--path", help="保存图片的路径",type=str)
    args = parser.parse_args()
    run(args.ip, args.origin, args.result, args.path)

执行脚本 
python3 do_argparse.py --ip 192.168.1.251 --origin 1 --result 1 --path '/home/pc_view/image/'



11、类中方法调用该类中的其他方法,需要加self
class Student(object):
    def fun1(self):
        pass
    def fun2(self):
        self.fun1()
stu = Student()
stu.fun2()

12、slice() 函数
slice() 函数实现切片对象，主要用在切片操作函数里的参数传递

slice 语法：
class slice(stop)
class slice(start, stop[, step])
参数说明：
start -- 起始位置
stop -- 结束位置
step -- 间距

>>>myslice = slice(5)    # 设置截取5个元素的切片
>>> myslice
slice(None, 5, None)
>>> arr = range(10)
>>> arr
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
>>> arr[myslice]         # 截取 5 个元素
[0, 1, 2, 3, 4]
>>>

13、reduce在python3中从内建函数移除了，直接使用会报错，放入了functools模块
>>> reduce(lambda x,y:x+y,[1,2,3])
NameError: name 'reduce' is not defined

from functools import reduce


14、小数转成百分百输出
rate = 0.1
res = format(rate, '.0%')
    # res == '10%'

15、画柱状图   
参考 https://blog.csdn.net/jenyzhang/article/details/52047557
matplotlib.pyplot.bar(left, height, width=0.8, bottom=None, hold=None, data=None, **kwargs)

参数说明：
left: 每一个柱形左侧的X坐标(这个值实际显示柱形的中间X坐标)
height:每一个柱形的高度
width: 柱形之间的宽度
bottom: 柱形的Y坐标
color: 柱形的颜色

示例：
#import numpy as np    
#import matplotlib.mlab as mlab    
import matplotlib.pyplot as plt    
  
X=[0,1,2,3,4,5]  
Y=[222,42,455,664,454,334]    
#fig = plt.figure()  
plt.bar(X,Y,0.4,color="green")  
plt.xlabel("X-axis")  
plt.ylabel("Y-axis")  
plt.title("bar chart")  
plt.show()
  
问题：
(1)linux上保存柱状图后时报错 
#执行显示后，再执行plt.savefig保存的图片是空白图片。
plt.show()
#注意想要保存柱状图，在linux必须保存成.png文件，否则报错    
plt.savefig("barChart.jpg")

(2)柱状图显示中文字体乱码

a.
Python版本及matplotlib配置文件位置查询

[hadoop@p168 ~]$ python
>>> import matplotlib

>>> print matplotlib.matplotlib_fname()

/home/hadoop/.pyenv/versions/2.7.10/lib/python2.7/site-packages/matplotlib/mpl-data/matplotlibrc
b.
首先将windwos中fonts目录下的simhei.ttf拷贝到/home/hadoop/.pyenv/versions/2.7.10/lib/python2.7/site-packages/matplotlib/mpl-data/fonts/ttf
(文件路径参考a，根据实际情况修改)目录中，
然后删除~/.cache/matplotlib的缓冲目录(用户目录下)


c.
第三在代码中动态设置参数：


import matplotlib.pyplot as plt 

plt.rcParams['font.sans-serif'] = ['SimHei']


plt.xlabel('时间差')  #   

16、str.strip()
方法用于移除字符串头尾指定的字符（默认为空格）

17、python写utf8文件
import codecs
f = codecs.open("demo_1.html",'w',encoding='utf8')
f.write(message)
f.close()

18.subprocess.call
子进程调用
subprocess.call()：执行命令，并返回执行状态，其中shell参数为False时，命令需要通过列表的方式传入，当shell为True时，可直接传入命令
示例如下：
>>> a = subprocess.call(['df','-hT'],shell=False)
Filesystem    Type    Size  Used Avail Use% Mounted on
/dev/sda2     ext4     94G   64G   26G  72% /
tmpfs        tmpfs    2.8G     0  2.8G   0% /dev/shm
/dev/sda1     ext4    976M   56M  853M   7% /boot

>>> a = subprocess.call('df -hT',shell=True)
Filesystem    Type    Size  Used Avail Use% Mounted on
/dev/sda2     ext4     94G   64G   26G  72% /
tmpfs        tmpfs    2.8G     0  2.8G   0% /dev/shm
/dev/sda1     ext4    976M   56M  853M   7% /boot

#执行命令，标准输出写入out.log,标准错误写进标准输出同一个文件
subprocess.call('ping -n 2 www.baidu.com',shell=True,stdout='out.log',stderr=subprocess.STDOUT)
subprocess.call('ping -n 2 www.baidu.com > out.log 2>&1',shell=True)

19.os.path.basename、os.path.splitext、os.path.split
os.path.basename(path)返回最后的文件名  os.path.splitext分离文件名和文件扩展名
os.path.split可以把一个路径拆分为两部分，后一部分总是最后级别的目录或文件名

20.二分搜索
import bisect 

L = [1,3,3,6,8,12,15]    #注意L中的值是有序的
x = 3  
  
x_insert_point = bisect.bisect_left(L,x)　　#在L中查找x，x存在时返回x左侧的位置，x不存在返回应该插入的位置..这是3存在于列表中，返回左侧位置１  
print x_insert_point  
  
x_insert_point = bisect.bisect_right(L,x)  #在L中查找x，x存在时返回x右侧的位置，x不存在返回应该插入的位置..这是3存在于列表中，返回右侧位置３  



21.默认等级是WARNING，这意味着仅仅这个等级及以上的才会反馈信息
级别             数字值
CRITICAL    50
ERROR       40
WARNING 30
INFO          20
DEBUG      10
NOTSET     0

import logging
logging.debug('This is debug log')
logging.info('This is info log')
logging.warning('This is warning log')
logging.error('This is error log')
logging.critical('This is critical log')

输出
======================= RESTART: E:\python\100\test.py =======================
WARNING:root:This is warning log
ERROR:root:This is error log
CRITICAL:root:This is critical log


配置日志器的日志级别，logging.basicConfig只能是第一次配置生效，下次再配置时，需要先退出python exit()
logging.basicConfig(level=logging.DEBUG)
上面的输出:
======================= RESTART: E:\python\100\test.py =======================
DEBUG:root:This is debug log
INFO:root:This is info log
WARNING:root:This is warning log
ERROR:root:This is error log
CRITICAL:root:This is critical log

配置日志输出到文件中
import logging
LOG_FORMAT = '%(asctime)s - %(levelname)s - %(message)s'
logging.basicConfig(filename='my.log',level=logging.DEBUG,format = LOG_FORMAT)
logging.debug('This is debug log')
logging.info('This is info log')
logging.warning('This is warning log')
logging.error('This is error log')
logging.critical('This is critical log')

此时会发现控制台中已经没有输出日志内容了，但是在python代码文件的相同目录下会生成一个名为'my.log'的日志文件，该文件中的内容为：
2018-07-20 12:20:04,638 - DEBUG - This is debug log
2018-07-20 12:20:04,639 - INFO - This is info log
2018-07-20 12:20:04,639 - WARNING - This is warning log
2018-07-20 12:20:04,639 - ERROR - This is error log
2018-07-20 12:20:04,640 - CRITICAL - This is critical log


22.insert() 函数用于将指定对象插入列表的指定位置。
list.insert(index, obj)

23.找到字符串中指定字符串的位置
s1 = 'abcdef'
s2 = 'bcd'
print(s1.find(s2))

24.如何在IDLE中进行批量缩进
Ctrl + [  回退
Ctrl + ]  前进

25.计算字符串中子串出现的次数
str1.count(str2)

26. r/R:非转义的原始字符串 
与普通字符相比，其他相对特殊的字符，其中可能包含转义字符，即那些，反斜杠加上对应字母，表示对应的特殊含义的，比如最常见的”\n”表示换行，”\t”表示Tab等。
而如果是以r开头，那么说明后面的字符，都是普通的字符了，即如果是“\n”那么表示一个反斜杠字符，一个字母n，而不是表示换行了。 
>>> str1 = r'12\n345'
>>> str2 = '12\n345'
>>> print(str1)
12\n345
>>> print(str2)
12
345

27.python2中的cmp被python3中的operator替代
import operator
operator.eq(1,1)  等于

operator.lt     小于
operator.le    小于等于
operator.eq   等于
operator.ne   不等于
operator.gt    大于
operator.ge   大于等于

28.如果你想要为一个定义在函数外的变量赋值，那么你就得告诉Python这个变量名不是局部的，而是 全局 的。我们使用global语句完成这一功能。没有global语句，是不可能为
定义在函数外的变量赋值的。
>>> y = 3
>>> def fun1():
...     global y
...     y = 5
...
>>> fun1()
>>> y
5

29.在序列中随机取n个数据
>>> from random import sample
>>> sample('abcde',2)
['c', 'd']

30.time 模块
>>> from time import *
>>> time1 = time()       #获取当前秒数时间
>>> time1
1534130206.3175268
>>> localtime(time1)    #将秒数转换成时间元组
time.struct_time(tm_year=2018, tm_mon=8, tm_mday=13, tm_hour=11, tm_min=16, tm_sec=46, tm_wday=0, tm_yday=225, tm_isdst=0)
>>> asctime(localtime(time1))   #将时间元组转换成字符串
'Mon Aug 13 11:16:46 2018'
>>> mktime(localtime(time1))   #将时间元组转换成秒数
1534130206.0

>>> ctime()    #获取当前字符串时间，或者使用asctime()
'Fri Aug 17 14:22:00 2018'
>>> localtime()  #获取时间元组
time.struct_time(tm_year=2018, tm_mon=11, tm_mday=19, tm_hour=17, tm_min=8, tm_sec=4, tm_wday=0, tm_yday=323, tm_isdst=0)
>>> time()         #获取时间秒数
1542618793.8715754



31.打印具体的错误信息
try:
    print  aa
except  NameError as msg:
    print  msg

32. map与reduce的使用
#reduce把一个函数作用在一个序列上，reduce把结果与序列的下一个元素做累计计算
>>> reduce(lambda a,b:a+b,[3,4,5])
12

#map将传入的函数依次作用到序列的每个元素，结果是惰性元素(lambda参数个数与序列个数一致)
>>> list1 = list(map(lambda a,b:a*b,[1,2,3],[4,5,6]))
>>> list1
[4, 10, 18]

>>> list1 = list(map(lambda a:a*a,[1,2,3]))
>>> list1
[1, 4, 9]

33.os.rename() 方法用于重命名文件或目录，从 src 到 dst,如果dst是一个存在的目录, 将抛出OSError。
os.rename(src, dst)

src -- 要修改的目录名
dst -- 修改后的目录名

34.#从环境变量中取字符串，获取环境变量的值
>>> os.getenv("TMP")
'C:\\Users\\ThinkPad\\AppData\\Local\\Temp'

35.字符串格式化
>>> '[{}]'.format('tmp')
'[tmp]'

38.返回文件大小
os.path.getsize(filename)

39.strftime 显示当前时间
>>> from time import strftime
>>> strftime("%Y-%m-%d_%H:%M:%S")
'2018-08-22_18:17:48'

40.os.system来执行系统命令
可以使用如下方法：
import os
print os.system('ping www.baidu.com')
输出的结果是：
64 bytes from 223.26.58.21: icmp_seq=0 ttl=245 time=36.798 ms
64 bytes from 223.26.58.21: icmp_seq=1 ttl=244 time=37.561 ms

41. os.stat() 方法用于在给定的路径上执行一个系统 stat 的调用

    返回值
    stat 结构:

    st_mode: inode 保护模式
    st_ino: inode 节点号。
    st_dev: inode 驻留的设备。
    st_nlink: inode 的链接数。
    st_uid: 所有者的用户ID。
    st_gid: 所有者的组ID。
    st_size: 普通文件以字节为单位的大小；包含等待某些特殊文件的数据。
    st_atime: 上次访问的时间。
    st_mtime: 最后一次修改的时间。
    st_ctime: 由操作系统报告的"ctime"。在某些系统上（如Unix）是最新的元数据更改的时间，在其它系统上（如Windows）是创建时间（详细信息参见平台的文档）。

    os.stat().st_mtime

42. eval() 函数用来执行一个字符串表达式，并返回表达式的值。
>>>x = 7
>>> eval( '3 * x' )
21
>>> eval('pow(2,2)')
4
>>> eval('2 + 2')
4
>>> n=81
>>> eval("n + 4")
85

43.github账号https://github.com
chenronglei/Root_123

44.yield
函数中用yield替换return,就成了生成器。不会立即计算，使用next生成器后才开始计算

优点:延迟计算，少占用内存

45.python代码转成exe
https://www.jianshu.com/p/64cb9108a7c6

46.所有变量的位操作都是通过强制转换成bool实现的
>>> 5 and 4      # True and True返回最后一个True值
4

>>> 0 or 3 or ''    #False or True or False  第一个True的值
3

47.多线程、多进程区别
a.都是为了完成多任务
b.多进程是独享变量，多线程是共享变量。多线程为了防止变量冲突异常，需要加锁等复杂操作。
c.多进程更稳定。多线程因为共享变量的原因，一个线程退出了，其他线程都可能退出。多进程一个进程推出了，一般不影响其他进程
d.多线程因为GIL全局锁的原因，不能有效的利用CPU的多核。多进程可以有效的使用
e.多进程可以分布式，在多台机器上使用，而多进程只能在一台机器上的CPU上的多核使用

48.获取当前目录的上级目录路径
os.path.abspath(os.path.join(os.getcwd(), ".."))
os.path.abspath(os.path.join(os.getcwd(), "..\.."))  上上级别目录

49.python Windows环境下文件路径问题
Windows下的文件目录路径使用反斜杠“\”来分隔。但是，和大多数语言一样，Python代码里面，反斜杠“\”是转义符，例如“\n”表示回车、“\t”表示制表符等等。这样，
如果继续用windows习惯使用“\”表示文件路径，就会产生歧义。

解决办法
:
采用下面任何一种书写形式均可：


使用斜杠“/”: 
"c:/test.txt"… 
不用反斜杠就没法产生歧义了


将反斜杠符号转义 
"c:\\test.txt" 
因为反斜杠是转义符，所以两个”\\“就表示一个反斜杠符号


使用Python的raw string 
r"c:\test.txt" 


>>> os.getcwd().replace('\','/')
  File "<stdin>", line 1
    os.getcwd().replace('\','/')
                               ^
SyntaxError: EOL while scanning string literal

将反斜杠替换成斜杆
>>> os.getcwd().replace('\\','/')
'E:/python/3.6/11/mztestpro'

50. __init__.py的作用
a.将文件夹当成包
b.
    有这样一个foo包：
foo/
    __init__.py
    foofactories.py
    tallFoos.py
    shortfoos.py
    mediumfoos.py
    santaslittlehelperfoo.py
    superawsomefoo.py
    anotherfoo.py

在init脚本里这样写：
__all__ = ['foofactories', 'tallFoos', 'shortfoos', 'medumfoos',
           'santaslittlehelperfoo', 'superawsomefoo', 'anotherfoo']
# deprecated to keep older scripts who import this from breaking
from foo.foofactories import fooFactory
from foo.tallfoos import tallFoo
from foo.shortfoos import shortFoo

如此做，则可以在别的脚本里简单方便的写：
from foo import fooFactory, tallFoo, shortFoo

简化了代码量。
若 from foo import * ，则导入了init里的 __all__ 变量里注册的所有模块（不推荐）

51.主程序调用模块后，模块里再调用模块是以主程序所在目录进行搜索模块的

52.python之字符串格式化(format)          它通过{}和:来代替传统%方式
>>> 'my name is {} ,age {}'.format('hoho',18)
'my name is hoho ,age 18'

53.super
当前类和对象可以作为super函数的参数使用，调用函数返回的对象的任何方法都是调用超类的方法，而不是当前类的方法
在子类的构造函数中引入父类的构造函数中配置（如果子类不重写构造方法，会直接使用父类的构造方法）
class Bird:
    def __init__(self):
        self.hungry = True
    def eat(self):
        if self.hungry:
            print 'Aaaah...'
            self.hungry = False
        else:
            print 'No, thanks!'
            

class SongBird(Bird):
         def __init__(self):
                 #在子类的构造函数中引入父类的构造函数中配置（如果子类不重写构造方法，会直接使用父类的构造方法）
                 super(SongBird,self).__init__()           #另外一种方法是使用Bird.__init__(self)
                 self.sound = 'Squawk!'
         def sing(self):
                 print self.sound
>>> s= SongBird()
>>> s.sing()
Squawk!
>>> s.eat()
Aaaah...
>>> s.eat()
No, thanks!


对于super(B, self).__init__()是这样理解的：super(B, self)首先找到B的父类（就是类A），然后把类B的对象self转换为类A的对象（通过某种方式，一直没有考究是什么方式，惭愧），然后“被转换”的类A对象调用自己的__init__函数。

class EditProfileForm(FlaskForm):
    def __init__(self, original_username, *args, **kwargs):
        #super(EditProfileForm, self)找到EditProfileForm的父类FlaskForm,将EditProfileForm的对象转换为FlaskForm的对象。最后FlaskForm的对象调用自己的__init__函数
        super(EditProfileForm, self).__init__(*args, **kwargs)
        self.original_username = original_username

54.特性（property）、静态方法（staticmethod）、类方法（classmethod）、__str__的用法
Python内置的@property装饰器就是负责把一个方法变成属性调用的
class Student(object):

    @property
    def score(self):
        return self._score

    @score.setter
    def score(self, value):
        if not isinstance(value, int):
            raise ValueError('score must be an integer!')
        if value < 0 or value > 100:
            raise ValueError('score must between 0 ~ 100!')
        self._score = value
把一个getter方法变成属性，只需要加上@property就可以了，此时，@property本身又创建了另一个装饰器@score.setter，负责把一个setter方法变成属性赋值

静态方法和类方法，二者是为类量身定制的，但是实例非要使用，也不会报错.
静态方法类似于类方法，唯一的区别是静态方法不接收类作为第一个参数

静态方法如下:
class Foo:
    @staticmethod #装饰器
    def spam(x,y,z):
        print(x,y,z)
Foo.spam(1,2,3) #调用函数应该有几个参数就传几个参数

类方法如下:
class A:
    x=1
    @classmethod
    def test(cls):
        print(cls,cls.x)

class B(A):
    x=2
B.test()

'''
输出结果:
<class '__main__.B'> 2
'''

55.列表利用set的自动去重功能
li=[1,2,3,4,5,1,2,3]
li=list(set(li))
print(li)

56.mysql插入中文数据报错   sqlalchemy.exc.InternalError: (pymysql.err.InternalError) (1366, "Incorrect string value: '\\xE6\\x88\\x91\\xE7\\xAC\\xAC...'
分析：是mysql数据库的字符集问题

解决方法一:
查看mysql某个数据库的字符集，是安装默认的latin1
mysql> show create database flaskblog;
+-----------+----------------------------------------------------------------------+
| Database  | Create Database                                                      |
+-----------+----------------------------------------------------------------------+
| flaskblog | CREATE DATABASE `flaskblog` /*!40100 DEFAULT CHARACTER SET latin1 */ |
+-----------+----------------------------------------------------------------------+

修改数据库的字符集为utf8(支持中文)
mysql> alter database flaskblog character set 'utf8';
Query OK, 1 row affected (0.00 sec)

再次查看该数据库的字符集
mysql> show create database flaskblog;
+-----------+--------------------------------------------------------------------+
| Database  | Create Database                                                    |
+-----------+--------------------------------------------------------------------+
| flaskblog | CREATE DATABASE `flaskblog` /*!40100 DEFAULT CHARACTER SET utf8 */ |
+-----------+--------------------------------------------------------------------+

之前创建的该库下的表字符集还是latin1
mysql> show create table user;
+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Table | Create Table                                                                                                                                                                                                                                                                                                                                              |
+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| user  | CREATE TABLE `user` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `username` varchar(64) DEFAULT NULL,
  `email` varchar(120) DEFAULT NULL,
  `password_hash` varchar(128) DEFAULT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `ix_user_email` (`email`),
  UNIQUE KEY `ix_user_username` (`username`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=latin1 |

需要单独修改这些表的字符集
mysql> alter table user character set 'utf8';
Query OK, 0 rows affected (0.08 sec)

再次查看该表的字符集已经修改成utf8
mysql> show create table user;
+-------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Table | Create Table                                                                                                                                                                                                                                                                                                                                                                                                           |
+-------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| user  | CREATE TABLE `user` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `username` varchar(64) CHARACTER SET latin1 DEFAULT NULL,
  `email` varchar(120) CHARACTER SET latin1 DEFAULT NULL,
  `password_hash` varchar(128) CHARACTER SET latin1 DEFAULT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `ix_user_email` (`email`),
  UNIQUE KEY `ix_user_username` (`username`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8 |


57.查看文件的编码模式
with open(infile,'rb') as f:
        result = chardet.detect(f.read())
        print('result:',result)
58.extend、append
extend与append方法的相似之处在于都是将新接收到参数放置到已有列表的后面。而extend方法只能接收list，且把这个list中的每个元素添加到原list中。

>>> A = ['q', 'w', 'e', 'r']
>>> A.extend(['t', 'y'])
>>> A
['q', 'w', 'e', 'r', 't', 'y']
>>>len(A)

>>> B = ['q', 'w', 'e', 'r']
>>> B.append(['t', 'y'])
>>> B
['q', 'w', 'e', 'r', ['t', 'y']]
>>>len(B)

59.解决flask db migrate 检测不到db.string() 长度变化
修改migrations下的env.py 添加参数compare_type = True

context.configure(connection=connection,

     target_metadata=target_metadata,

     process_revision_directives=process_revision_directives,

     compare_type = True,   #compare_type默认为False,不检测数据变化

     **current_app.extensions['migrate'].configure_args)


再执行migrate 命令和upgrade命令就可以生效了

60.sys.path属性。
他是一个list.默然情况下python导入文件或者模块的话，他会先在sys.path里找模块的路径。如果没有的话，程序就会报错。
所以我们一般自己写程序的话。最好把自己的模块路径给加到当前模块扫描的路径里,eg: sys.path.append('你的模块的名称'),这样程序就不会
因为找不到模块而报错








 







