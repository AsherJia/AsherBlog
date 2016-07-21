---
layout:     post
title:      "Javascript this"
subtitle:   "this"
date:       2016-07-04 15:23
author:     "Asher"
header-img: "home-bg.jpg"
header-mask: 0.3
catalog:    true
tags:
    - javascript
---

在Javascript中this指向函数执行时的当前对象。
> 值得注意，该关键字在Javascript中和执行环境，而非声明环境有关。

## eval
> 对于eval函数，其执行的时候似乎没有指定当前对象，但实际上其this并非指向windows，因为该函数执行时的作
> 用域是当前作用域，即等用于在该行将里面的代码填进去。