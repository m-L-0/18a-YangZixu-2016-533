```
'''
    姓名:杨子旭
    年级:16-5
    学号:2016011533
'''
```

作业没什么问题

```python
import tensorflow as tf
with tf.Graph().as_default() as g2:
    w1=tf.Variable(2.5)
    w2=tf.Variable(3.6)
    b=tf.Variable(1.0)
    x=tf.placeholder(dtype=tf.float32,shape=[])
    y=tf.placeholder(dtype=tf.float32,shape=[])
    z=tf.add(tf.add(tf.multiply(w1,x),tf.multiply(w2,y)),b)
with tf.Session(graph= g2) as sess2:
    #sess2.run(tf.variables_initializer([w1, w2,b]))
    #print(w1,w2)
    sess2.run(tf.global_variables_initializer())
    print(sess2.run(z,feed_dict={x:3.5,y:4.2}))
```

