============
简介
============

项目初衷
==========

在selenium的使用中，时常因为driver和浏览器的版本造成了很多驱动引起的错误，明显降低了代码的稳定性，所以，有一个能够时常检查代码运行的工具，
在某些时候是非常有必要的。


项目使用第三方库
==================

1. requests
2. bs4
3. selenium

SafeDriver实现功能
====================

当使用SafeDriver生成driver对象时，SafeDriver会尝试获取当前可用driver对象，当出现
错误后，SafeDriver将会根据当前的浏览器版本，自动下载并替换当前的旧版本driver文件，
保证当前的代码可用

.. image:: ./_static/yanshi.png
    :width: 500px

.. image:: ./_static/res.png
    :width: 500px






