================
PyPI 源使用帮助
================

地址
====

https://mirrors.scau.edu.cn/pypi/

说明
====

PyPI(pip) 软件源.

使用说明
========

Linux 用户修改配置文件 ``~/.pip/pip.conf``

Windows 用户修改配置文件 ``%HOME%\pip\pip.ini`` (没有就新建一个)

找到配置文件中 以 ``index-url`` 开头的一行并将其修改为下面一行:

::

  [global]
  index-url = https://mirrors.scau.edu.cn/pypi/web/simple
  
相关链接
========
:PyPI Official Mirrors: https://pypi.python.org/mirrors
:PEP-381 Mirroring Protocol: http://www.python.org/dev/peps/pep-0381/
:bandersnatch: https://pypi.python.org/pypi/bandersnatch
