1.使用Anaconda安装指定版本的pytorch:

conda install pytorch=0.4.0 -c soumith

#使用pip安装指定版本

pip install pytorch==0.4.0

如何查看当前pytorch版本:

import torch

print(torch.__version__)

2、安装torchtext(version 0.2.3)

用conda安装出现PackageNotFoundError，

![pytorch](https://github.com/EnernityTwinkle/Tutorial-Summarization/blob/master/python-config/images/torch1.png)
      
 
使用网上说的anaconda search查找到相关包后重新安装，发现出现同样的错误：
 ![pytorch](https://github.com/EnernityTwinkle/Tutorial-Summarization/blob/master/python-config/images/torch2.png)
 
改用pip install torchtext==0.2.3后成功：
![pytorch](https://github.com/EnernityTwinkle/Tutorial-Summarization/blob/master/python-config/images/torch3.png)
 
3、安装NLTK

conda install NLTK

安装nltk data，参考：

https://jingyan.baidu.com/article/295430f1e0b3b20c7f005064.html

4、安装docker

pip install docker

1.以服务的方式启动docker守护进程：

start docker //启动

stop docker //停止

status docker //查看状态

2.利用docker daemon命令

docker daemon




