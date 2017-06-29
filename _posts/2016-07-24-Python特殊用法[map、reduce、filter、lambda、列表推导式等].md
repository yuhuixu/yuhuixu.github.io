---
layout: post
title: Python特殊用法[map、reduce、filter、lambda、列表推导式等]
category: Python
tags: [Python]
---

## Map函数

原型：map(function, sequence)，作用是将一个列表映射到另一个列表。即对每个元素进行相同操作。

使用方法：

```python
def f(x):
    return x**2
l = range(1,10)
map(f,l)
Out[3]: [1, 4, 9, 16, 25, 36, 49, 64, 81]

```

## Reduce函数 

原型：reduce(function, sequence, startValue)，作用是将一个列表归纳为一个输出。即先对1，2元素进行操作，得到结果与3元素操作，直到最后。

使用方法：

```python
def f2(x,y):
    return x+y
reduce(f1,l)
Out[7]: 45
reduce(f2,l,10)
Out[8]: 55
```

## Filter函数 

原型：filter(function, sequence)，作用是按照所定义的函数过滤掉列表中的一些元素。即对每一个元素都进行函数操作，根据返回的bool值确定元素是否过滤。

使用方法：

```python
def f2(x):
    return x%2 != 0
filter(f2,l)
Out[5]: [1, 3, 5, 7, 9]
```

记住：这里的function必须返回布尔值。

## Lambda函数 

原型：lambda <参数>: 函数体，隐函数，定义一些简单的操作。

使用方法：


```python
f3 = lambda x: x**2
f3(2)
Out[10]: 4
```

还可以结合map、reduce、filter来使用，如：
map(f3,l)
Out[11]: [1, 4, 9, 16, 25, 36, 49, 64, 81]

## 字典设置默认值

python字典中设置条目默认值在有些时候非常有用，例如初始化一个字典的时候。

使用方法：

```python
x = {}
x.setdefault(1,0)
Out[15]: 0
x[2] = 10
x
Out[17]: {1: 0, 2: 10}
x.setdefault(2,1)
Out[18]: 10
```

## 列表推导式

基本形式：`[x for item in sequence <if (conditions)>],` 这里x表示对item的操作。

使用方法：

```python
[i**2 for i in l]
Out[12]: [1, 4, 9, 16, 25, 36, 49, 64, 81]
```
