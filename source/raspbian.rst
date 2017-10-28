===================
Raspbian 源使用帮助
===================

镜像说明
========

Raspbian 是为树莓派设计，基于 Debian 7.0/wheezy 的操作系统。

其不隶属于树莓派基金会，但被列为官方支持的操作系统。

地址
====

https://mirrors.scau.edu.cn/raspbian/


收录架构
========

armhf

收录版本
========

wheezy，jessie


使用说明
========

先用以下命令备份 ``/etc/apt/sources.list`` 文件内容：

::
  
  sudo mv /etc/apt/sources.list /etc/apt/sources.list.bak

新建 ``/etc/apt/sources.list`` 文件，并根据版本加入对应内容：

**Debian 8 jessie**

::
  
  deb http://mirrors.scau.edu.cn/raspbian/raspbian/ jessie main non-free contrib
  deb-src http://mirrors.scau.edu.cn/raspbian/raspbian/ jessie main non-free contrib

**Debian 7 wheezy**

::
  
  deb http://mirrors.scau.edu.cn/raspbian/raspbian/ wheezy main non-free contrib
  deb-src http://mirrors.scau.edu.cn/raspbian/raspbian/ wheezy main non-free contrib

最后执行 ``sudo apt-get update`` 更新软件源
