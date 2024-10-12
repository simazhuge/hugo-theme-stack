+++
author = "若水"
title = "Linux常用命令"
date = "2024-06-18"
description = "Linux 常用命令"
categories = [
    "Linux"
]
tags = [
    " Linux 常用命令",
]
+++
# Linux 常用命令
### 1. 修改 mac地址
~~~
ifconfig eth0 down
ifconfig eth0 hw ether 00:aa:aa:aa:aa:01
ifconfig eth0 192.168.210.210
ifconfig eth0 up
~~~ 