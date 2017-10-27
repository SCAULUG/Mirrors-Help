=====================
Docker Hub 源使用帮助
=====================

地址
====

https://mirrors.scau.edu.cn:5000/

说明
====

Docker Hub 镜像缓存

使用说明
========


Linux下 修改配置文件 ``/etc/docker/daemon.json``
Windows下 修改配置文件 ``%programdata%\docker\config\daemon.json``

在配置文件中加入（没有就新建一个）：

::

    {
      "registry-mirrors": ["https://mirrors.scau.edu.cn:5000"]
    }
	
重新启动docker：

::

  sudo service docker restart

相关链接
========

:Docker 主页: https://www.docker.com
:Docker Hub: https://hub.docker.com
