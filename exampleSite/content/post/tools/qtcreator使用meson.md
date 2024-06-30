+++
author = "若水"
title = "qtcreator使用meson"
date = "2024-06-27"
description = "qtcreator使用meson"
categories = [
    "Tools"
]
tags = [
    "工具",
    "QtCreator"
]
+++
# 参考
[qtcreator配置官方文档](https://doc.qt.io/qtcreator/creator-project-meson.html)

使用的mysys 下环境搭建
1. meson环境搭建
pacman -S mingw-w64-x86_64-meson 
- [meson安装](https://mesonbuild.com/Getting-meson_zh.html)
- [meson的使用](https://mesonbuild.com/Quick-guide.html#compiling-a-meson-project)
2. ninja安装
注意：需要配置Path, Qtcreator 存在BUG 目前版本手动添加 ninja无法保存