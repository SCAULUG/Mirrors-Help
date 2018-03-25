================
Anaconda 源使用帮助
================

镜像说明
=======

Anaconda 是一个用于科学计算的 Python 发行版，支持 Linux, Mac, Windows, 包含了众多流行的科学计算、数据分析的 

Python 包。它有着可以和 PyPI 协作的独立包管理系统 conda ，可以通过不同于 PyPI 的源进行许多 Python 包的安装。

此镜像还包含了 MiniConda 镜像和一些第三方源，包括 Conda Forge, msys2, bioconda 和 menpo 。

地址
====

https://mirrors.scau.edu.cn/anaconda/

使用说明
======

Anaconda 安装包可以到 ``https://mirrors.scau.edu.cn/anaconda/archive/`` 下载。

也可以运行以下命令添加 Anaconda Python 免费仓库：

::

   conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
   conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
   conda config --set show_channel_urls yes



添加完后可运行 ``conda install numpy`` 进行测试

Miniconda 安装包可以到 ``https://mirrors.scau.edu.cn/anaconda/miniconda/`` 下载。

- Conda Forge 

::
  
  conda config --add channels https://mirrors.scau.edu.cn/anaconda/cloud/conda-forge/



- msys2 

::

  conda config --add channels https://mirrors.scau.edu.cn/anaconda/cloud/msys2/



- bioconda 

::

  conda config --add channels https://mirrors.scau.edu.cn/anaconda/cloud/bioconda/



- menpo 

 ::

  conda config --add channels https://mirrors.scau.edu.cn/anaconda/cloud/menpo/



相关链接
======

: 官方主页: https://www.continuum.io/

