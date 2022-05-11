===================
Termux 源使用帮助
===================

地址
====

https://mirrors.scau.edu.cn/termux

说明
====

Termux APT 源镜像

收录架构
========

ARM, AArch64, i686, x86_64

使用说明
==============

首先备份软件源配置：

::

    cp $PREFIX/etc/apt/sources.list $PREFIX/etc/apt/sources.list.bak
    cp -r $PREFIX/etc/apt/sources.list.d/ $PREFIX/etc/apt/sources.list.d.bak/

接着使用以下命令替换默认的配置：

::

    sed -i 's|packages.termux.org|mirrors.scau.edu.cn/termux|g' $PREFIX/etc/apt/sources.list
    sed -i 's|packages.termux.org|mirrors.scau.edu.cn/termux|g' $PREFIX/etc/apt/sources.list.d/*.list

替换后执行 ``apt update`` 更新软件源列表

注：Termux 会自动将环境变量 ``$PREFIX`` 设定为 ``/data/data/com.termux/files/usr``

.. warning::
    Google Play 上的 Termux 已被弃用，如安装会产生兼容性问题。请通过 GitHub 或 F-Droid 来安装 Termux。

相关链接
========

:Termux 官网: https://termux.com/
:GitHub: https://github.com/termux/termux-app
:F-Droid: https://f-droid.org/zh_Hant/packages/com.termux
