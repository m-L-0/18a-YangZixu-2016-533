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
X=tf.placeholder(tf.float32)

with tf.variable_scope('abc',reuse=tf.AUTO_REUSE) as scope:
    w=tf.get_variable('w',initializer=tf.random_normal_initializer(mean=0.0, stddev=1.0, seed=None, dtype=tf.float32),shape=[1],dtype=tf.float32)
    b=tf.get_variable('b',initializer=tf.random_normal_initializer(mean=0.0, stddev=1.0, seed=None, dtype=tf.float32),shape=[1],dtype=tf.float32)
    yp=tf.nn.sigmoid(tf.add(tf.multiply(X,tf.get_variable('w')),tf.get_variable('b')))

with tf.Session() as sess:
    sess.run(tf.global_variables_initializer())
    print(sess.run(yp,feed_dict={X:1.5}))
```

