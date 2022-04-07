==================
使用SafeDriver
==================

使用浏览器配置
================


如何使用driver
----------------

.. py:function:: driver(*args, **kwargs);

    :param: 输入参数同selenium的webdriver.Chrome()

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

.. py:function:: option.os_($str);

    :param string: 'win', 'mac', 'mac_m1', 'linux'可选


.. py:function:: option.pypath($str);

    :param string: 需要保存的driver路径

.. warning:: 

    参数非必填，不填写则视为自动搜索，如果是linux或者mac用户，请尽量使用声明的形式，声明当前driver存放路径和系统名称
    


.. code-block:: python

    from SafeDriver.drivers import driver, option
    option.os_ = 'win'
    option.pypath = 'D:\\python'

