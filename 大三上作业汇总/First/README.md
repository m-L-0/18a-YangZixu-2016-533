## 这是我的第一次作业提交

```
姓名：杨子旭
班级：16-5
学号：2016011533
```

1. 作业中遇到的主要问题
   1. 第三个问题我不知道想表达什么意思
2. 下边是代码和文字介绍(源代码在另一个文件里)

```python
import tensorflow as tf
img=[1,2,3]*tf.ones(shape=[10,28,28,3])
#1. 如何利用索引取出第2张图片？（注意：索引均从0开始，第二张则索引为1，下同）
fir=img[1:2,:,:,:]
#2.如何利用切片取出第2张图片？
sec=tf.slice(img,[1,0,0,0],[1,28,28,3])
#3. 使用切片与使用索引取出的一张图片有何不同？
    #我认为没什么不同
#4 如何取出其中的第1、3、5、7张图片？
fou=img[0:7:2,:,:,:]
#5 如何取出第6-8张（包括6不包括8）图片中中心区域（14*14）的部分？
fiv=img[5:7,7:21,7:21,:]
#6 如何将图片根据通道拆分成三份单通道图片？
six1=sec[:,:,:,0]
six2=sec[:,:,:,1]
six3=sec[:,:,:,2]
#7写出`tf.shape(img)`返回的张量的阶数以及`shape`属性的值。
sev=tf.shape(img)
#阶数：4， shape属性值：[10 28 28 3]
#这里可以看效果
with tf.Session() as se3:
    #print(se3.run(img))
    #print(se3.run(sec))
    print('***********************')
    #print(se3.run(fir))
    #print(se3.run(fou).shape)
    #print(se3.run(fiv).shape)
    #123456789 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28
    #print(se3.run(six))
    #print(se3.run([six1,six2,six3]))
    #print(se3.run(sev))
```

3.

