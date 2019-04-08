### 1.使用Anaconda安装指定版本的pytorch:

conda install pytorch=0.4.0 -c soumith

#使用pip安装指定版本

pip install pytorch==0.4.0

如何查看当前pytorch版本:

import torch

print(torch.__version__)

ps:如果上面方法出错，可以先从开源软件镜像上（https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/win-64/） 
下载对应版本的文件（网址是win-64的），然后输入下面的命令：
```
conda install numpy mkl cffi
conda install --offline pytorch-1.0.1-py3.7_cuda100_cudnn7_1.tar.bz2
```
另外，也可以参考pytorch官网方法安装：https://pytorch.org/get-started/locally/

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




