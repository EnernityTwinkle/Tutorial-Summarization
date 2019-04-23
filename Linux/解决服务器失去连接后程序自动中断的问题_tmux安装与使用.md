参考网址：https://www.jianshu.com/p/48b5b61e1c38
基本命令参考网址：https://www.cnblogs.com/lizhang4/p/7325086.html

# 基本使用命令

1、输入‘tmux’进入，或者‘tmux new -s SessionName’进入有名称的会话

2、ctrl+b d （松开ctrl+b后再按d）脱离当前会话，回到shell的终端环境

3、tmux ls 终端环境查看会话列表

4、tmux attach 返回会话

5、tmux a -t session1 从终端环境返回指定会话

6、ctrl+b &关闭当前窗口

7、ctrl+b s选择并切换会话；在同时开启了多个会话时使用

使用脚本：

#!/bin/bash


#Script for installing tmux on systems where you don't have root access.

#tmux will be installed in $HOME/local/bin.

#It's assumed that wget and a C/C++ compiler are installed.


#exit on error

set -e



#create our directories

mkdir -p $HOME/local $HOME/tmux_tmp

cd $HOME/tmux_tmp


#download source files for tmux, libevent, and ncurses


#extract files, configure, and compile


############

#libevent #

############

tar xvzf libevent-2.0.19-stable.tar.gz

cd libevent-2.0.19-stable

./configure --prefix=$HOME/local --disable-shared

make

make install

cd ..



############

#ncurses  #

############

tar xvzf ncurses-5.9.tar.gz

cd ncurses-5.9

./configure --prefix=$HOME/local

make

make install

cd ..



############

#tmux     #

############

cd tmux

./configure CFLAGS="-I$HOME/local/include -I$HOME/local/include/ncurses" LDFLAGS="-L$HOME/local/lib -L$HOME/local/include/ncurses -L$HOME/local/include"

CPPFLAGS="-I$HOME/local/include -I$HOME/local/include/ncurses" LDFLAGS="-static -L$HOME/local/include -L$HOME/local/include/ncurses -L$HOME/local/lib" make

cp tmux $HOME/local/bin

cd ..



#cleanup

rm -rf $HOME/tmux_tmp



echo "$HOME/local/bin/tmux is now available. You can optionally add $HOME/local/bin to your PATH."


