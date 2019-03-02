1、查看内核/操作系统/CPU信息	uname -a
2、查看操作系统版本	cat head -n 1 /etc/issue
3、查看内存大小	cat /proc/meminfo | grep MemTotal
4、查看硬盘大小	fdisk -l | grep Disk
5、查看CPU信息	cat /proc/cpuinfo |grep "model name"
6、查看GPU信息
如果是NVIDIA显卡，可以使用nvidia-smi命令，
一般方法为查看lspci| grep -i vga，然后进一步查看具体信息
 
