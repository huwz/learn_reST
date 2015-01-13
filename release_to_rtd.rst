文档发布
========

创建sphinx工程
--------------

选择一个公共的git服务器，创建一个裸仓库。
本人选择的是: `Github <https://github.com>`_。
将仓库 `git clone` 到本地，假设 `.git` 所在的文件夹为 **test_sphinx**。

在test_sphinx文件夹中打开cmd，执行sphinx-quickstart.py [1]_。
创建一个sphinx工程之后，可以向index.rst中添加文档。
文档编辑之后，可以本地执行 `make.bat html` 进行测试。
在build成功 [2]_ 之后，可以提交到远程仓库。

发布到RTD
---------

将sphinx工程发布到RTD是写文档的最后一个步骤。
登陆 `RTD官方网站 <https://readthedocs.org>`_，选择 `Import a Project`。
然后选择 `Manually Import Project`，有一些必要的选项：

* rtd工程名（不能和别的工程同名）
* 仓库url——填写sphinx工程所在的远程仓库的url，例如：https://github.com/huwz/learn_reST.git
* 仓库类型选择 `git`
* 勾选编辑工程高级选项
* 文档类型选择 `Sphinx Html`
* HTML显示的语言为：`Simplified Chinese`
* 编程语言选择：`Only words`
* 仅保留 `lastest` 版本，勾选 `Single Version`

.. [1] 除了工程名，作者名，版本号和发布版本号之外，其余的可以默认
.. [2] 0 errors, 0 warning
