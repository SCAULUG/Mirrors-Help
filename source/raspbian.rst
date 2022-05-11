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

* stretch (oldoldstable)
* buster (oldstable)
* bullseye (stable)
* bookworm (testing)


使用说明
========

由于镜像站强制使用https，需要提前安装 ``apt-transport-https`` 

先用以下命令备份 ``/etc/apt/sources.list`` 文件内容：

::

  sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak

将 :file:`/etc/apt/sources.list` 文件中默认的源地址 ``http://raspbian.raspberrypi.org/`` 替换为 ``https://mirrors.scau.edu.cn/raspbian/`` 即可。

raspbian 2018-04-19 之后的镜像默认源已经更改，用如下命令替换：

::

  sudo sed -i 's|http://raspbian.raspberrypi.org|https://mirrors.scau.edu.cn/raspbian|g' /etc/apt/sources.list

旧版的系统可以用以下命令替换：

::

  sudo sed -i 's|http://mirrordirector.raspbian.org|https://mirrors.scau.edu.cn/raspbian|g' /etc/apt/sources.list
  sudo sed -i 's|http://archive.raspbian.org|https://mirrors.scau.edu.cn/raspbian|g' /etc/apt/sources.list


当然也可以直接编辑 :file:`/etc/apt/sources.list` 文件（需要使用 sudo）。删除原文件所有内容，用以下内容取代：

**Debian 11 bullseye**

::

    deb https://mirrors.scau.edu.cn/raspbian/raspbian/ bullseye main non-free contrib rpi
    # deb-src https://mirrors.scau.edu.cn/raspbian/raspbian/ bullseye main non-free contrib rpi

**Debian 10 buster**

::
  
  deb https://mirrors.scau.edu.cn/raspbian/raspbian/ buster main non-free contrib rpi
  deb-src https://mirrors.scau.edu.cn/raspbian/raspbian/ buster main non-free contrib rpi

**Debian 9 stretch**

::
  
  deb https://mirrors.scau.edu.cn/raspbian/raspbian/ stretch main non-free contrib rpi
  deb-src https://mirrors.scau.edu.cn/raspbian/raspbian/ stretch main non-free contrib rpi

最后执行 ``sudo apt-get update`` 更新软件源

同时也需要更改 archive.raspberrypi.org 源，请参考本帮助文档下方的 Raspberrypi 源使用帮助

相关链接
========

Raspbian 链接
  :Raspbian 主页: http://www.raspbian.org/
  :文档: http://www.raspbian.org/RaspbianDocumentation
  :Bug Tracker: http://www.raspbian.org/RaspbianBugs
  :镜像列表: http://www.raspbian.org/RaspbianMirrors

树莓派链接
  :树莓派基金会主页: https://www.raspberrypi.org/
  :树莓派基金会论坛 Raspberry Pi OS 版块: https://www.raspberrypi.org/forums/viewforum.php?f=66


======================
Raspberrypi 源使用帮助
======================

镜像说明
========

树莓派的 archive.raspberrypi.org 软件源，也即 ``/etc/apt/sources.list.d/raspi.list`` ，

是由树莓派基金会提供的软件源，包括 ui 相关程序（如 Raspbian 的桌面环境 PIXEL DE）及部分由树莓派基金会为树莓派编写的软件，通常与 ``archive.raspbian.org`` （参考 Raspbian 源使用帮助）一起使用。

地址
====

https://mirrors.scau.edu.cn/raspberrypi/

收录架构
========

* armhf
* arm64
* x86
* x86_64

收录版本
========

* wheezy
* jessie
* stretch
* buster
* bullseye

使用说明
========

由于镜像站强制使用https，需要提前安装 ``apt-transport-https`` 

先用以下命令备份 ``/etc/apt/sources.list.d/raspi.list`` 文件：

::

  sudo cp /etc/apt/sources.list.d/raspi.list /etc/apt/sources.list.d/raspi.list.bak

一般情况下，将 :file:`/etc/apt/sources.list.d/raspi.list` 文件中默认的源地址 ``http://archive.raspberrypi.org/`` 替换为 ``https://mirrors.scau.edu.cn/raspberrypi/`` 即可。

可以使用如下命令：

::

    sudo sed -i 's|http://archive.raspberrypi.org|https://mirrors.scau.edu.cn/raspberrypi|g' /etc/apt/sources.list.d/raspi.list

当然也可以直接编辑 :file:`/etc/apt/sources.list.d/raspi.list` 文件（需要使用 sudo）。删除原文件所有内容，用以下内容取代：

**Debian 11 bullseye**

::
  
  deb https://mirrors.scau.edu.cn/raspberrypi/ bullseye main ui
  #deb-src https://mirrors.scau.edu.cn/raspberrypi/ bullseye main ui

**Debian 10 buster**

::
  
  deb https://mirrors.scau.edu.cn/raspberrypi/ buster main ui
  #deb-src https://mirrors.scau.edu.cn/raspberrypi/ buster main ui

**Debian 9 stretch**

::
  
  deb https://mirrors.scau.edu.cn/raspberrypi/ stretch main ui
  #deb-src https://mirrors.scau.edu.cn/raspberrypi/ stretch main ui
  
**Debian 8 jessie**

::
  
  deb https://mirrors.scau.edu.cn/raspberrypi/ jessie main ui
  #deb-src https://mirrors.scau.edu.cn/raspberrypi/ jessie main ui

**Debian 7 wheezy**

::
  
  deb https://mirrors.scau.edu.cn/raspberrypi/ wheezy main ui
  #deb-src https://mirrors.scau.edu.cn/raspberrypi/ wheezy main ui

最后执行 ``sudo apt-get update`` 更新软件源

相关链接
========

:官方主页: https://www.raspberrypi.org/
:文档: https://www.raspberrypi.org/documentation/

