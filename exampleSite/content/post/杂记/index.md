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


# 关于bool 和  char 之间 memcpy
#include <iostream>
#include <cstring>
gcc 在 -O2 的情况下会优化， 导致行为错误，i值是21. 主要是因为 b1值变为21，然后 b1==b2这边又用了异或运算
int main(int argc, char *argv[])
{

    char c1 = 20,c2 = 1;
    bool b1 = false;
    bool b2 = false;

    memcpy(&b1, &c1,1);
    memcpy(&b2, &c2,1);


    int i = ((b1 == b2) ? 0 : 1);
    std::cout << i;
    return 0;
}