```
姓名：杨子旭
班级：16-5
学号:2016011533
```

本次作业的主要问题

1. 除法函数divide()没办法用，改为truediv()可正常使用

数学运算函数参考：[传送门](https://blog.csdn.net/zywvvd/article/details/78593618?utm_source=blogxgwz0)

```python
#在一个notebook文件中构建一张图，实现两个数的加法操作，并在两个不同的会话中执行图。
import tensorflow as tf
import math as mt
with tf.Graph().as_default() as g:
    a=tf.constant(2)
    b=tf.constant(3)
    c=tf.add(a,b)
with tf.Session(graph=g) as sess1:
    print(sess1.run(c))
with tf.Session(graph=g) as sess2:
    print(sess2.run(c))
#查找资料学习TensorFlow中执行常量基本运算API的基本用法，如`tf.add`、`tf.subtract`、`tf.multiply`、`tf.divide`、`tf.mod`、`tf.pow`、`tf.square`、`tf.sqrt`等的用法，并在notebook中演示其基本用法

with tf.Graph().as_default() as g2:
    a=tf.subtract(5,3) # 5-3减法运算
    b=tf.multiply(5,3) # 5*3乘法运算
    c=tf.truediv(6,2)   # 6/2除法运算
    d=tf.mod(6,4)      # 6%4取模运算
    e=tf.abs(-5)       # |5|取绝对值
    f=tf.negative(5)   #  -5 取负操作
    g=tf.round(1.4)    #1 四舍五入
    h=tf.pow(2,3)      #幂次方
    j=tf.square(4)     #平方
    k=tf.sqrt(4.0)     #开根号 必须传入浮点数或复数
    l=tf.exp(2.0)        #e的次方
    m=tf.log(tf.exp(1.0))   #以 e 为底，必须传入浮点数或复数
    n=tf.ceil(2.1)     #3 向上取整
    o=tf.floor(2.9)    #2 向下取整
    p=tf.maximum(2,3)  #返回最大值
    q=tf.minimum(2,3)  #返回最小值
    r=tf.cos(mt.pi)    #cos函数
    s=tf.sin(mt.pi)    #sin函数
    t=tf.tan(mt.pi)    #tan函数
with tf.Session(graph=g2) as sess:
    print(sess.run([a,b,c,d,e,f,g,h,j,k,l,m,n,o,p,q,r,s,t]))
```

