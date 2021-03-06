sphinx+sublime3构造reST编辑环境
===============================

.. note::
	在安装sphinx和sublime之前要安装Python2.x或者Python3.x。

1. 到官方网站下载 `Sphinx-1.3b2.tar.gz <https://pypi.python.org/pypi/Sphinx/1.3b2>`_
2. 解压 `Sphinx-1.3b2.tar.gz` 到本地文件夹
   进入 `Sphinx-1.3b2`，执行 `ez_setup.py`
3. 第二步获取到压缩包 `setuptools-7.0.zip`
4. 解压 `setuptools-7.0.zip`，进入文件夹 `setuptools-7.0`
5. 在当前目录打开 `cmd`，运行 `easy_install.py sphinx`
6. 将 `Sphinx-1.3b2` 文件夹路径写入环境变量 `path`
7. 到sublime官网下载 `sublime3 <http://www.sublimetext.com/3>`_
8. 安装sublime3（未注册版本）
9. 给sublime3安装一些必要的插件:
    
    * `Package Control <https://packagecontrol.io/installation>`_
    * `sublime-rst-completion <https://github.com/mgaitan/sublime-rst-completion>`_
    * RestructuredText Improved [1]_
    * OmniMarkupPreviewer

.. [1] 本人在安装完该插件之后，每次打开Sublime都提示不存在Packages/RestructuredText/tmLanguage。将sublime界面中的文件都关闭，重新加载.rst文件，错误信息消失。