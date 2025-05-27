快捷键

1、打开终端 ctrl+alt+t

2、推出鼠标ctrl+command

3、tar -zxvf filename 解压缩

4、cd 进入指定的目录

cd .. 返回上一级目录

5、ls 查看当前目录下的所有的目录与文件名

6、touch filename 表示创建一个文件

7、mkdir dirname 表示创建一个目录

8、rm filename 表示删除一个文件

rm -rf dirname 表示删除该目录及其所有的子级目录一起删掉

rm -rf */

9、 rmdir dirname 表示删除一个空目录

10、help 帮助命令，查看命令的用法

命令 --help

11、ctrl+c 强制终止，不会终止进程

12、ctrl+z 强制终止，终止进程

13、clear 清楚命令行终端中的内容

14、ctrl+l 快捷键，快速清除终端中的内容

15、sudo 以管理员身份运行上一个命令

16、source /opt/ros/indigo/setup.bash 使环境设置文件生效source

17、ifconfig 查看IP地址等信息

18、ubuntu下软件安装：apt-get install 应用名 （老版本）

apt install 应用名

19、root文件夹不能复制文件

1）用root账号登陆

2）chmod 777 文件夹 让当前用户访问root文件夹，具有读写权限

3）cp -r /home/id/pc /root/catkin_ws

20、创建软链接命令

sudo ln -s 文件绝对路径 目的地址

  

系统信息命令

1、lshw： 查看硬件信息

2、lscpu：查看cpu信息

3、lsusb：查看usb信息

4、uname： 查看当前系统名

uname -a : 查看当前系统的所有信息

5、arch：查看系统的架构 x86 表示32位 x86_64表示64位

6、df： 查看磁盘空间

df -h ： 可以直观的查看磁盘的空间..

7、date：查看当前的时间

8、cal：查看当月日历

9、hostname： 显示主机名

10、who： 查看当前用户信息

11、free： 查看当前内存的使用情况

free -h 可以直观的查看当前的内存使用情况

12、ps: 查看当前文件的进程 进程号

13、 kill：杀死

kill 进程号 杀死一个进程

14、top：根据消耗的资源,从上之下排序

15、ifconfig ： 查看网络情况

16、ping： 测试网络连通

17、netstat ： 显示网络状态信息

18、clear ： 清屏

  

系统目录

1、cd / : 进入根目录

2、bin：可执行的二进制文件，通常放的是系统自带的文件

3、dev：Device，设备，通常系统的硬件被抽象成一个文件存放在dev中

4、initrd.img：开机启动时的图片

5、lost+found：异常关机时存放错误信息的文件

6、opt：Options，存放开发者自己开发并安装的软件

7、run：系统运行时需要的文件

8、srv：存放服务启动后需要访问的文件数据

9、usr：存放与用户直接相关的文件目录

10、boot：启动配置文件，启动时需要的核心文件

11、etc：配置文件（系统中各种所需要的配置文件）

12、lib、lib64：库，系统内置的库文件，自己安装的各种软件的动态或静态的链接，windows中的dll很相似。

13、media：媒体，存放是系统外接设备，如U盘，硬盘

14、proc：系统文件

15、sbin：系统管理员特用的二进制文件（root用户）

16、sys：系统文件

17、var：存放日志信息（启动日志，软件日志）

18、cdrom：挂载入口

18、home：家，每个用户都会在home目录下有一个自己的文件夹，这个文件夹的名称与用户名一致

19、mnt：挂载点，临时安装的挂载

20、root：超级管理员的目录

21、snap：全新的管理软件包的方式

22、tmp：临时文件

  

使用超级管理员帐户 root

0.安装的系统的时候,没有设置root密码

1.切换到root用户

su

输入密码

2.设置root 密码

sudo passwd root

需要重复2次输入

3.exit:退出root账号

4.切换账号

su 用户名

切换到对应用户,

如果不写用户名,默认切换到root用户

5.修改用户的密码

passwd 用户名

如果不写用户名,默认是当前用户

  

基础命令

0.Linux的基础命令

ls 列出当前目录下的文件

ls -a 列出当前目录下的所有文件，包括隐藏的文件

mkdir dir 创建名为dir的文件目录

touch 创建空文件

cd dir 进入目录change directory

cd . 当前目录

cd .. 进入父目录

pwd 打印当前的绝对路径

cd~ 家目录

cp 复制

mv file1 file2 移动文件或者改变名字

rm 移除目录

rmdir 移除目录

find 在文件系统中搜索某文件

tree 树形结构显示目录，需要安装tree包

ln 创建链接文件

clear 清屏

1.find 命令 查找一个文件

例: find -name 文件名 表示在当前目录下查找指定文件位置

例: find 路径 -name 文件名 表示在指定目录下查找指定文件位置

2.查看文件的类型

file 文件名/目录名

3.linux中的文本编辑

linux 默认自带 vi, 升级版 vim。简单编辑器为gedit

4.软件的安装分类

命令行形式的安装 apt install 应用名

用可执行文件安装 .deb 文件

原码安装

5.打包/解包 压缩/解压缩

打包

tar -cvf 打包后的文件名 目录名 默认将打包后的文件放在当前目录下

例2:tar -cvf yy.tar yy

解包

tar -xvf 已经打包的文件 表示在当前目录下解包

tar -xvf 已经打包的文件 -C 指定目录 表示在指定目录下解包

压缩

tar -zcvf 压缩后的文件名 目录名

-z或--gzip或--ungzip：通过gzip指令处理备份文件；

例: tar -zcvf yy.tar.gz yy

解压缩

tar -zxvf 已经压缩的文件 表示在当前目录下解压

tar -zxvf 已经压缩的文件 -C 指定目录 表示在指定目录下解压

6. 关机或重启命令

poweroff: 立即关机

shutdown -h now : 立即关机

shutdown -h +5: 5分钟之后自动关机

shutdown -c : 取消自动关机

reboot: 重启

shutdown -r now: 重启

7.Linux软件包管理

dpkg 管理工具，软件包名以.deb后缀。

比如安装tree命令的安装包，先将tree.deb传到Linux系统中，再使用命令。

sudo dpkg -i tree_1.5.3-1_i386.deb 安装软件

sudo dpkg -r tree 卸载软件

APT高级软件工具，适合系统能够连接互联网，以tree为例。

sudo apt-get install tree 安装tree

sudo apt-get remove tree 卸载tree

sudo apt-get update 更新软件

sudo apt-get upgrade

8. 更改权限

sudo chmod [u所属用户 g所属组 o其他用户 a所有用户] [+增加权限 -减少权限] [r w x] 目录名

例如：有一个文件filename，权限为“-rw-r----x” ,将权限值改"-rwxrw-r-x"，用数值表示为765

sudo chmod u+x g+w o+r filename

用数值表示sudo chmod 765 filename

完全权限：sudo chmod 777 -R filename

9.设置Linux服务器用户权限

　　添加用户:adduser 用户名

　　设置密码:passwd 用户名

10. vim使用

vim三种模式：命令模式、插入模式、编辑模式。使用ESC或i或：来切换模式。

命令模式下：

:q 退出

:q! 强制退出

:wq 保存并退出

:set number 显示行号

:set nonumber 隐藏行号

yyp 复制光标所在行，并粘贴