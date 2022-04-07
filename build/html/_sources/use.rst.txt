================
使用SafeDriver
================

使用浏览器配置
==============


如何使用driver
----------------

.. code-block:: python

    from SafeDriver.drivers import driver, option

    dr = driver()
    dr.get("https://www.baidu.com")
    dr.quit()


配置浏览器的option
-------------------

.. code-block:: python

    from SafeDriver.drivers import driver, option

    option.headless = True
    dr = driver()
    dr.get("https://www.baidu.com")
    print(dr.title)
    dr.quit()




配置driver存放路径和所使用的当前系统
------------------------------------


.. code-block:: python

    from SafeDriver.drivers import driver, option
    option.os_ = 'win'
    option.pypath = 'D:\\python'


s