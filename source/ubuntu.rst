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

也可以直接编辑 :file:`/etc/apt/sources.list` 文件（需要使用 sudo）。以下是 Ubuntu 16.04 参考配置内容：

::
  
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


相关链接
========

:官方主页: https://www.ubuntu.com/
:文档: https://help.ubuntu.com/
:Wiki: https://wiki.ubuntu.com/
:邮件列表: https://community.ubuntu.com/contribute/support/mailinglists/
:提问: https://askubuntu.com/
:论坛: https://ubuntuforums.org/
:中文论坛: https://forum.ubuntu.org.cn/

