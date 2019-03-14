一、Windows系统下安装Anaconda

1.1 在官网https://www.anaconda.com/distribution/ 上下载Anaconda，这里我选择的是Python2.7版本的,下载完成后按照指示正常安装即可

1.2 安装成功后，在已安装程序中找到Anaconda Prompt，进入Anaconda Prompt，正常测试如下：
![Anaconda](https://github.com/EnernityTwinkle/Tutorial-Summarization/blob/master/python-config/images/Anaconda1.png)

二、linux服务器安装anaconda:

参考网址：https://www.cnblogs.com/andylhc/p/9513504.html

2.1 下载安装脚本：

wget https://repo.anaconda.com/archive/Anaconda3-5.2.0-Linux-x86_64.sh

2.2 运行安装向导：

bash Anaconda3-5.2.0-Linux-x86_64.sh

2.3 确认是否安装成功：（需要重新启动终端）

conda –version


三、使用Anaconda管理多个版本的python环境参考网址：https://jingyan.baidu.com/album/22a299b5e6e4909e18376a4b.html?picindex=2

示例：现在，我想添加一个Python2.7的环境，执行命令：conda create --name python27 python=2.7，命令中我制定了环境名称是python27，指定了Python版本是2.7，执行命令后，Conda会自动下载最新版的Python2.7，并自动部署。

•	更改默认环境python版本：download the latest version of Anaconda and run the following command to install Python 3.5 (or 3.6) in the root environment: conda install python=3.5

or conda install python=3.6


此时，再次查看你的系统当前已有的Python环境，执行命令：conda info --envs，从图中我们看到，这里多了一个名字为python27的Python环境

查看我们当前使用的Python版本，执行命令：python --version，从图中看到当前的Python环境是3.6版本

切换Python环境到刚才新添加的Python2.7，执行命令：activate python27，然后执行命令：python --version，查看是否切换成功

在Python27环境下，完成工作后，切回原来的Python环境，执行命令：deactivate python27

如果刚才添加的Python27环境，不再使用，可通过执行命令：conda remove --name python27 --all，进行删除。

注：在使用命令activate py27切换Python2的时候出现的权限问题：

命令更改为：source/conda activate py27即可。


更换pip源：

1、在windows文件管理器中,输入 %APPDATA%

2、在该目录下新建pip文件夹，然后到pip文件夹里面去新建个pip.ini文件

3、在新建的pip.ini文件中输入以下内容

[global]

timeout = 6000

index-url = http://pypi.douban.com/simple

trusted-host = pypi.douban.com


Linux更换pip源：

cd $HOME  

mkdir .pip  

cd .pip

sudo vim pip.conf  



在里面添加  

[global]  

index-url=https://pypi.tuna.tsinghua.edu.cn/simple

[install]  

trusted-host=pypi.tuna.tsinghua.edu.cn 

disable-pip-version-check = true  

timeout = 6000 

 
更换conda源：

1、在cmd下输入：conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/

2、在cmd下输入：conda config --set show_channel_urls yes

#好了，这次可以开心的下载东西了

# 如何删除添加的源呢？

# conda config --remove channels 'https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/' 

# 看看当前的 cofig 是什么样的

conda config --show



notebook远程无法访问解决方案：

https://blog.csdn.net/du_qi/article/details/51427857


