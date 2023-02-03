+++
title = "JavaScript 基础"
author = ["wenhu"]
date = 2023-02-02T13:58:00+08:00
categories = ["js"]
draft = false
+++

## Var {#var}

only a variable's declaration is hoisted, not its initialization

var declarations are processed when the function starts (or script starts for globals)

var 的变量声明会被提升，变量赋值及初始化不会

var 没有块级作用域，只有函数和全局作用域

without use strict, an assignment to a non-existing variable creates a new global variable


## Lexical Environment[^fn:1] {#lexical-environment}

运行中的函数，代码块，脚本全局都有与之对应的 LE

词法环境对象，包括两部分:

1.  Environment Record 环境记录对象，保存局部变量，this 信息
2.  指向外层词法环境的指针

A variable is a property of a special internal object, associated with the currently executing block/function/script

执行上下文分全局上下文、函数上下文和块级上下文

代码执行流每进入一个新上下文，都会创建一个作用域链，用于搜索变量和函数。


## Function {#function}

函数声明会在词法环境创建时，立刻初始化，所以我们可以在函数声明前调用函数

函数表达式不会

```js
// 函数声明
function foo() {}

// 函数表达式
let a = function () {}
```

函数在每次调用时，都会创建一个与之关联的 LE

参数，局部变量，都是 ER 的一个属性


### 闭包 {#闭包}

闭包即函数，能记住其外层作用域变量并使用

每个函数都有个隐藏的 [ [Environment] ] 属性，指向其被创建的词法环境


### 箭头函数 {#箭头函数}

this 为外层词法环境的 this，不能被 new，没有 arguments, 没有 super


## Prototype {#prototype}


## Class {#class}

[^fn:1]: [lexical-environment](https://javascript.info/closure)