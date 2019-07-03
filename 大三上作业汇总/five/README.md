```
'''
    姓名:杨子旭
    年级:16-5
    学号:2016011533
'''
```

本次作业没遇到什么大问题

本次代码

```python
import tensorflow as tf
'''
设计一个函数，要求输入两个`shape、dtype`一样的张量，
输出一个同样`shape、dtype`的张量，
并且输出的张量中的元素的每一个值都是输入的两个张量中对应元素最大的。
即模拟`tf.maximum`的功能，但不能直接使用此函数。
'''
def Maxnum(ts1,ts2):
    res=tf.stack([ts1,ts2],axis=0)
    tmp=tf.reduce_max(res,reduction_indices=0)
    return tmp
a=tf.constant([1,7,3])
b=tf.constant([4,5,2])
ans=Maxnum(a,b)
with tf.Session() as sess:
    print(sess.run(ans))
```

```python
c=tf.maximum(a,b)
d=tf.minimum(a,b)
with tf.Session() as sess:
    print(sess.run(c))
    print(sess.run(d))
```

```python
'''
    了解`TensorArray`的基本用法，并尝试配合`tf.while_loop`配合使用
'''
def cond(idx,opt):
    return tf.less(idx,5)
def body(idx,opt):
    opt=opt.write(idx,[1.2,3.4])
    idx+=1
    return idx,opt

opt=tf.TensorArray(dtype=tf.float32,size=1,dynamic_size=True)
idx=tf.constant(0)
t,res=tf.while_loop(cond,body,[idx,opt])
with tf.Session() as sess:
    print(sess.run(res.stack()))
```

