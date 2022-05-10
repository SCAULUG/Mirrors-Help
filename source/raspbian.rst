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

stretch (oldoldstable)

buster (oldstable)

bullseye (stable)

bookworm (testing)


使用说明
========

由于镜像站强制使用https,需要提前安装 ``apt-transport-https`` 

先用以下命令备份 ``/etc/apt/sources.list`` 文件内容：

::
  
  sudo mv /etc/apt/sources.list /etc/apt/sources.list.bak

新建 ``/etc/apt/sources.list`` 文件，并根据版本加入对应内容：

**Debian 10 buster**

::
  
  deb https://mirrors.scau.edu.cn/raspbian/raspbian/ buster main non-free contrib rpi
  deb-src https://mirrors.scau.edu.cn/raspbian/raspbian/ buster main non-free contrib rpi

**Debian 9 stretch**

::
  
  deb https://mirrors.scau.edu.cn/raspbian/raspbian/ stretch main non-free contrib rpi
  deb-src https://mirrors.scau.edu.cn/raspbian/raspbian/ stretch main non-free contrib rpi
  
**Debian 8 jessie**

::
  
  deb https://mirrors.scau.edu.cn/raspbian/raspbian/ jessie main non-free contrib rpi
  deb-src https://mirrors.scau.edu.cn/raspbian/raspbian/ jessie main non-free contrib rpi

**Debian 7 wheezy**

::
  
  deb https://mirrors.scau.edu.cn/raspbian/raspbian/ wheezy main non-free contrib rpi
  deb-src https://mirrors.scau.edu.cn/raspbian/raspbian/ wheezy main non-free contrib rpi

最后执行 ``sudo apt-get update`` 更新软件源

同时也需要更改 archive.raspberrypi.org 源

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

Raspberrypi 源使用帮助
======================

先用以下命令备份 ``/etc/apt/sources.list.d/raspi.list`` 文件内容：

::
  
  sudo mv /etc/apt/sources.list.d/raspi.list /etc/apt/sources.list.d/raspi.list.bak

新建 ``/etc/apt/sources.list.d/raspi.list`` 文件，并根据版本加入对应内容：

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

