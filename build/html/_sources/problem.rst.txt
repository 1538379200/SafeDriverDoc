=======================
SafeDriver问题解决
=======================

linux和mac不能正常使用
=======================

在linux和mac中使用，为了稳定性，需要将pypath和os_填写完整，pypath为driver需要放置的
路径，而os_是当前使用的操作系统，目前支持的操作系统"win", "linux", "mac", "mac_m1"


SafeDriver不稳定
==================

SafeDriver使用的是最简单的获取方式，所以受网站变化的影响也比较大，比较好的是，driver
网站目前更新并没有非常频繁，所以获取也不会有很大影响，当使用不稳定的时候，可以尝试
写入当前系统和driver保存路径

mac用户写好了路径也不能使用？
============================

mac用户某些路径是不可见或者不可操作的，所以，mac用户如果想稳定的使用此工具，最好将
driver放入一个公共的文件夹中，在调用的时候，写好当前driver的路径，如下方所示::

    from SafeDriver.drivers import driver, option
    
    path = 'D:\\python'
    dr = driver(executable_path=path)
    dr.get("https://www.baidu.com")
    dr.quit()


为什么不能给火狐浏览器替换driver？
====================================

目前SafeDriver仅支持chromedriver的更换，这也是更多人选择的driver，后续如果有更多的
使用，会考虑将火狐等浏览器加入