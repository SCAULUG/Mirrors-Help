===============
EPEL 源使用帮助
===============

镜像说明
========

EPEL (Extra Packages for Enterprise Linux) 是由 Fedora Special Interest Group 为企业 Linux 创建、维护和管理的一个高质量附加包集合，适用于但不仅限于 Red Hat Enterprise Linux (RHEL), CentOS, Scientific Linux (SL), Oracle Linux (OL)

地址
====

https://mirrors.scau.edu.cn/epel/

收录架构
==============================

官方支持的所有架构

收录版本
==============================

官方支持的所有版本

使用说明
========

若还没有安装epel-release，首先将其安装：

::
  
  sudo yum install epel-release

先备份 ``/etc/yum.repos.d/epel.repo`` 文件：

::
  
  sudo cp /etc/yum.repos.d/epel.repo /etc/yum.repos.d/epel.repo.bak

执行以下命令：

::
  
  sudo sed -e 's|^metalink=|#metalink=|g' \
           -e 's|^#baseurl=https\?://download.fedoraproject.org/pub/epel/|baseurl=https://mirrors.scau.edu.cn/epel/|g' \
           -e 's|^#baseurl=https\?://download.example/pub/epel/|baseurl=https://mirrors.scau.edu.cn/epel/|g' \
           -i.bak \
           /etc/yum.repos.d/epel.repo

修改后的 ``/etc/yum.repos.d/epel.repo`` 文件如下(因Linux版本不同有所差异)：

::

    [epel]
    name=Extra Packages for Enterprise Linux 7 - $basearch
    baseurl=https://mirrors.scau.edu.cn/epel/7/$basearch
    #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=epel-7&arch=$basearch
    failovermethod=priority
    enabled=1
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7

    [epel-debuginfo]
    name=Extra Packages for Enterprise Linux 7 - $basearch - Debug
    baseurl=https://mirrors.scau.edu.cn/epel/7/$basearch/debug
    #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=epel-debug-7&arch=$basearch
    failovermethod=priority
    enabled=0
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7
    gpgcheck=1

    [epel-source]
    name=Extra Packages for Enterprise Linux 7 - $basearch - Source
    baseurl=https://mirrors.scau.edu.cn/epel/7/SRPMS
    #mirrorlist=https://mirrors.fedoraproject.org/metalink?repo=epel-source-7&arch=$basearch
    failovermethod=priority
    enabled=0
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7
    gpgcheck=1

相关链接
==============================

:WIKI: http://fedoraproject.org/wiki/EPEL
:FAQ: http://fedoraproject.org/wiki/EPEL/faq

