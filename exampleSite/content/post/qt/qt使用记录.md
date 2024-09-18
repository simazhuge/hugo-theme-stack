+++
author = "若水"
title = "Qt使用记录"
date = "2024-06-18"
description = "记录一些日常使用Qt的小技巧和坑"
categories = [
    "Qt"
]
tags = [
    "QPainter",
]
+++

# 1、 QDir::currentPath() 和 QCoreApplication::applicationDirPath() 区别
~~~
QString QDir::currentPath()
返回的是启动应用程序的父进程

如果在VS中运行，则返回的是源文件和头文件所在的路径；
如果直接双击exe运行，则返回的是exe所在的路径；
QString QCoreApplication::applicationDirPath()

无论在什么情况下，返回的都是exe所在的绝对路径。
~~~ 