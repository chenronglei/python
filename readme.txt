selenium  https://github.com/chenronglei/SELENIUM  chenronglei@163.com/608806crl

pip��װ̫�������������淽�������
pip install XXX -i https://pypi.tuna.tsinghua.edu.cn/simple


linuxϵͳ���߰�װ apt install tree



�й�Python������Ƶ�̳̣�ȫ38����

01.�߽�Python
1.Python����
a.����ѧ  b.������&������  c.�������  d.�߼����ԣ����迼�ǹ����ڴ�  e.����չ�Լ���Ƕ��ʽ  d.��Դ�����   f.����ֲ��   g.�ḻ�Ŀ�

02. ��ʼ��̰�
����ģʽ���ı�ģʽ

ִ�нű� 
a.   python 1.py  
b    ./1.py        #���븳���ִ��Ȩ��   +  python�ű�·��  #! /usr/bin/python  ��python3ʹ������ #! /usr/bin/python3.5 ��

    ����:��windowsϵͳ��д��python�ű�����linux�¸���Ȩ��chmod +x xxx.py �Ժ�ִ��./xxx.py������ʾ��bash: /usr/bin/autocrorder: /usr/bin/python^M: bad 
interpreter: No such file or directory
    ���������ǲ�ͬϵͳ�����ʽ����ģ���windowsϵͳ�б༭��.sh .py�ļ������в��ɼ��ַ���������Linuxϵͳ��ִ�лᱨ�����쳣��Ϣ��һ������Ϊwindows�н�β��
linux�н�β��ʶ��ͬ��ɵġ�
   ���:��Linux��ת����
        ��һ�ַ���:
        a.������������鿴�ļ���ʽ
           :set ff �� :set fileformat
        b.�������������޸��ļ���ʽ
            :set ff=unix �� :set fileformat=unix
        �ڶ��ַ���:
            dos2unix xxx.py


SyntaxError  �﷨����
exit() �˳�����ģʽ

�ļ�����
a,Դ���� .py
1.py

b.�ֽڴ���  .pyc         #Դ�ļ���������.pyc�ļ� 
��Ҫ����ģ��  
import py_compile
py_complie.compile('1.py')
python 2.py                  #���� 1.pyc�ļ�

c. �Ż����� .pyo
python -O -m py_compile 1.py   #���� 1.pyo�ļ�

b,cִ�и��죬��aʹ�÷���

03.����
������������ĸ�����֡��»�����ɣ��������Դ����ֻ����ֿ�ͷ
�����Ǽ�����ڴ��е�һ�����򣬱������ڴ����ݵı�ǩ
NameError ������������û�ж���

�鿴�������ڴ��еĵ�ַ
id(a)

04.����������ʽ��
��ֵ�����   =  +=   -=   *=    /=     %=

���������  + - * /    
 //  ������
 %
 3.0/2    С������
 **     ָ��  

��ϵ�����
<  > <=  >= !=    ==
True
False


�߼������
and
or 
not


�������ȼ����ڸ�ֵ����

��������
a=raw_input()  �ַ���
a=int(raw_input())  ����
a=int(raw_input(��please input num1:��))  ��ʾ����


05.�������ͣ����ֺ��ַ�����
������������ tpye()

����
���Ρ�������(123L)��������(1.0)������(3.14j)

�ַ���
''              ""    """ """
�������ſ��Զ���doc�ĵ���һ�δ����ע�ͣ�����
�����š�˫����û�б������� ע�������е����ţ�����ʹ��˫����
����������е���˫���ţ����Լ�ת���ַ� \
�ַ������п���ʹ�� \n,Ҳ����ʹ����������
main = """tom:
				 i am jack
				 goodbye
			"""
a= 'abcde'
a[0]+a[1]  'ab'
a[1:4]       'bcd'��Ƭ 
a[1:4:2]     'bd'  �ֱ�����ʼֵ������ֵ���������Լ���������
a[-1:-4:-1]   'edc'   ��ʼֵ-1��ʾ���һ��ֵ������-1��ʾ��������ȡֵ

ȡǰ��5��stmp[:5]
ȡ����5��stmp[-5:]
��ǰ�濪ʼȡ���������������stmp[:-2]
�ӵ�1��ȡ����2��stmp[0:2]
��ǰ�濪ʼȡ��������ǰ������stmp[2:]

Ԫ��
�б�
�ֵ� 

06.Ԫ��
�ַ�����Ԫ�顢�б������С���
���е�2����Ҫ��������������������Ƭ������

���еĻ�������
len
+     ����2������
*      �ظ����� str1*5
in     �ж�Ԫ���Ƿ��������� ��c' in str1(�ֵ�ļ�ֵ��in�ж�)
max()
min()
cmp(str1,str2)   �Ƚ������Ƿ���ͬ����ȵ���0��str1>str2,����1   str1<str2,����-1    (��ĸ��������)


�����޸��������ַ�����Ԫ���е�ֵ�����¸�ֵ�����޸ģ�ռ���ڴ�ռ��ѱ䣬������ԭ�ռ��Ͻ����޸ģ�

t=����milo",30,"male')��

��������Ԫ�ص�Ԫ��
t=(1,)

Ԫ���е�Ԫ�ؿ������������ַ������б��

������ֵ
>>> a,b,c=(1,2,3)
>>> a
1
>>> b
2
>>> c
3

07.�б�
�б�Ԫ�ؿ��������֡��ַ�����Ԫ��
�����޸�Ԫ��ֵ

��������Ԫ�ص��б�
t=[1]

listmile=['zou',30,'male']
listmile[0]='lucy'
�޸��б���Ԫ��ֵ���б�洢�ռ䲻��

�б�������Ԫ��
listmile.append("12345578")

�б���ɾ��Ԫ�أ�����Ļ���ɾ����һ�����ֵģ�
listmile.remove("12345578")
del(listmile[0])

ɾ���б�
del(listmile)

IndexError�������󣬳�������ֵ

�鿴����
help(list.append)
q�˳�

�б���һ���࣬��ʵ�������Ƕ���ͨ����������Ժͷ������в���

08.�ֵ�
zip(list1,list2) ��list1,list2��ֵһһ�����Ԫ��

�ֵ��ǿɱ�ģ����ֵ�ļ�����ʹ�ò��ɱ�Ķ���,;�ֵ��������
dic={'name':0,1:1,2:2}
dic['name']=0
dic[1]=2

�����ֵ�
for i in dic:
    print i
	print dic[i]
	
�ֵ�����Ԫ��
dic['tel']='12345678'

�ֵ��޸�Ԫ��
dic['tel']='1234569'

�ֵ�ɾ��Ԫ��
del(dic['tel'])
dic.pop('tel')  ����

�ֵ�ɾ������Ԫ��
dic.clear()

ɾ���ֵ�
del(dic)   #del����ɾ�����б���

dic.get(key,default=None)  ����key��value,��������ڣ�����None
dic1.get('name1','error')      ����key��value,��������ڣ�����'error'

dic1.keys()                  �����ֵ��м������б����ʽ
>>> dic1.items()
[('name', 'lucy'), ('sex', 'female')]

dic1.items()                 ���ؼ�ֵ��Ԫ����б�
>>> dic1.keys()
['name', 'sex']

dic1.values()                �����ֵ���ֵ�����б����ʽ

len(dic1)                       �����ֵ䳤��


09.���̿���(if���)
if expression:
    statement(s)     #ʹ��4���ո��tab��������
	
IndentationError  ��������

�ǿյ�����True
0��None������False

if expression:
    statement(s) 
elif  expression:
    statement(s) 
else:
    statement(s) 
	
10.���̿��ƣ��߼���
and or not
��������Ƕ��

11.���̿���(for���)
�����ַ������б�Ԫ��
for x in "abcd":
    print "lucy",x
	
range(i,j,����ֵ) iΪ��ʼֵ����ѡ�Ļ���0��j����ֵֹ
for x in range(100) 

12.���̿��ƣ��������к��ֵ䣩
s = "abcd"
for  x  in range(len(s)):
    print s[x]

�����ֵ��2�ַ�ʽ��
d = {1:11,2:12}	
for x in dic1:
	print dic1[x]
	
for  k,v in d.items():
	print k,v
	
	
13.���̿��ƣ�ѭ�����ƣ�

d = {1:11,2:12}	
for x in dic1:
	print dic1[x]
	if x == 2:
		pass                        #����׮�������κβ���
	if x == 5:
		exit()                        #������������
else:                                #forѭ������������ִ��else;Ctrl+cǿ����ֹ��break������ִ��else
	print "ending"

#ͣ��һ��	
import time
time.sleep(1)    

14.���̿��ƣ�while)
whileѭ����Ϊ��һֱִ��

x= ""
while x != 'q':                           #���벻Ϊqִ��
	print 'lucy'
	x = raw_input("please input q for quit")
	if not x:                                 #�������˳�
		break
else:                                         #��������ִ��else��break������ִ��else
	print 'ending...'
	
15.����������͵��ã�
���������ڳ���Ĳ�ͬ�ĵط����ִ�У�����Ҫ�ظ���д
�Զ��庯����Ԥ�����Python����

def �����������б�:
���������ж�����ʣ��ڶ������ʿ�ʼ����ĸ��д

16.�������β�ʵ��Ĭ�ϲ�����
���庯��ʱ���βΣ����ú���ʱ��ʵ��
#coding:utf8              linux��utf8�����������ģ�windows��gbk����

ȱʡ������Ĭ�ϲ�����,����ֵʹ��Ĭ�ϲ�������ֵʹ�ô���ֵ
def machine(x,y='����'):              #ȱʡ�������������д�������������﷨����SyntaxError: non-default argument follows default argument��
    print "produce",x,"Ԫ",y,"��ζ�ı�����"
	
machine(10)
machine(x=10,'�ɿ���')


17.����������������
�ֲ�������ȫ�ֱ���
����������ȫ�ֱ�����Ҫ���ú�������Ч  global   
vi����ʾ�к�   vi /etc/vimrc��β����:set number(shift+G ֱ�ӵ���β)
vi�в���ʾ�к�   vi /etc/vimrc��β����:set nonumber(shift+G ֱ�ӵ���β)

18.������return����ֵ
Ĭ�Ϸ���None
returnִ�к󣬺�����ֹ
���Է����κ�ֵ�����֡��ַ������б��

sum([1,2,3,4,5])    15
sum((1,2,3,4,5))    15

19.�����������
�����ʹ�ֵ
t=('name','milo')
def f(x,y):
	print "%s :%s"  % (x,y)             #��ʽ�����

>>>f(*t)                                              #����*t��һ��Ԫ��,Ԫ���Ԫ�ظ����뺯���β�����һ��
name : milo

 #�ֵ��е�key�뺯���β�һһ��Ӧ������һ��
>>> def f(name,age):
... 	print "%s : %s" % (name,age)
... 
>>> d
{'age': 30, 'name': 'lucy'}
>>> f(**d)
lucy : 30


��ֵ����
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

20.����lambda��������
lambda������һ�ֿ��ٶ��嵥�е���С ����,û�к�������

def f(x,y):
	return x*y
	
g=lambda x,y:x*y
g(2,3)

ʹ��reduce����5�Ľ׳˼���
>>> l = range(1,6)
>>> def f(x,y):
... 	return x*y
... 
>>> reduce(f,l)
120

ֱ��ʹ��lambda����
>>> reduce(lambda x,y:x*y,l)
120

21.Switchʵ��
pythonû���ṩswitch��䣬����ʹ���ֵ�ʵ��

from __future__ import division  #������С��

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

22.�ڽ�����
abs(-2)     �����ֵ
max([1,2,3,4,5])   �����ֵ
min                     ��Сֵ
len()                    �����еĳ���
divmod(5,2)         ���̺�ģ
pow(2,3)              2�����η�
round(2)              ����ת�ɸ�����
callable()              ���Ժ����Ƿ��ǿɵ���
isinstance(l,list)     �ж�����
cmp('lucy','lili')                    �ж�2�������Ƿ�һ��
range(10)                           ��ȡ����
xrange(10)                          ��ȡ���е�����������rangeЧ�ʸ�

����ת������
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


23.�ڽ��������ַ�������
str.capitalize()                  ����ĸ��д
str.upper()                         ��ĸ��д
str.lower()                         ��ĸСд
str.replace('hello','good')    helloת����good

str.split('.')                          f
�ָĬ���Կո�ָ�,
>>> ip 
'192.168.1.123'
>>> ip.split('.')
['192', '168', '1', '123']
>>> ip.split('.',1)           #1��ʾֻ����һ�ηָ�
['192', '168.1.123']


�鿴����
help(str.replace)


ʹ��string���в���
import string
string.replace(s,'hello','good')  helloת����good  python2
str.replace(s,'hello','good')  helloת����good  python3

���д�����
len()
max()
min()

filter()             #����ֵΪTrue�ı�������
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

24.�ڽ����������д���
zip()                          #����̵ĺϲ���ע��python3��zip���������������ɵ���������Ϊ����,�������ж�Ӧ��Ԫ�ش����һ��tuple,Ȼ�󷵻�һ���ɵ�����zip����.       
>>> name = ['mile','zou','tom']
>>> age=[20,30,40]
>>> tel=['133','156','189']
>>> test=[1,2]
>>> zip(name,age,tel)
[('mile', 20, '133'), ('zou', 30, '156'), ('tom', 40, '189')]
>>> zip(name,age,tel,test)
[('mile', 20, '133', 1), ('zou', 30, '156', 2)]




map()                         #����ĺϲ� ��û����None��� ��ע��python3��map��������һ��map����ʹ��list(map())�����ؽ��
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

��
>>> reduce(lambda x,y:x+y,l)
5050

filterҲ����ʹ��lambda
filter(lambda x:x%2==0 , l)

25.����ģ��
ģ����python��֯����Ļ�����ʽ
��.py�ű�������(import)�������ű�������ʱ�����ǽ����Ϊģ��

ģ������ű����ļ�����ͬ
switch.py:
from __future__ import division  #������С��

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

if  __name__  ==  "__main__"                        #ִ��python switch.py��ʾ__main__,,�������ִ��    new.py������ʾswitch������Ĳ�ִ��
	f(2,"/",3)

new.py:
import switch
switch.jia(1,2)
��
from switch import jia
jia.(1,2)

python����ģ���˳��
��ǰĿ¼�²���
libĿ¼��

����python����ļ�  rpm -ql python
linux����.py�ļ�   find / -name '*.py'

Python��ģ����԰�Ŀ¼��֯Ϊ��
�������Ĳ��裺
����һ������Ϊ�����ֵ��ļ���
�ڸ��ļ����´���һ��__init__.py�ļ�
������Ҫ��Ŀ¼�·��ýű�

import csvtpy.switch           #csvtpy�ǰ�����switch�ǽű�����ģ�飩
print csvtpy.switch.jia(1,2)   


26.������ʽ����ʼ��
������ʽ��һ��С�͡�רҵ���ı������

ʹ��������ʽ����Ҫ����reģ��


�ַ�ƥ��
��ͨ�ַ�
>>> import re
>>> s = r'abc'
>>> re.findall(s,"123abc12abc")
['abc', 'abc']

Ԫ�ַ�
. ^ $ * + ? {} [] \ | ()

[] �ƶ�һ���ַ�����ƥ�����е�һ���ַ�
>>> s = r 'a[a-z]c'
>>> re.findall(s,"abc a1c azc")
['abc', 'alc', 'azc']
s = r 'a[^ab]c'   # ��[]��^��ʾȡ��
Ԫ�ַ���[]�в�������
[0-9]        #��������
[a-zA-Z0-9]  #������ĸ������

^ ƥ������
>>> re.findall(r'^hello','hello 12 hello hello2')
['hello']


$ ƥ����β
>>> re.findall(r'hello$','hello 12 hello 2hello')
['hello']



27.������ʽ��Ԫ�ַ���

\        
a.��Ҫƥ��Ԫ�ַ�����Ҫ��Ԫ�ַ�ǰ�� \
>>> re.findall(r'\^abc','^abc b^abc')
b.  \����Ӳ�ͬ���ַ����Ա�ʾ��ͬ�����⺬��
\d     ��ʾ����������ַ����൱��[0-9]
\D     ��ʾ�κη������ַ�   [^0-9]
\w     ��ʾ�������ĸ�����ַ� ���൱��[0-9a-zA-Z]
\W     ��ʾ����ķ���ĸ�����ַ� ���൱��[^0-9a-zA-Z]
\s     ��ʾ����հ��ַ����൱��[\t\n\r\f\v]                       #�û���ע����õ�
\S     ��ʾ����ǿհ��ַ����൱��[^\t\n\r\f\v]


.       ƥ�������ַ������˻��з�
*      �ظ�  ǰ��һ���ַ�0�ε����

r'^010-\d{8}'              {}ƥ��ǰ��һ���ַ��ظ�8��

+      �ظ�  ǰ��һ���ַ�1�ε����    

��     �ظ�  ǰ��һ���ַ�0�λ�1��
       ʵ����Сƥ��
>>> re.findall(r'ab+','abbbbbbbbbbbbbbbbbbbbbbbbbbbbbb')                      #̰��ƥ��
['abbbbbbbbbbbbbbbbbbbbbbbbbbbbbb']
>>> re.findall(r'ab+?','abbbbbbbbbbbbbbbbbbbbbbbbbbbbbb')                     #��Сƥ��
['ab']


{} �ظ�  ǰ��һ���ַ��ظ�����
{1,3}   �ظ�1��3��
{3}     �ظ�3��


28.������ʽ�����ú�����
����
>>> p_tel=re.compile(r'010-?\d{8}')
>>> p_tel.findall('010-12345678')
['010-12345678']

�����ִ�Сд
>>> p_csvt=re.compile(r'csvt',re.I)
>>> p_csvt.findall('csvt CSvt1')
['csvt', 'CSvt']

#match��ͷƥ�䵽(�ǿ�ͷƥ�䵽�Ĳ���)������һ�����󣬷��򷵻ؿ�
>>> p_csvt.match('csvt CSvt1')          
<_sre.SRE_Match object at 0x7fe4d18ce648>       
>>> p_csvt.match('cs1vt C2Svt1')
>>> p_csvt.match('cs1vt CSvt1')

>>> x= p_csvt.match('csvt CSvt1')   #����matchƥ����ַ���
>>> x.group()
'csvt'
ʵ��ʹ�����ǽ�Match���صĶ��󱣴���һ�������Ȼ�������Ƿ�ΪNone



#search����λ��ƥ�䵽������һ�����󣬷��򷵻ؿ�
#findall()  ��������ƥ�䵽���Ӵ��������б���ʽ����
#finditer()  ��������ƥ�䵽���Ӵ������Ե�������ʽ���أ���next()�����鿴�����ֵ��match����


re.sub         #�����滻����replace�Աȿ��Խ�������replaceֻ�ܶԾ����ַ�
>>> rs=r'c..t'
>>> re.sub(rs,'python','csvt caat cvvt ccccct')
'python python python ccpython'
>>> re.subn(rs,'python','csvt caat cvvt ccccct')
('python python python ccpython', 4)          #ͳ��ƥ�����


split �и�
>>> ip = '1.2.3.4'
>>> ip.split('.')
['1', '2', '3', '4']

>>> s = '123+456-789*000'    
>>> re.split(r'[\+\-\*]',s)    #�����и+-* �������ַ�����\ת��
['123', '456', '789', '000']


29.������ʽ��re���Է��飩
���˱�־
S  ʹ.ƥ������������ڵ������ַ�
I  ���Դ�Сд
M  ���ж���ƥ��
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



X    ������ʽ���Զ����е��з�
>>> tel = r"""
... \d{3,4}
... -?
... \d{8}
... """
>>> re.findall(tel,'010-12345678')
[]
>>> re.findall(tel,'010-12345678',re.X)
['010-12345678']


����
>>> email = r'\w{3}@\w+(\.com|\.cn)'
>>> re.findall(email,'zzz@csvt.com')    #�������ȷ��ط��鵱�еĵ�����
['.com']


30.����
��ȡԴ�����ģ��
import urllib
urllib.urlopen(url)

����ͼƬ���� 
urllib.urlretrieve(img,'1.jpg')         #����ͼƬ��������1.jpg
urllib.request.urlretrieve(img,'1.jpg')    #����ͼƬ��������1.jpg (python3)

�����������������˫���ţ��������õ�����;�����ַ���\ת��;��Ҫʹ��?������Сƥ��


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
        urllib.urlretrieve(img,'%d.jpg' % x)                      #����ͼƬ��ַ��������
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
    #bytes�����string
    return html.decode('UTF-8')

def Down(html):
    img = re.compile(r'https://.+?\.jpg')
    list1 = re.findall(img,html)
    print(list1)
    x = 1
    for i in list1:
        urllib.request.urlretrieve(i,'%s.jpg' % x)
        #��������ǽ��ļ����ص�ָ����Ŀ¼��
        #urllib.request.urlretrieve(img,'E:\\python\\38\\30\\%s.jpg' % x)
        x += 1

url = 'https://image.baidu.com/search/index?tn=baiduimage&ipn=r&ct=201326592&cl=2&lm=-1&st=-1&fm=index&fr=&hs=0&xthttps=111111&sf=1&fmq=&pv=&ic=0&nc=1&z=&se=1&showtab=0&fb=0&width=&height=&face=0&istype=2&ie=utf-8&word=minieye&oq=minieye&rsp=-1'
html = Open(url)
Down(html)


31.�����ǳ����
python���ڴ������
ǳ�����Ƕ����õĿ�����ֻ����������
����ǶԶ�����Դ�Ŀ���
import copy


#���������һ���ڴ��������ã�һ�������޸ģ������Ķ��޸ģ��ұ������ڴ�id��һ�µ�
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

#�Ա�����copy�������ڴ������¿���һ���ռ䣬�����ı䣬������copy����
>>> import copy
>>> a = [1,2,3,['a','b','c']]
>>> b=a
>>> c = copy.copy(a)
>>> 
>>> id(a)
139907157826304
>>> id(b)
139907157826304
>>> id(c)                            #������copy��id�ǲ�һ����
139907157426472
>>> id(a[0])                         #ǳ��������Ԫ�ص�id���䣬ֻ�ǶԸ����������copy
13816152
>>> id(c[0])
13816152

>>> a.append('d')                    #����������˿������޸ĸ�����ǳ�����Ķ�Ӧ�����޸�       
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
>>> a[3].append('d')                #�Ӷ���û�н��п������޸��Ӷ������֡��ַ�����Ԫ�鲻���޸ģ��б�����޸�,����ǳ�����Ķ�ӦҲ���޸�
>>> a
[1, 2, 3, ['a', 'b', 'c', 'd'], 'd']
>>> c
[1, 2, 3, ['a', 'b', 'c', 'd']]




#  �������������Ӷ��󶼽�����copy
>>> d=copy.deepcopy(a)
>>> a
[1, 2, 3, ['a', 'b', 'c', 'd'], 'd']
>>> d
[1, 2, 3, ['a', 'b', 'c', 'd'], 'd']
>>> id(a)
139907157826304
>>> id(d)                 #����������˿���
139907157426256
>>> id(a[3])
139907157826232
>>> id(d[3])              #�Ӷ�������˿���
139907157826088
>>> id(a[0])            
13816152
>>> id(c[0])              #�Ӷ����в��ɱ�Ԫ�ز��ܿ���   
13816152


32.�ļ�֮�ļ���д
python�����ļ���д�ĺ�����open��file��
mode:
r   ֻ��
r+  ��д
w   д�룬��ɾ��ԭ�ļ���������д�룬����ļ�û���򴴽�
w+  ��д����ɾ��ԭ�ļ���������д�룬����ļ�û���򴴽�
a   д�룬���ļ�ĩβ�����µ����ݣ��ļ������ڣ�����
a+  ��д�����ļ�ĩβ�����µ����ݣ��ļ������ڣ�����

>>> fi = open('test.txt')
>>> fi
<open file 'test.txt', mode 'r' at 0x7f49f908d540>
>>> fi.read()                #���ļ�
'123\n'
>>> fi.close()               #�ر��ļ�
��
>>> f1 = file('test.txt')
>>> f1
<open file 'test.txt', mode 'r' at 0x7f49f908d5d0>
>>> f1.read()
'123\n'
>>> f1.close()



>>> f1=open('test.txt','w')
>>> f1.write('lucy')            #д�ļ�������
>>> f1.close()                  #ֻ�йرպ󣬲��ܿ����ļ���д��


>>> f1 = open('test.txt','r+')
>>> f1.read()                   #��ȡ��ָ��ָ�����û��read������ָ���ڿ�ʼλ��
'lucy'
>>> f1.write('lili')
>>> f1.close()                  #�رպ�鿴����ʾlucylili

>>> f1 = open('test.txt','r+')
>>> f1.write('tom')
>>> f1.close()                  #�رպ�鿴����ʾtomy��û��read������ָ���ڿ�ʼλ�ý���д����������ԭ���ģ�



33.�ļ�֮�ļ�����ķ���
FileObject.read()    �����ַ���

test.txt  ��
lucy
tom
lili

readline     ÿ�ζ�ȡһ��
>>> f1 = open('test.txt')
>>> f1.readline()
'lucy\n'
>>> f1.readline()
'tom\n'
>>> f1.readline()
'lili\n'
>>> f1.readline()   #  ������Χ���ؿ�
''
>>> 


>>> for i in open('test.txt'):
...     print i
... 
lucy

tom

lili


readlines     ��ȡ����ԭ�򣬵����б���ʽ����ÿ������
>>> f1 = open('test.txt')
>>> f1.readlines()
['lucy\n', 'tom\n', 'lili\n']


next          ���ص�ǰ�У������ļ�ָ�뵽��һ��
>>> f1 = open('test.txt')
>>> f1.next()
'lucy\n'
>>> f1.next()
'tom\n'
>>> f1.next()
'lili\n'
>>> f1.next()         #������Χ����ֹͣ�������Ǳ�readline�Ż��ĵط�
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
StopIteration


write
writelines(List)  ����д��Ч�ʱ�write�ߣ�����д������ write

>>> l = ['one\n','two\n','three\n']
>>> f1 = open('test.txt','a')
>>> f1.write(l)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: expected a string or other character buffer object
>>> f1.writelines(l)
>>> f1.close()

seek(ƫ������ѡ�
--ѡ��0����ʾ���ļ�ָ��ָ����ļ�ͷ����ƫ�����ֽڴ�
--ѡ��1����ʾ�ļ�ָ��ָ����ļ���ǰλ�ã�����ƶ�ƫ�����ֽ�
--ѡ��2����ʾ�ļ�ָ��ָ���ļ�β������ǰ�ƶ�ƫ�����ֽ�
seek(0,0)  �ļ�ָ���Ƶ���ͷ
seek(0,2)  �ļ�ָ���Ƶ���β

f1.seek(0,0)

flush()   �ύ����


a.t  :
hello world
hello hello world


ͳ��a.t�ļ���hello������
find.py
#!/usr/bin/python
import re

res = r'hello'
f = open('a.t','r')
list1 = re.findall(res,f.read())
print len(list1)
f.close()


��a.t�е�hello�滻Ϊcsvt,�����������ļ�a2.t��
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
��
#!/usr/bin/python
import re

f1 = open('a.t','r')
f2 = open('a2.t','w')
s =  f1.readlines()
for x in s:
    f2.write(x.replace('hello','csvt'))
f1.close()
f2.close()


��a.t�е�hello�滻Ϊcsvt,�����������ļ�a.t��
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


34.�ļ�֮OSģ��
Ŀ¼��������ͨ��python��ʵ��Ŀ¼�Ĵ������޸ĺͱ����ȹ���

import os
Ŀ¼������Ҫ����osģ�飬����os.mkdir('/root/csct')

>>> import os
>>> os.mkdir('test')   #����Ŀ¼

�����༶Ŀ¼  mkdir -p a/b/c
>>> os.makedirs('a/b/c')  
# tree a
a
������ b
    ������ c

ɾ��Ŀ¼
os.rmdir('test')

ɾ���༶Ŀ¼a
os.removedirs('a/b/c')

ɾ���ļ�
os.remove()


��ʾ��ǰĿ¼���ļ��������ص�һ���ļ����ļ��У�
os.listdir��'.')
��ʾ��Ŀ¼���ļ�
os.listdir��'/')


��ʾ��ǰĿ¼·��
os.getcwd()

�л�Ŀ¼
os.chdir('/')
>>> os.chdir('/')
>>> os.listdir('.')
['sys', 'media', 'dev', 'sbin', 'lost+found', 'mnt', 'home', 'run', 'tmp', 'snap', 'opt', 'var', 'bin', 'usr', 'lib64', 'lib', 'srv', 'etc', 'initrd.img', 'root', 'vmlinuz', 'proc', 'boot']
>>> os.getcwd()
'/'

35.Ŀ¼����֮ɱ�����

os.path.join(path1,path2)   ·���ϲ�
os.path.isdir(path)         �ж��Ƿ���Ŀ¼
os.path.isfile(file)         �ж��Ƿ����ļ�



����ָ��Ŀ¼�������ļ��ľ���·��
#!/usr/bin/python
import os
paths = []
def path(name):
    for x in os.listdir(name):
        path2 = os.path.join(name,x)               #path2 = name + '/' +x    �������Ҳ��
        if os.path.isdir(path2):                   #ʹ�õݹ�ķ���
            path(path2)
        else:
            paths.append(path2)
    return paths

print path('/root/python/file/testdir')


os.walk(path) 

>>> os.walk('/root/python/file/testdir')      #����������
<generator object walk at 0x7f04375e77d0>   
>>> g = os.walk('/root/python/file/testdir')
>>> g.next()              #ע��python3��ִ��next(g)
('/root/python/file/testdir', ['jpg'], ['f1', 'f2', 'f3'])    #����Ԫ�飬�ֱ𷵻ص�ǰ·������ǰĿ¼��·������ǰĿ¼���ļ�
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



����Ŀ¼����Ŀ¼���ļ����ְ���f���ļ�ɾ��
# tree testdir
testdir
������ f1
������ f2
������ f3
������ jpg
    ������ f22
    ������ getjpg.py


�ݹ�ķ�����
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



walk�ķ�����
>>> g = os.walk('/root/python/file/testdir')
>>> 
>>> for path,d,filelist in g:
...     for filename in filelist:
...         allfile = os.path.join(path,filename)
...         if 'f' in filename:
...             os.remove(allfile)




��Ŀ¼���ļ����ݰ���123���ļ�ɾ��
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


36.�쳣����
�쳣�׳����ƣ�Ϊ���򿪷���Ա�ṩһ�ַ��ִ��󣬽��лָ�����


try:
    f = open('abc.txt')
    print hello
except IOError as msg:                        #����ʵ�ʱ��������쳣
    print 'IOError'
except NameError,msg:                      #���Բ������쳣
    pass
finally:
     f.close()                             #�����Ƿ����finally�µ����ݶ���ִ��,һ�����ļ��رգ��ͷ��������ݿ����ӷ��ظ����ӳء�finally��Ҳ��������if\try�ȸ������

raise�׳��쳣�������Լ����������Ϣ����һ��Ҫ�Ǵ��ڵĴ�������
x = 'hello'
if x == 'hello':
    raise Error("x is equal hello!!!")

Traceback (most recent call last):
  File "36.py", line 18, in <module>
    raise NameError("x is equal hello!!!")
NameError: x is equal hello!!!

������Python�쳣
IOError                ��������쳣���������޷����ļ�
ImportError            �޷�����ģ����
IndentationError       �﷨���󣬴���û����ȷ����
IndexError             �±곬�������༭
KeyError               ��ֵ���ֵ��в�����
NameError              ����û�ж���
SyntaxError            �����߼��﷨���󣬲���ִ��
ValueError             ����һ������������ֵ  




except NoSuchElementException as e:                #���e���쳣��NoSuchElementException��һ��ʵ��
    print (e)

37.MySQLdb

http://www.linuxidc.com/Linux/2016-07/133128.htm  ��װmysql
��mysql���洴�����ݣ���python������ɾ�Ĳ�

��½mysql(ubuntu,����root)
mysql -u root -p
mysql> show databases;        #�鿴��ǰ���ݿ�
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
4 rows in set (0.00 sec)

mysql> use mysql;              #�������ݿ�
mysql> show tables;            #�鿴��ǰ���ݿ��±�

mysql> desc python;            #�鿴��ṹ

mysql> insert into python values(1,'lucy',21);            #��������

mysql> insert into python values(2,'lili',22),(3,'tom',23); 


mysql> create table python(id INT NOT NULL,name VARCHAR(40) NOT NULL,age INT NOT NULL);   #������

mysql> create database view;    �������ݿ�


            
 
  
��װMySQL-python   http://www.jb51.net/article/87364.htm  
(ע:python3��֧��MySQLdb����mysql.connector���)

python3�������ݿ����£�
import mysql.connector
conn = mysql.connector.connect(user='root', password='root',host='127.0.0.1', database='mysql')
cursor = conn.cursor()
#����������Խ�� InternalError("Unread result found")����
cursor = conn.cursor(buffered=True)

python2�������ݿ�����:
>>> import MySQLdb
>>> conn = MySQLdb.connect(user='root',passwd='root',host='127.0.0.1')     #�������ݿ�
>>> cur = conn.cursor()                                                    #��Ҫʹ���α�������ݿ�
>>> conn.select_db('mysql')                                                #���Ŀ�
>>> cur.execute("insert into python value('2','lili',20)")                 #��������
1L
>>> conn.commit()                                                          #�ύ��Ч

>>> sqli = "insert into python value(%s,%s,%s)"                            #��ʽ����������
>>> cur.execute(sqli,(3,'tom',25))
1L

>>> sqlim = "insert into python values(%s,%s,%s)"                          #��ʽ�����Ӷ���
>>> cur.executemany(sqlim,[(4,'jim',23),(5,'lilei',26)])                   #
2L

>>> cur.execute("delete from python where id = 2")                         #ɾ��һ��
1L
>>> cur.execute("update  python set name = 'lucy2' where id = 3")          #�޸�һ��


>>> cur.execute("select * from python")                                    #��ѯ����
4L
>>> cur.fetchone()
(1L, 'lucy', 21L)
>>> cur.fetchone()
(3L, 'lucy2', 25L)

>>> cur.scroll(0,'absolute')                                               #�α��Ƶ���ͷ
>>> cur.fetchone()
(1L, 'lucy', 21L)

>>> cur.scroll(0,'absolute')                      
>>> cur.fetchmany(4)                                                       #ȡ��ȫ��4������
((1L, 'lucy', 21L), (3L, 'lucy2', 25L), (4L, 'jim', 23L), (5L, 'lilei', 26L))    

>>> cur.fetchmany(cur.execute("select * from python"))                     #һ������ȡ��ȫ��4������
((1L, 'lucy', 21L), (3L, 'lucy2', 25L), (4L, 'jim', 23L), (5L, 'lilei', 26L)) 


cur.close()                                                                #�ر��α�
conn.close()                                                               #�ر�����

�鿴mysql�Ķ˿�
show global variables like 'port'


ɾ�����ݿ�����ݿ��ʧ��(����)��ʹ�����������鿴ʲô����������
mysql> show full processlist;
kill + idɱ����Ӧ�Ľ���

38.�������֮��Ͷ���
��Ͷ���������������Ҫ����
��������ĳ��󣬶��������һ��ʵ��


>>> class Test:
...     first = 123
...     second = 456
...     def f(self):                          #���к�������һ���β�self,����Ҫ��ֵ����ʵ�Ǵ�����������
...         return 'test'
... 

>>> milo = Test()                             #�������
>>> milo.f()
'test'
>>> milo.first
123


>>>help(list)                                 #�б�Ҳ��һ����
Help on class list in module __builtin__:

class list(object)
 |  list() -> new empty list
 |  list(iterable) -> new list initialized from iterable's items


Add:
1. try except else
try��ִ�п��ܻ�������̽����䣬�������������ǿ��Ե��������Դ���ʹ�ó����޷�����ִ����ȥ
except�����try���������޷���ȷִ�У���ô��ִ��except�������䣬����������Ǵ�����Ϣ���������Ŀ�ִ�����
else�����try���������������ִ�У���ô��ִ��else�������䣨�൱�ڳ���û�����������Դ���

2.���Ϊassert�����������쳣����
assert expression [, arguments]
assert (add == 5),"Integer addition result error!"

3.�����Ľ���װ���������þ���Ϊ�Ѿ����ڵĶ�����Ӷ���Ĺ��ܡ�
�����������������ڲ���Ҫ���κδ���䶯��ǰ�������Ӷ��⹦�ܣ�װ�����ķ���ֵҲ��һ����������

4.��python�£���ȡ��ǰִ�����ű��ķ�����������sys.argv[0]��__file__
��ȡ���ļ�·������ѷ�������sys.argv[0]���ڽ�����__file__ Ҳ���������ģ�����ڵ�·����

5.os.path.dirname(path) 
����path���ڵ�Ŀ¼���ļ�����һ��Ŀ¼��

6.S.join()
���ڽ������е�Ԫ����ָ�����ַ���������һ���µ��ַ���

str = "-";
seq = ("a", "b", "c"); # �ַ�������
print str.join( seq );
����ʵ�����������£�
a-b-c

7.json.dumps()��json.loads()��json��ʽ��������������ô��⣬json���ַ�����
import json
����(1)json.dumps()�����ǽ�һ��Python���������б����json��ʽ�ı��루������ô��⣬json.dumps()�����ǽ��ֵ�ת��Ϊ�ַ�����
����(2)json.loads()�����ǽ�json��ʽ����ת��Ϊ�ֵ䣨������ô��⣬json.loads()�����ǽ��ַ���ת��Ϊ�ֵ䣩
       (3)json.dump()�������ֵ�ת����json��д��json�ļ�
>>> d = dict(name='Bob',age=20,score=88)
>>> f = open('dump.json','w')
>>> json.dump(d,f)
>>> f.close()
       (4)json.load()������json�ļ��ж�ȡ�ַ����������л����ֵ�
>>> f = open('dump.json','r')
>>> json.load(f) 
{'name': 'Bob', 'age': 20, 'score': 88}
      

8. ���������� Click
init_case.py

__author__ = 'muhongyun <muhongyun@minieye.cc>'
__version__ = '0.1.0'
__progname__ = 'init_case'

@click.command(name='handle-case')
@click.help_option('-h', '--help')
#�鿴�汾
@click.version_option(__version__, '-v', '--version', prog_name=__progname__, message='%(prog)s version %(version)s')
@click.option('-p', '--para-file', type=str, default='', help='ָ���ű������ļ� (default: none)')
@click.option('-c', '--case-path', type=str, default='', help='ֱ��cli����case·��')
def cli(**options):
    #��ӡoptions�ֵ�
    print('options:', options)
    ...
if __name__ == '__main__':
    cli()

#�鿴�汾
PS E:\python\3.6\click> python3 init_case.py -v
init_case version 0.1.0
#��ӡĬ���ֵ�����ע������para-file���Զ�ת��para_file
options: {'para_file': '', 'case_path': ''}



Click ��ʹ�ô������������裺
ʹ�� @click.command()װ��һ��������ʹ֮��Ϊ�����нӿڣ� 
ʹ�� @click.option()��װ�κ�����Ϊ�����������ѡ���,Ϊ�����ṩ������ 
����һ�ֵ���ʹ����ʽ���£�

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

$ python hello.py --help   # click �������Զ������� `--help` �÷�
Usage: hello.py [OPTIONS]

  Simple program that greets NAME for a total of COUNT times.

Options:
  --count INTEGER  Number of greetings.
  --name TEXT      The person to greet.
  --help           Show this message and exit.


Argument ����
Argument ���������� Option����û�� Option ��ôȫ��Ĺ��ܡ�
�� Option һ����Argument �������Ӧ�þ��Ǵ���һ���򵥱���ֵ��
import click
@click.command()
@click.argument('filename')
'''
�����������һ��
def touch(**arguments):
    print(arguments['count'])
'''
def touch(filename):
    click.echo(filename)
if __name__ == '__main__':
    touch()
    
python do_click.py name1
ִ�н��
name1



9.
self.xxx��ȫ�ֵģ�xxx�Ǿֲ��Ķ��ڸ÷�����Ч
python���෽����������Ҫ��self��Ҳ����self.xxx������Ƿ��������ԣ�
�෽���ı�������self��Ҳ����xxx������Ƿ����ľֲ����������ܱ����ã�ֻ���ڸ÷����ڲ�ʹ�ã�

10��ִ�нű�ʱָ������  python3 1.py /home/1.json
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

ʹ��argparseָ������
#do_argparse.py
import argparse

def run(ip, origin_save, result_save, path):
    pass
if __name__ == "__main__":
    #crl:��Ӳ�������
    parser = argparse.ArgumentParser()
    #crl:z���Ӳ���
    parser.add_argument("--ip", help="ip address",type=str)
    parser.add_argument("--origin", help="�Ƿ񱣴�ԭʼͼƬ��Ĭ�ϲ�����",type=str)
    parser.add_argument("--result", help="�Ƿ񱣴洦���ͼƬ��Ĭ�ϲ�����",type=str)
    parser.add_argument("--path", help="����ͼƬ��·��",type=str)
    args = parser.parse_args()
    run(args.ip, args.origin, args.result, args.path)

ִ�нű� 
python3 do_argparse.py --ip 192.168.1.251 --origin 1 --result 1 --path '/home/pc_view/image/'



11�����з������ø����е���������,��Ҫ��self
class Student(object):
    def fun1(self):
        pass
    def fun2(self):
        self.fun1()
stu = Student()
stu.fun2()

12��slice() ����
slice() ����ʵ����Ƭ������Ҫ������Ƭ����������Ĳ�������

slice �﷨��
class slice(stop)
class slice(start, stop[, step])
����˵����
start -- ��ʼλ��
stop -- ����λ��
step -- ���

>>>myslice = slice(5)    # ���ý�ȡ5��Ԫ�ص���Ƭ
>>> myslice
slice(None, 5, None)
>>> arr = range(10)
>>> arr
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
>>> arr[myslice]         # ��ȡ 5 ��Ԫ��
[0, 1, 2, 3, 4]
>>>

13��reduce��python3�д��ڽ������Ƴ��ˣ�ֱ��ʹ�ûᱨ��������functoolsģ��
>>> reduce(lambda x,y:x+y,[1,2,3])
NameError: name 'reduce' is not defined

from functools import reduce


14��С��ת�ɰٷְ����
rate = 0.1
res = format(rate, '.0%')
    # res == '10%'

15������״ͼ   
�ο� https://blog.csdn.net/jenyzhang/article/details/52047557
matplotlib.pyplot.bar(left, height, width=0.8, bottom=None, hold=None, data=None, **kwargs)

����˵����
left: ÿһ����������X����(���ֵʵ����ʾ���ε��м�X����)
height:ÿһ�����εĸ߶�
width: ����֮��Ŀ��
bottom: ���ε�Y����
color: ���ε���ɫ

ʾ����
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
  
���⣺
(1)linux�ϱ�����״ͼ��ʱ���� 
#ִ����ʾ����ִ��plt.savefig�����ͼƬ�ǿհ�ͼƬ��
plt.show()
#ע����Ҫ������״ͼ����linux���뱣���.png�ļ������򱨴�    
plt.savefig("barChart.jpg")

(2)��״ͼ��ʾ������������

a.
Python�汾��matplotlib�����ļ�λ�ò�ѯ

[hadoop@p168 ~]$ python
>>> import matplotlib

>>> print matplotlib.matplotlib_fname()

/home/hadoop/.pyenv/versions/2.7.10/lib/python2.7/site-packages/matplotlib/mpl-data/matplotlibrc
b.
���Ƚ�windwos��fontsĿ¼�µ�simhei.ttf������/home/hadoop/.pyenv/versions/2.7.10/lib/python2.7/site-packages/matplotlib/mpl-data/fonts/ttf
(�ļ�·���ο�a������ʵ������޸�)Ŀ¼�У�
Ȼ��ɾ��~/.cache/matplotlib�Ļ���Ŀ¼(�û�Ŀ¼��)


c.
�����ڴ����ж�̬���ò�����


import matplotlib.pyplot as plt 

plt.rcParams['font.sans-serif'] = ['SimHei']


plt.xlabel('ʱ���')  #   

16��str.strip()
���������Ƴ��ַ���ͷβָ�����ַ���Ĭ��Ϊ�ո�

17��pythonдutf8�ļ�
import codecs
f = codecs.open("demo_1.html",'w',encoding='utf8')
f.write(message)
f.close()

18.subprocess.call
�ӽ��̵���
subprocess.call()��ִ�����������ִ��״̬������shell����ΪFalseʱ��������Ҫͨ���б�ķ�ʽ���룬��shellΪTrueʱ����ֱ�Ӵ�������
ʾ�����£�
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

#ִ�������׼���д��out.log,��׼����д����׼���ͬһ���ļ�
subprocess.call('ping -n 2 www.baidu.com',shell=True,stdout='out.log',stderr=subprocess.STDOUT)
subprocess.call('ping -n 2 www.baidu.com > out.log 2>&1',shell=True)

19.os.path.basename��os.path.splitext��os.path.split
os.path.basename(path)���������ļ���  os.path.splitext�����ļ������ļ���չ��
os.path.split���԰�һ��·�����Ϊ�����֣���һ����������󼶱��Ŀ¼���ļ���

20.��������
import bisect 

L = [1,3,3,6,8,12,15]    #ע��L�е�ֵ�������
x = 3  
  
x_insert_point = bisect.bisect_left(L,x)����#��L�в���x��x����ʱ����x����λ�ã�x�����ڷ���Ӧ�ò����λ��..����3�������б��У��������λ�ã�  
print x_insert_point  
  
x_insert_point = bisect.bisect_right(L,x)  #��L�в���x��x����ʱ����x�Ҳ��λ�ã�x�����ڷ���Ӧ�ò����λ��..����3�������б��У������Ҳ�λ�ã�  



21.Ĭ�ϵȼ���WARNING������ζ�Ž�������ȼ������ϵĲŻᷴ����Ϣ
����             ����ֵ
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

���
======================= RESTART: E:\python\100\test.py =======================
WARNING:root:This is warning log
ERROR:root:This is error log
CRITICAL:root:This is critical log


������־������־����logging.basicConfigֻ���ǵ�һ��������Ч���´�������ʱ����Ҫ���˳�python exit()
logging.basicConfig(level=logging.DEBUG)
��������:
======================= RESTART: E:\python\100\test.py =======================
DEBUG:root:This is debug log
INFO:root:This is info log
WARNING:root:This is warning log
ERROR:root:This is error log
CRITICAL:root:This is critical log

������־������ļ���
import logging
LOG_FORMAT = '%(asctime)s - %(levelname)s - %(message)s'
logging.basicConfig(filename='my.log',level=logging.DEBUG,format = LOG_FORMAT)
logging.debug('This is debug log')
logging.info('This is info log')
logging.warning('This is warning log')
logging.error('This is error log')
logging.critical('This is critical log')

��ʱ�ᷢ�ֿ���̨���Ѿ�û�������־�����ˣ�������python�����ļ�����ͬĿ¼�»�����һ����Ϊ'my.log'����־�ļ������ļ��е�����Ϊ��
2018-07-20 12:20:04,638 - DEBUG - This is debug log
2018-07-20 12:20:04,639 - INFO - This is info log
2018-07-20 12:20:04,639 - WARNING - This is warning log
2018-07-20 12:20:04,639 - ERROR - This is error log
2018-07-20 12:20:04,640 - CRITICAL - This is critical log


22.insert() �������ڽ�ָ����������б��ָ��λ�á�
list.insert(index, obj)

23.�ҵ��ַ�����ָ���ַ�����λ��
s1 = 'abcdef'
s2 = 'bcd'
print(s1.find(s2))

24.�����IDLE�н�����������
Ctrl + [  ����
Ctrl + ]  ǰ��

25.�����ַ������Ӵ����ֵĴ���
str1.count(str2)

26. r/R:��ת���ԭʼ�ַ��� 
����ͨ�ַ���ȣ��������������ַ������п��ܰ���ת���ַ�������Щ����б�ܼ��϶�Ӧ��ĸ����ʾ��Ӧ�����⺬��ģ���������ġ�\n����ʾ���У���\t����ʾTab�ȡ�
���������r��ͷ����ô˵��������ַ���������ͨ���ַ��ˣ�������ǡ�\n����ô��ʾһ����б���ַ���һ����ĸn�������Ǳ�ʾ�����ˡ� 
>>> str1 = r'12\n345'
>>> str2 = '12\n345'
>>> print(str1)
12\n345
>>> print(str2)
12
345

27.python2�е�cmp��python3�е�operator���
import operator
operator.eq(1,1)  ����

operator.lt     С��
operator.le    С�ڵ���
operator.eq   ����
operator.ne   ������
operator.gt    ����
operator.ge   ���ڵ���

28.�������ҪΪһ�������ں�����ı�����ֵ����ô��͵ø���Python������������Ǿֲ��ģ����� ȫ�� �ġ�����ʹ��global��������һ���ܡ�û��global��䣬�ǲ�����Ϊ
�����ں�����ı�����ֵ�ġ�
>>> y = 3
>>> def fun1():
...     global y
...     y = 5
...
>>> fun1()
>>> y
5

29.�����������ȡn������
>>> from random import sample
>>> sample('abcde',2)
['c', 'd']

30.time ģ��
>>> from time import *
>>> time1 = time()       #��ȡ��ǰ����ʱ��
>>> time1
1534130206.3175268
>>> localtime(time1)    #������ת����ʱ��Ԫ��
time.struct_time(tm_year=2018, tm_mon=8, tm_mday=13, tm_hour=11, tm_min=16, tm_sec=46, tm_wday=0, tm_yday=225, tm_isdst=0)
>>> asctime(localtime(time1))   #��ʱ��Ԫ��ת�����ַ���
'Mon Aug 13 11:16:46 2018'
>>> mktime(localtime(time1))   #��ʱ��Ԫ��ת��������
1534130206.0

>>> ctime()    #��ȡ��ǰ�ַ���ʱ�䣬����ʹ��asctime()
'Fri Aug 17 14:22:00 2018'
>>> localtime()  #��ȡʱ��Ԫ��
time.struct_time(tm_year=2018, tm_mon=11, tm_mday=19, tm_hour=17, tm_min=8, tm_sec=4, tm_wday=0, tm_yday=323, tm_isdst=0)
>>> time()         #��ȡʱ������
1542618793.8715754



31.��ӡ����Ĵ�����Ϣ
try:
    print  aa
except  NameError as msg:
    print  msg

32. map��reduce��ʹ��
#reduce��һ������������һ�������ϣ�reduce�ѽ�������е���һ��Ԫ�����ۼƼ���
>>> reduce(lambda a,b:a+b,[3,4,5])
12

#map������ĺ����������õ����е�ÿ��Ԫ�أ�����Ƕ���Ԫ��(lambda�������������и���һ��)
>>> list1 = list(map(lambda a,b:a*b,[1,2,3],[4,5,6]))
>>> list1
[4, 10, 18]

>>> list1 = list(map(lambda a:a*a,[1,2,3]))
>>> list1
[1, 4, 9]

33.os.rename() ���������������ļ���Ŀ¼���� src �� dst,���dst��һ�����ڵ�Ŀ¼, ���׳�OSError��
os.rename(src, dst)

src -- Ҫ�޸ĵ�Ŀ¼��
dst -- �޸ĺ��Ŀ¼��

34.#�ӻ���������ȡ�ַ�������ȡ����������ֵ
>>> os.getenv("TMP")
'C:\\Users\\ThinkPad\\AppData\\Local\\Temp'

35.�ַ�����ʽ��
>>> '[{}]'.format('tmp')
'[tmp]'

38.�����ļ���С
os.path.getsize(filename)

39.strftime ��ʾ��ǰʱ��
>>> from time import strftime
>>> strftime("%Y-%m-%d_%H:%M:%S")
'2018-08-22_18:17:48'

40.os.system��ִ��ϵͳ����
����ʹ�����·�����
import os
print os.system('ping www.baidu.com')
����Ľ���ǣ�
64 bytes from 223.26.58.21: icmp_seq=0 ttl=245 time=36.798 ms
64 bytes from 223.26.58.21: icmp_seq=1 ttl=244 time=37.561 ms

41. os.stat() ���������ڸ�����·����ִ��һ��ϵͳ stat �ĵ���

    ����ֵ
    stat �ṹ:

    st_mode: inode ����ģʽ
    st_ino: inode �ڵ�š�
    st_dev: inode פ�����豸��
    st_nlink: inode ����������
    st_uid: �����ߵ��û�ID��
    st_gid: �����ߵ���ID��
    st_size: ��ͨ�ļ����ֽ�Ϊ��λ�Ĵ�С�������ȴ�ĳЩ�����ļ������ݡ�
    st_atime: �ϴη��ʵ�ʱ�䡣
    st_mtime: ���һ���޸ĵ�ʱ�䡣
    st_ctime: �ɲ���ϵͳ�����"ctime"����ĳЩϵͳ�ϣ���Unix�������µ�Ԫ���ݸ��ĵ�ʱ�䣬������ϵͳ�ϣ���Windows���Ǵ���ʱ�䣨��ϸ��Ϣ�μ�ƽ̨���ĵ�����

    os.stat().st_mtime

42. eval() ��������ִ��һ���ַ������ʽ�������ر��ʽ��ֵ��
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

43.github�˺�https://github.com
chenronglei/Root_123

44.yield
��������yield�滻return,�ͳ����������������������㣬ʹ��next��������ſ�ʼ����

�ŵ�:�ӳټ��㣬��ռ���ڴ�

45.python����ת��exe
https://www.jianshu.com/p/64cb9108a7c6

46.���б�����λ��������ͨ��ǿ��ת����boolʵ�ֵ�
>>> 5 and 4      # True and True�������һ��Trueֵ
4

>>> 0 or 3 or ''    #False or True or False  ��һ��True��ֵ
3

47.���̡߳����������
a.����Ϊ����ɶ�����
b.������Ƕ�����������߳��ǹ�����������߳�Ϊ�˷�ֹ������ͻ�쳣����Ҫ�����ȸ��Ӳ�����
c.����̸��ȶ������߳���Ϊ���������ԭ��һ���߳��˳��ˣ������̶߳������˳��������һ�������Ƴ��ˣ�һ�㲻Ӱ����������
d.���߳���ΪGILȫ������ԭ�򣬲�����Ч������CPU�Ķ�ˡ�����̿�����Ч��ʹ��
e.����̿��Էֲ�ʽ���ڶ�̨������ʹ�ã��������ֻ����һ̨�����ϵ�CPU�ϵĶ��ʹ��

48.��ȡ��ǰĿ¼���ϼ�Ŀ¼·��
os.path.abspath(os.path.join(os.getcwd(), ".."))
os.path.abspath(os.path.join(os.getcwd(), "..\.."))  ���ϼ���Ŀ¼

49.python Windows�������ļ�·������
Windows�µ��ļ�Ŀ¼·��ʹ�÷�б�ܡ�\�����ָ������ǣ��ʹ��������һ����Python�������棬��б�ܡ�\����ת��������硰\n����ʾ�س�����\t����ʾ�Ʊ���ȵȡ�������
���������windowsϰ��ʹ�á�\����ʾ�ļ�·�����ͻ�������塣

����취
:
���������κ�һ����д��ʽ���ɣ�


ʹ��б�ܡ�/��: 
"c:/test.txt"�� 
���÷�б�ܾ�û������������


����б�ܷ���ת�� 
"c:\\test.txt" 
��Ϊ��б����ת���������������\\���ͱ�ʾһ����б�ܷ���


ʹ��Python��raw string 
r"c:\test.txt" 


>>> os.getcwd().replace('\','/')
  File "<stdin>", line 1
    os.getcwd().replace('\','/')
                               ^
SyntaxError: EOL while scanning string literal

����б���滻��б��
>>> os.getcwd().replace('\\','/')
'E:/python/3.6/11/mztestpro'

50. __init__.py������
a.���ļ��е��ɰ�
b.
    ������һ��foo����
foo/
    __init__.py
    foofactories.py
    tallFoos.py
    shortfoos.py
    mediumfoos.py
    santaslittlehelperfoo.py
    superawsomefoo.py
    anotherfoo.py

��init�ű�������д��
__all__ = ['foofactories', 'tallFoos', 'shortfoos', 'medumfoos',
           'santaslittlehelperfoo', 'superawsomefoo', 'anotherfoo']
# deprecated to keep older scripts who import this from breaking
from foo.foofactories import fooFactory
from foo.tallfoos import tallFoo
from foo.shortfoos import shortFoo

�������������ڱ�Ľű���򵥷����д��
from foo import fooFactory, tallFoo, shortFoo

���˴�������
�� from foo import * ��������init��� __all__ ������ע�������ģ�飨���Ƽ���

51.���������ģ���ģ�����ٵ���ģ����������������Ŀ¼��������ģ���

52.python֮�ַ�����ʽ��(format)          ��ͨ��{}��:�����洫ͳ%��ʽ
>>> 'my name is {} ,age {}'.format('hoho',18)
'my name is hoho ,age 18'

53.super
��ǰ��Ͷ��������Ϊsuper�����Ĳ���ʹ�ã����ú������صĶ�����κη������ǵ��ó���ķ����������ǵ�ǰ��ķ���
������Ĺ��캯�������븸��Ĺ��캯�������ã�������಻��д���췽������ֱ��ʹ�ø���Ĺ��췽����
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
                 #������Ĺ��캯�������븸��Ĺ��캯�������ã�������಻��д���췽������ֱ��ʹ�ø���Ĺ��췽����
                 super(SongBird,self).__init__()           #����һ�ַ�����ʹ��Bird.__init__(self)
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


����super(B, self).__init__()���������ģ�super(B, self)�����ҵ�B�ĸ��ࣨ������A����Ȼ�����B�Ķ���selfת��Ϊ��A�Ķ���ͨ��ĳ�ַ�ʽ��һֱû�п�����ʲô��ʽ����������Ȼ�󡰱�ת��������A��������Լ���__init__������

class EditProfileForm(FlaskForm):
    def __init__(self, original_username, *args, **kwargs):
        #super(EditProfileForm, self)�ҵ�EditProfileForm�ĸ���FlaskForm,��EditProfileForm�Ķ���ת��ΪFlaskForm�Ķ������FlaskForm�Ķ�������Լ���__init__����
        super(EditProfileForm, self).__init__(*args, **kwargs)
        self.original_username = original_username

54.���ԣ�property������̬������staticmethod�����෽����classmethod����__str__���÷�
Python���õ�@propertyװ�������Ǹ����һ������������Ե��õ�
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
��һ��getter����������ԣ�ֻ��Ҫ����@property�Ϳ����ˣ���ʱ��@property�����ִ�������һ��װ����@score.setter�������һ��setter����������Ը�ֵ

��̬�������෽����������Ϊ�������Ƶģ�����ʵ����Ҫʹ�ã�Ҳ���ᱨ��.
��̬�����������෽����Ψһ�������Ǿ�̬��������������Ϊ��һ������

��̬��������:
class Foo:
    @staticmethod #װ����
    def spam(x,y,z):
        print(x,y,z)
Foo.spam(1,2,3) #���ú���Ӧ���м��������ʹ���������

�෽������:
class A:
    x=1
    @classmethod
    def test(cls):
        print(cls,cls.x)

class B(A):
    x=2
B.test()

'''
������:
<class '__main__.B'> 2
'''

55.�б�����set���Զ�ȥ�ع���
li=[1,2,3,4,5,1,2,3]
li=list(set(li))
print(li)

56.mysql�����������ݱ���   sqlalchemy.exc.InternalError: (pymysql.err.InternalError) (1366, "Incorrect string value: '\\xE6\\x88\\x91\\xE7\\xAC\\xAC...'
��������mysql���ݿ���ַ�������

�������һ:
�鿴mysqlĳ�����ݿ���ַ������ǰ�װĬ�ϵ�latin1
mysql> show create database flaskblog;
+-----------+----------------------------------------------------------------------+
| Database  | Create Database                                                      |
+-----------+----------------------------------------------------------------------+
| flaskblog | CREATE DATABASE `flaskblog` /*!40100 DEFAULT CHARACTER SET latin1 */ |
+-----------+----------------------------------------------------------------------+

�޸����ݿ���ַ���Ϊutf8(֧������)
mysql> alter database flaskblog character set 'utf8';
Query OK, 1 row affected (0.00 sec)

�ٴβ鿴�����ݿ���ַ���
mysql> show create database flaskblog;
+-----------+--------------------------------------------------------------------+
| Database  | Create Database                                                    |
+-----------+--------------------------------------------------------------------+
| flaskblog | CREATE DATABASE `flaskblog` /*!40100 DEFAULT CHARACTER SET utf8 */ |
+-----------+--------------------------------------------------------------------+

֮ǰ�����ĸÿ��µı��ַ�������latin1
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

��Ҫ�����޸���Щ����ַ���
mysql> alter table user character set 'utf8';
Query OK, 0 rows affected (0.08 sec)

�ٴβ鿴�ñ���ַ����Ѿ��޸ĳ�utf8
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


57.�鿴�ļ��ı���ģʽ
with open(infile,'rb') as f:
        result = chardet.detect(f.read())
        print('result:',result)
58.extend��append
extend��append����������֮�����ڶ��ǽ��½��յ��������õ������б�ĺ��档��extend����ֻ�ܽ���list���Ұ����list�е�ÿ��Ԫ����ӵ�ԭlist�С�

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

59.���flask db migrate ��ⲻ��db.string() ���ȱ仯
�޸�migrations�µ�env.py ��Ӳ���compare_type = True

context.configure(connection=connection,

     target_metadata=target_metadata,

     process_revision_directives=process_revision_directives,

     compare_type = True,   #compare_typeĬ��ΪFalse,��������ݱ仯

     **current_app.extensions['migrate'].configure_args)


��ִ��migrate �����upgrade����Ϳ�����Ч��

60.sys.path���ԡ�
����һ��list.ĬȻ�����python�����ļ�����ģ��Ļ�����������sys.path����ģ���·�������û�еĻ�������ͻᱨ��
��������һ���Լ�д����Ļ�����ð��Լ���ģ��·�����ӵ���ǰģ��ɨ���·����,eg: sys.path.append('���ģ�������'),��������Ͳ���
��Ϊ�Ҳ���ģ�������








 







