+++
author = "若水"
title = "Qt使用记录"
date = "2024-06-18"
description = "记录一些日常使用Qt的小技巧和坑"
categories = [
    "Qt"
]
tags = [
    "QML",
]
+++

# Image 使用svg时候如何不失真， 模糊？
#### 需要将width, height 和 sourceSize的相等
~~~
Image {                         
width: 30
height: 30
source:"qrc:/vieoplayer/video_start.svg";
sourceSize: Qt.size(30, 30)
}
~~~