# GPU版本的TensorFlow安装

pip install tensorflow-gpu==1.8.0

1、安装cuda，网址为：https://developer.nvidia.com/cuda-downloads
可参考教程：https://blog.csdn.net/Mr_xuexi/article/details/88815107

2、cuda安装之后，因为版本不匹配问题，重启后发现ubuntu系统进不到图形界面，于是删除cuda-10.0，参考网址为：

https://blog.csdn.net/ALDNOAH_ZERO/article/details/81235863

虚拟机系统里的显卡是软件模拟的，与宿主显卡设备没有关系，所以在这里不使用GPU加速。

3、使用pip安装TensorFlow，
详情参考安装TensorFlow:https://blog.csdn.net/shuzfan/article/details/78516542

pip install tensorflow

测试是否安装成功：

import tensorflow as tf

hello = tf.constant('Hello, TensorFlow!')

sess = tf.Session()

print(sess.run(hello))

4、安装pycharm开发工具，启动命令：sudo sh pycharm/bin/pycharm.sh

5、进行测试，结果如下：
![TensorFlow](https://github.com/EnernityTwinkle/Tutorial-Summarization/blob/master/python-config/images/tensorflow1.png)
 
6、进行案例测试，参考案例实践:https://blog.csdn.net/cs_hnu_scw/article/details/79695347。

TensorFlow相关概念：

Variable，是变量的意思，一般用来表示图中的各计算参数，包括矩阵，向量等，Variable必须初始化以后才有具体的值。

Placeholder又叫占位符，是一个抽象的概念。表示这里有一个值/向量/矩阵，现在我没有给定具体数值，不过在正式运行的时候会补上。


