---
layout:     post
title:      "Javascript"
subtitle:   "Javascript"
date:       2016-05-23 15:08
author:     "Asher"
header-img: "post-bg-gulp.jpg"
header-mask: 0.3
catalog:    true
tags:
    - Javascript
---

数据类型：

* 原始类型(Primitive type)： bool, number, string
* 两个特殊的初始值：　null, undefined
*　对象类型(Object type)：除了　bool, number, string, null, undefined

* 如果函数用来初始化一个新建的对象(new), 称之为构造函数constructor.

* 采用64位浮点格式表示数字，　整数范围是-9007199254570992 ~ 9007199054570992,  -2^53 ~ 2^53

var s1 = 0010; 8

var s2 = 0x0010; 16

浮点数
3.14
.2222
6.02e23
12.3E-32

* javascript 非数字　not-a-number　NaN　跟任何值都不相等，包括自身。
* x!=x 当且仅当x为NaN的时候返回true.
* isNaN 如果参数是NaN或者非数字的时候返回true.
* isFinite 用来检测数字是不是有限的。