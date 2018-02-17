
## **bytes**类型的数据用'b'前缀的单引号或双引号表示


```python
x = b'ABC'
x
```




    b'ABC'




```python
'ABC'.encode('ascii')
```




    b'ABC'




```python
'中文'.encode('utf-8')
```




    b'\xe4\xb8\xad\xe6\x96\x87'




```python
'ABC'.encode('utf-8')
```




    b'ABC'




```python
x.decode('ascii')
```




    'ABC'




```python
x.decode('utf-8')
```




    'ABC'




```python
b'\xe4\xb8\xad\xe6\x96\x87'.decode('utf-8')
```




    '中文'



## len()函数计算**str**的字符数，或者字节数


```python
len(x)
```




    3




```python
len(b'\xe4\xb8\xad\xe6\x96\x87')
```




    6




```python
len('中文'.encode('utf-8'))
```




    6



## 格式化输出


```python
'hello, %s' %'world'
```




    'hello, world'




```python
'hello, %s, you have $%d' %('Tom', 100000)
```




    'hello, Tom, you have $100000'



### %s表示字符串替换，%d表示整数替换，有几个%?占位符，后面就有几个变量或者值，顺序一一对应

|         |        |
|-------------|------------|
|   %d     |   整数   |
|   %f     |  浮点数   |
|   %s     |  字符串   |
|   %x     | 十六进制整数|


```python
'%2d-%02d' %(3, 1)
```




    ' 3-01'




```python
'%.2f' % 3.1415926
```




    '3.14'



### 不确定用什么用%s，会转化为字符串


```python
'Age: %s. Gender: %s' % (25, 'male')
```




    'Age: 25. Gender: male'




```python
# 两个%表示一个%
'growth rate: %d%%' % 7
```




    'growth rate: 7%'



## format()，传入参数依次替换字符串内占位符{0}、{1}......


```python
'Hello, {0}, 成绩提升了{1: .1f}%'.format('Tom', 14.78)
```




    'Hello, Tom, 成绩提升了 14.8%'




```python
s1 = 72
s2 = 85
r = (s2 - s1)/s1
'Congratulations, your score increase %.2f%% rate' % (r*100)
```




    'Congratulations, your score increase 18.06% rate'




```python
'Congratulations, your score increase {0: .2f}% rate'.format(r*100)
```




    'Congratulations, your score increase  18.06% rate'


