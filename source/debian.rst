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

有关发行版信息可以查看 Debian 官网：https://www.archlinux.org/


使用说明
========


可以运用如下命令备份 ``/etc/apt/sources.list`` 文件：

::

  sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak

一般情况下，将 :file:`/etc/apt/sources.list` 文件中 Debian 默认的源地址 ``http://httpredir.debian.org/``
替换为 ``http://mirrors.scau.edu.cn`` 即可

可以使用如下命令进行替换：

::

  sudo sed -i 's/httpredir.debian.org/mirrors.scau.edu.cn/g' /etc/apt/sources.list

替换后执行 ``sudo apt-get update`` 更新软件源列表

相关链接
========

:官方主页: https://www.debian.org/
:邮件列表: https://www.debian.org/MailingLists/
:Wiki: https://wiki.debian.org/
:文档: https://www.debian.org/doc/
:镜像列表: https://www.debian.org/mirror/list
