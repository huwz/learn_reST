reST学习积累
============

.. note::

  本文纯属个人的经验之谈，存疑之处，请参考reStructuredText官方文档。

reST语法不转义
--------------

暂时只知道两种情况下，不会转义，而且保留回车换行符：

1. 在 ```````` 中
2. 在代码块里

行内引用
--------

1. 加重强调，例如：
   ``**a**``，效果为: **a**
2. 斜体，例如：
   ``*a*`` 或者 ```a``` ，效果为： *a* 或者 `a`
3. 保留reST的功能字符不转义，例如：
   ````*a*````，效果为： ``*a*``

.. _code-block-label:

代码块
------

代码块 [1]_ 的格式::

  <代码块说明>::
  (blank line)
  (缩进)<代码块>
  (blank line)

  代码块的缩进量不能小于 `<代码块说明>` 语句。
  退出代码块时，需要添加空行。
  新的正文缩进不超过 `<代码块说明>` 语句的缩进。

在代码块中所有的语法都失效了，可以直接写原本应该转义的reST代码。

举例：

.. code-block:: C
  :linenos:

    void main()
    {
        printf("hello,world\n");
    }

链接
----

1. 链接某个章节
   
   语法格式::

      (blank line)
      .. _label_name:
      (blank line)
      chapter title
      -------------

      引用：:ref:`content<label_name>`/ :ref:`label_name`/ `label_name`_。
      第三种方式不太好，会在html中直接显示label_name

.. _link_picture:

2. 链接图片
   
   * 引用带标题的图片，其语法如下::

      .. _label_name:
      (blank line)
      .. figure:: image path
      (blank line)
      <image title>
   	  
      引用的时候，用:ref:`label_name`。

    举例说明：

    :ref:`my_table`

   * 引用不带标题的图片，比较简单::
     
      .. image:: <image relative or absolute path>

3. 链接非章节，语法如下::
   
       .. _label_name:
       (blank line)
       <正文>
       (blank)
       引用的时候，使用:ref:`content<label_name>`
       
4. 注脚的语法如下::
   
     1. 在需要添加注脚的词汇后面添加[1_],[2_],...
     2. 前后各需要一个空格
     3. 在文章的某个位置加上:

       .. [1] 对词汇1的解释
       .. [2] 对词汇2的解释
       ...

7. 添加引文，其语法::
	
   	.. [refname] text，引用 ``[refname]_``，前后都有空格。

   举例： [引文]_

8. 使用role，语法格式::

  * code-block 参照 :ref:`code-block-label`
  * note 语法::
      
      .. note:: <正文>

    正文的缩进不能小于 `.. note::` 语句。
    结束note时，前面有空行。
    新的正文缩进量不能大于 `.. note::` 语句。
  * warning/error/important 和note一样
  * image 参考 :ref:`链接图片<link_picture>`
	
9. 测试用例：
    
   .. error:: 出错了
   

   .. _my_table:

   .. figure:: images/1.png
      
     带标题图表引用

   
   .. [引文] 这是引文

   .. [1] 代码块不等同于code-block
