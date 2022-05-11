===========================
Debian Security 源使用帮助
===========================

地址
====

https://mirrors.scau.edu.cn/debian-security/


收录架构
========

Debian 支持的所有架构，如 AMD64 (x86_64), Intel x86, ARM, MIPS, ppc64el, s390x 等


收录版本
========

Debian Old Old Stable, Old Stable, Stable

当前 Stable 为 Debian 11，代号为 Bullseye


使用须知
=========

本站（华南农业大学开源镜像源）Debian Security 源的直接上游为 `科大开源软件镜像站<https://mirrors.ustc.edu.cn/debian-security/>`_，且镜像同步时间为每日凌晨一点，对debian-security官方源的同步不一定及时。因此，用户如需尽快获取安全更新，应该直接使用官方源 http://security.debian.org/debian-security 进行安全更新。


使用说明
========

如果还没有安装 ``apt-transport-https`` ，请先用如下命令安装:

::

  sudo apt-get install apt-transport-https


之后，可以运用如下命令备份 ``/etc/apt/sources.list`` 文件：

::

  sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak


一般情况下，将 :file:`/etc/apt/sources.list` 文件中 Debian 默认的源地址 ``http://security.debian.org/debian-security/``
替换为 ``https://mirrors.scau.edu.cn/debian-security/`` 即可

需要注意的是，从 Debian 11 "Bullseye" 开始，安全更新仓库名从 ``发行版代号/updates`` 更新为 ``发行版代号-security``，详见 `Debian 11 (bullseye) 发行说明 <https://www.debian.org/releases/bullseye/amd64/release-notes/ch-information.zh-cn.html#security-archive>`_，请旧版本用户注意。

对于 Debian 9 "stretch" 或更新的版本，可以使用如下命令进行替换：

::

  sudo sed -i 's#http://security.debian.org/debian-security#https://mirrors.scau.edu.cn/debian-security#g' /etc/apt/sources.list


对于 Debian 8 "Jessie" 或更早的版本，则默认的 debian-security 源地址为 ``http://security.debian.org/`` （和新版不同最后没有子目录）。

替换后执行 ``sudo apt-get update`` 更新软件源列表


相关链接
========

:官方主页: https://www.debian.org/security/
:Debian 安全追踪网: https://security-tracker.debian.org/tracker/
