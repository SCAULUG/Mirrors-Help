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

6,7,8

使用说明
========

首先备份 :

::

    sudo cp /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.bak


然后替换文件 ``/etc/yum.repos.d/CentOS-Base.repo`` 内容为以下相应内容  


CentOS 8 配置文件内容：

::

    # CentOS-Base.repo
    #
    # The mirror system uses the connecting IP address of the client and the
    # update status of each mirror to pick mirrors that are updated to and
    # geographically close to the client.  You should use this for CentOS updates
    # unless you are manually picking other mirrors.
    #
    # If the mirrorlist= does not work for you, as a fall back you can try the
    # remarked out baseurl= line instead.
    #
    #



    [BaseOS]
    name=CentOS-$releasever - Base
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/BaseOS/$basearch/os/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=BaseOS&infra=$infra
    enabled=1
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-centosofficial

    [AppStream]
    name=CentOS-$releasever - AppStream
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/AppStream/$basearch/os/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=AppStream&infra=$infra
    enabled=1
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-centosofficial

    [PowerTools]
    name=CentOS-$releasever - PowerTools
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/PowerTools/$basearch/os/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=PowerTools&infra=$infra
    enabled=0
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-centosofficial

    #additional packages that may be useful
    [extras]
    name=CentOS-$releasever - Extras
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/extras/$basearch/os/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=extras
    enabled=1
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-centosofficial

    #additional packages that extend functionality of existing packages
    [centosplus]
    name=CentOS-$releasever - Plus
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/centosplus/$basearch/os/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=centosplus
    gpgcheck=1
    enabled=0
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-centosofficial





CentOS 7 配置文件内容：

::

    # CentOS-Base.repo
    #
    # The mirror system uses the connecting IP address of the client and the
    # update status of each mirror to pick mirrors that are updated to and
    # geographically close to the client.  You should use this for CentOS updates
    # unless you are manually picking other mirrors.
    #
    # If the mirrorlist= does not work for you, as a fall back you can try the
    # remarked out baseurl= line instead.
    #
    #

    [base]
    name=CentOS-$releasever - Base
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/os/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=os
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7

    #released updates
    [updates]
    name=CentOS-$releasever - Updates
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/updates/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=updates
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7

    #additional packages that may be useful
    [extras]
    name=CentOS-$releasever - Extras
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/extras/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=extras
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7

    #additional packages that extend functionality of existing packages
    [centosplus]
    name=CentOS-$releasever - Plus
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/centosplus/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=centosplus
    gpgcheck=1
    enabled=0
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7

    



CentOS 6 配置文件内容：

::

    # CentOS-Base.repo
    #
    # The mirror system uses the connecting IP address of the client and the
    # update status of each mirror to pick mirrors that are updated to and
    # geographically close to the client.  You should use this for CentOS updates
    # unless you are manually picking other mirrors.
    #
    # If the mirrorlist= does not work for you, as a fall back you can try the
    # remarked out baseurl= line instead.
    #
    #

    [base]
    name=CentOS-$releasever - Base
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/os/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=os
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6

    #released updates
    [updates]
    name=CentOS-$releasever - Updates
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/updates/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=updates
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6

    #additional packages that may be useful
    [extras]
    name=CentOS-$releasever - Extras
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/extras/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=extras
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6

    #additional packages that extend functionality of existing packages
    [centosplus]
    name=CentOS-$releasever - Plus
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/centosplus/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=centosplus
    gpgcheck=1
    enabled=0
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6

    #contrib - packages by Centos Users
    [contrib]
    name=CentOS-$releasever - Contrib
    baseurl=https://mirrors.scau.edu.cn/centos/$releasever/contrib/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=contrib
    gpgcheck=1
    enabled=0
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6


    


执行 ``sudo yum makecache`` 生成缓存。

相关链接
========

:官方主页: https://www.centos.org/
:邮件列表: https://www.centos.org/modules/tinycontent/index.php?id=16
:论坛: https://www.centos.org/modules/newbb/
:文档: https://www.centos.org/docs/
:Wiki: https://wiki.centos.org/
:镜像列表: https://www.centos.org/modules/tinycontent/index.php?id=32

