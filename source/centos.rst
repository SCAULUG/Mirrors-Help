==================
CentOS 源使用帮助
==================

地址
====

https://mirrors.scau.edu.cn/centos/

收录架构
========

i386, x86_64

收录版本
========

7,8

使用说明
========

首先备份 :

::

    sudo cp -r /etc/yum.repos.d/ /etc/yum.repos.d.bak/


对于 CentOS 8，使用以下命令替换默认的配置

::

    sudo sed -e 's|^mirrorlist=|#mirrorlist=|g' \
            -e 's|^#baseurl=http://mirror.centos.org/$contentdir|baseurl=https://mirrors.scau.edu.cn/centos|g' \
            -i.bak \
            /etc/yum.repos.d/CentOS-Linux-AppStream.repo \
            /etc/yum.repos.d/CentOS-Linux-BaseOS.repo \
            /etc/yum.repos.d/CentOS-Linux-Extras.repo \
            /etc/yum.repos.d/CentOS-Linux-PowerTools.repo \
            /etc/yum.repos.d/CentOS-Linux-Plus.repo


对于 CentOS 7，使用以下命令替换默认配置

::

  sudo sed -e 's|^mirrorlist=|#mirrorlist=|g' \
           -e 's|^#baseurl=http://mirror.centos.org/centos|baseurl=https://mirrors.scau.edu.cn/centos|g' \
           -i.bak \
           /etc/yum.repos.d/CentOS-Base.repo


注意，如果需要启用其中一些 repo，请将其中的 ``enabled=0`` 改为 ``enabled=1``。

执行 ``sudo yum makecache`` 生成缓存。

相关链接
========

:官方主页: https://www.centos.org/
:邮件列表: https://www.centos.org/modules/tinycontent/index.php?id=16
:论坛: https://www.centos.org/modules/newbb/
:文档: https://www.centos.org/docs/
:Wiki: https://wiki.centos.org/
:镜像列表: https://www.centos.org/modules/tinycontent/index.php?id=32

