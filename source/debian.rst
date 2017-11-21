=================
Debian 源使用帮助
=================

地址
====

https://mirrors.scau.edu.cn/debian/


收录架构
========

Debian 支持的所有架构，如 AMD64 (x86_64), Intel x86, ARM, MIPS, ppc64el, s390x 等


收录版本
========

Debian Old Stable, Stable(稳定版), Testing(测试版), Unstable(不稳定版)

当前 Stable 为 Debian 9，代号为 Stretch。
当前的”测试版“版本代号是 buster。
”不稳定版“的版本代号永远都被称为 sid。

有关发行版信息可以查看 Debian 官网说明：https://www.debian.org/releases/index.zh-tw.html


使用说明
========

如果还没有安装 ``apt-transport-https`` ，请先用如下命令安装:

::

  sudo apt-get install apt-transport-https


之后，可以运用如下命令备份 ``/etc/apt/sources.list`` 文件：

::

  sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak

一般情况下，将 :file:`/etc/apt/sources.list` 文件中 Debian 默认的源地址 ``http://deb.debian.org/``
替换为 ``https://mirrors.scau.edu.cn`` 即可

可以使用如下命令进行替换：

::

  sudo sed -i 's/deb.debian.org/mirrors.scau.edu.cn/g' /etc/apt/sources.list

也可以直接编辑 :file:`/etc/apt/sources.list` 文件（需要使用 sudo）。以下是 Debian Stable 参考配置内容：

::

    deb https://mirrors.scau.edu.cn/debian stable main contrib non-free
    # deb-src https://mirrors.scau.edu.cn/debian stable main contrib non-free
    
    deb https://mirrors.scau.edu.cn/debian stable-updates main contrib non-free
    # deb-src https://mirrors.scau.edu.cn/debian stable-updates main contrib non-free

    # deb https://mirrors.scau.edu.cn/debian stable-proposed-updates main contrib non-free
    # deb-src https://mirrors.scau.edu.cn/debian stable-proposed-updates main contrib non-free

替换后执行 ``sudo apt-get update`` 更新软件源列表


相关链接
========

:官方主页: https://www.debian.org/
:邮件列表: https://www.debian.org/MailingLists/
:Wiki: https://wiki.debian.org/
:文档: https://www.debian.org/doc/
:镜像列表: https://www.debian.org/mirror/list
