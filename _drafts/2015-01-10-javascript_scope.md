---
title: JavaScript 作用域
category: 技术
tag: JavaScript
---

## 概要

在 JavaScript 中，作用域就是执行代码的上下文。作用域有三种类型：全局作用域、局部作用域（亦称作“函数作用域”）、eval 作用域。

在函数内部使用 var 定义的代码，其作用域是局部的，且只对该函数的其他表达式是“可见的”，包括嵌套（子函数）中的代码。

在全局作用域内定义的变量从任何地方都可以访问，但它是作用域链中的最高层（最后一个）。