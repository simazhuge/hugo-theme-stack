+++
author = "若水"
title = "TODO"
date = "2024-06-28"
description = "准备做的工作列表"
categories = [
    "work"
]
tags = [
    "TODO",
]
+++

# svg 编辑工具
1. 支持svg导入
2. 支持svg编辑
3. 支持svg转tvg （简化版svg)
4. 支持svg def属性的引用，标记为def，引用等
# C语言结构体序列化和反序列化
1. 语言包和编译数据分离：原因，很多情况下都只在一种语种运行，没必要全部载入内存
2. 读写时使用内存映射，提高性能。
3. 对齐，按照CPU特性进行对齐
4. 变量、事件、告警、数据库等都单独编译，然后打包进 hmi种
5. 增加版本控制
6. 采用C++代码，保证standard_layout 兼容 static_assert(std::is_standard_layout<Pen >::value==true,"Pen is not a standard_layout type");
7. 逻辑和数据分离
8. 支持插件式传递，高度兼容性
9. 高度内聚化，开发者不需要关注编译数据的读写过程
