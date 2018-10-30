=====================
Ubuntu 源使用帮助
=====================

地址
====

https://mirrors.scau.edu.cn/ubuntu/

收录架构
========

AMD64 (x86_64), i3686

使用说明
========

先通过如下指令备份配置文件：

::
  
  sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak


一般情况下，将 :file:`/etc/apt/sources.list` 文件中 Ubuntu 默认的源地址 ``http://archive.ubuntu.com/``
替换为 ``https://mirrors.scau.edu.cn`` 即可。

可用以下命令替换：

::

  sudo sed -i 's/archive.ubuntu.com/mirrors.scau.edu.cn/g' /etc/apt/sources.list

.. tip::
    如果你在安装时选择的语言不是英语，默认的源地址通常不是 ``http://archive.ubuntu.com/`` ，而是 ``http://<country-code>.archive.ubuntu.com/ubuntu/`` 例如： ``http://cn.archive.ubuntu.com/ubuntu/`` ，此时只需将上面的命令进行相应的替换即可，如： ``sudo sed -i 's/cn.archive.ubuntu.com/mirrors.scau.edu.cn/g' /etc/apt/sources.list`` 。
 
最后执行 ``sudo apt-get update`` 更新软件源列表

也可以直接编辑 :file:`/etc/apt/sources.list` 文件（需要使用 sudo）。以下是 Ubuntu 各版本参考配置内容：

::
  
    # Ubuntu 18.04 LTS
    # 默认注释了源码仓库，如有需要可自行取消注释
    deb https://mirrors.scau.edu.cn/ubuntu/ bionic main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ bionic main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ bionic-security main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ bionic-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirrors.scau.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse

::
  
    # Ubuntu 16.04 LTS
    # 默认注释了源码仓库，如有需要可自行取消注释
    deb https://mirrors.scau.edu.cn/ubuntu/ xenial main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ xenial main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ xenial-security main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ xenial-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirrors.scau.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse

::
  
    # Ubuntu 14.04 LTS
    # 默认注释了源码仓库，如有需要可自行取消注释
    deb https://mirrors.scau.edu.cn/ubuntu/ trusty main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ trusty main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ trusty-updates main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ trusty-updates main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ trusty-backports main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ trusty-backports main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ trusty-security main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ trusty-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirrors.scau.edu.cn/ubuntu/ trusty-proposed main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ trusty-proposed main restricted universe multiverse

::
  
    # Ubuntu 12.04 LTS
    # 默认注释了源码仓库，如有需要可自行取消注释
    deb https://mirrors.scau.edu.cn/ubuntu/ precise main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ precise main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ precise-updates main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ precise-updates main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ precise-backports main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ precise-backports main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ precise-security main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ precise-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirrors.scau.edu.cn/ubuntu/ precise-proposed main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ precise-proposed main restricted universe multiverse

::
  
    # Ubuntu 18.10
    # 默认注释了源码仓库，如有需要可自行取消注释
    deb https://mirrors.scau.edu.cn/ubuntu/ cosmic main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ cosmic main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ cosmic-updates main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ cosmic-updates main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ cosmic-backports main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ cosmic-backports main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ cosmic-security main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ cosmic-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirrors.scau.edu.cn/ubuntu/ cosmic-proposed main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ cosmic-proposed main restricted universe multiverse

::
  
    # Ubuntu 17.10
    # 默认注释了源码仓库，如有需要可自行取消注释
    deb https://mirrors.scau.edu.cn/ubuntu/ artful main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ artful main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ artful-updates main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ artful-updates main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ artful-backports main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ artful-backports main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ artful-security main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ artful-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirrors.scau.edu.cn/ubuntu/ artful-proposed main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ artful-proposed main restricted universe multiverse

::
  
    # Ubuntu 17.04
    # 默认注释了源码仓库，如有需要可自行取消注释
    deb https://mirrors.scau.edu.cn/ubuntu/ zesty main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ zesty main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ zesty-updates main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ zesty-updates main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ zesty-backports main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ zesty-backports main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ zesty-security main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ zesty-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirrors.scau.edu.cn/ubuntu/ zesty-proposed main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ zesty-proposed main restricted universe multiverse

::
  
    # Ubuntu 16.10
    # 默认注释了源码仓库，如有需要可自行取消注释
    deb https://mirrors.scau.edu.cn/ubuntu/ yakkety main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ yakkety main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ yakkety-updates main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ yakkety-updates main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ yakkety-backports main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ yakkety-backports main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ yakkety-security main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ yakkety-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirrors.scau.edu.cn/ubuntu/ yakkety-proposed main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ yakkety-proposed main restricted universe multiverse

::
  
    # Ubuntu 15.10
    # 默认注释了源码仓库，如有需要可自行取消注释
    deb https://mirrors.scau.edu.cn/ubuntu/ wily main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ wily main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ wily-updates main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ wily-updates main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ wily-backports main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ wily-backports main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ wily-security main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ wily-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirrors.scau.edu.cn/ubuntu/ wily-proposed main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ wily-proposed main restricted universe multiverse

::
  
    # Ubuntu 15.04
    # 默认注释了源码仓库，如有需要可自行取消注释
    deb https://mirrors.scau.edu.cn/ubuntu/ vivid main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ vivid main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ vivid-updates main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ vivid-updates main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ vivid-backports main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ vivid-backports main restricted universe multiverse
    deb https://mirrors.scau.edu.cn/ubuntu/ vivid-security main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ vivid-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirrors.scau.edu.cn/ubuntu/ vivid-proposed main restricted universe multiverse
    # deb-src https://mirrors.scau.edu.cn/ubuntu/ vivid-proposed main restricted universe multiverse

相关链接
========

:官方主页: https://www.ubuntu.com/
:文档: https://help.ubuntu.com/
:Wiki: https://wiki.ubuntu.com/
:邮件列表: https://community.ubuntu.com/contribute/support/mailinglists/
:提问: https://askubuntu.com/
:论坛: https://ubuntuforums.org/
:中文论坛: https://forum.ubuntu.org.cn/

