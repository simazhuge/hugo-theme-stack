+++
author = "若水"
title = "杂记"
date = "2024-06-24"
description = "随手记录"
categories = [
    "work"
]
tags = [
    "杂记",
]
+++

# mutable 关键字什么作用
在C++中，mutable 关键字用于允许一个类的成员变量在 const 成员函数中被修改。通常，在 const 成员函数中，所有成员变量都被视为常量，不能被修改。然而，有时候我们希望能够在 const 成员函数中修改某些特定的成员变量，例如缓存数据或调试信息，这时就可以使用 mutable 关键字。

# 编译时候静态检测
- static_assert(std::is_standard_layout<Pen >::value==true,"Pen is not a standard_layout type");
- is_trivially_copyable
- is_standard_layout
- is_pod