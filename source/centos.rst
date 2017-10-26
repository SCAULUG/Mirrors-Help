==================
CentOS 源使用帮助
==================

地址
====

https://mirrors.scau.edu.cn/centos/

收录架构
========

i686, x86_64

收录版本

5,6,7

使用说明
========

首先备份 :

::

    sudo mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.bak


CentOS 7 配置文件：

::

    sudo wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.scau.edu.cn/CentOS7-Base.repo

CentOS 6 配置文件：

::

    sudo wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.scau.edu.cn/CentOS6-Base.repo

CentOS 5 配置文件：

::

    sudo wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.scau.edu.cn/CentOS5-Base.repo
	
执行 ``sudo yum makecache`` 生成缓存。

相关链接
========

:官方主页: https://www.centos.org/
:邮件列表: https://www.centos.org/modules/tinycontent/index.php?id=16
:论坛: https://www.centos.org/modules/newbb/
:文档: https://www.centos.org/docs/
:Wiki: https://wiki.centos.org/
:镜像列表: https://www.centos.org/modules/tinycontent/index.php?id=32

