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

string 由16位值组成的不可变的有序序列。

boolean:

> undefined null 0 -0 NaN ""  会转化为false

type of null  -> object
type of '' -> string
type of undefined -> undefined
null == undefined -> true
null === undefined -> false


全局属性：　undefined, Infinity, NaN
全局函数：　isNaN(), parseInt(), eval()
构造函数：　Date(), RegExp(), String(), Object(), Array()
全局对象：　Math, JSON

Math.floor 返回不大于的最大整数
Math.round 1=>1 1.5=>2 1.6=>2 -1.5=>1 -1.6=>2
Math.ceil 返回不小于的最小整数

in运算符
希望左侧为字符串或者可以转换为字符串。
右侧是一个对象。
右侧对象是否包含一个名为左操作数的属性值。

instanceof
左侧为对象，右侧为标识对象的类

http://bonsaiden.github.io/JavaScript-Garden/zh/