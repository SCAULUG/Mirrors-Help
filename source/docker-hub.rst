=====================
Docker Hub 源使用帮助
=====================

镜像说明
======

Docker Hub 镜像缓存

地址
====

https://mirrors.scau.edu.cn:5000/


使用说明
========

Linux下 修改配置文件 ``/etc/docker/daemon.json``
Windows下 修改配置文件 ``%programdata%\docker\config\daemon.json``

在配置文件中加入（没有就新建一个）：

::

    {
      "registry-mirrors": ["https://mirrors.scau.edu.cn:5000"]
    }
	
重启docker服务后生效

相关链接
========

:Docker 主页: https://www.docker.com
:Docker Hub: https://hub.docker.com
