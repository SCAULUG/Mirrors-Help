===================
Raspbian 源使用帮助
===================

镜像说明
========

Raspbian 是为树莓派设计，基于 Debian 7.0/wheezy 的操作系统。

其不隶属于树莓派基金会，但被列为官方支持的操作系统，推荐用于树莓派的首选系统。

地址
====

https://mirrors.scau.edu.cn/raspbian/


收录架构
========

armhf

收录版本
========

wheezy，jessie，stretch


使用说明
========

由于镜像站强制使用https,需要提前安装 ``apt-transport-https`` 

先用以下命令备份 ``/etc/apt/sources.list`` 文件内容：

::
  
  sudo mv /etc/apt/sources.list /etc/apt/sources.list.bak

新建 ``/etc/apt/sources.list`` 文件，并根据版本加入对应内容：

**Debian 9 stretch**

::
  
  deb https://mirrors.scau.edu.cn/raspbian/raspbian/ stretch main non-free contrib
  deb-src https://mirrors.scau.edu.cn/raspbian/raspbian/ stretch main non-free contrib
  
**Debian 8 jessie**

::
  
  deb https://mirrors.scau.edu.cn/raspbian/raspbian/ jessie main non-free contrib
  deb-src https://mirrors.scau.edu.cn/raspbian/raspbian/ jessie main non-free contrib

**Debian 7 wheezy**

::
  
  deb https://mirrors.scau.edu.cn/raspbian/raspbian/ wheezy main non-free contrib
  deb-src https://mirrors.scau.edu.cn/raspbian/raspbian/ wheezy main non-free contrib

最后执行 ``sudo apt-get update`` 更新软件源

同时也需要更改 archive.raspberrypi.org 源

Raspberrypi 源使用帮助
======================

先用以下命令备份 ``/etc/apt/sources.list.d/raspi.list`` 文件内容：

::
  
  sudo mv /etc/apt/sources.list.d/raspi.list /etc/apt/sources.list.d/raspi.list.bak

新建 ``/etc/apt/sources.list.d/raspi.list`` 文件，并根据版本加入对应内容：

**Debian 9 stretch**

::
  
  deb https://mirrors.scau.edu.cn/raspberrypi/ stretch main
  deb-src https://mirrors.scau.edu.cn/raspberrypi/ stretch main
  
**Debian 8 jessie**

::
  
  deb https://mirrors.scau.edu.cn/raspberrypi/ jessie main
  deb-src https://mirrors.scau.edu.cn/raspberrypi/ jessie main

**Debian 7 wheezy**

::
  
  deb https://mirrors.scau.edu.cn/raspberrypi/ wheezy main
  deb-src https://mirrors.scau.edu.cn/raspberrypi/ wheezy main

最后执行 ``sudo apt-get update`` 更新软件源
