---
title: 2018/09/08-VUEJS学习笔记整理
date: 2018-09-08 16:02:26
categories: -VUEJS
tags:
    - VUEJS
    - 学习笔记
---

1. 生命周期钩子(created\mounted\updated\destroyed)的 this 上下文指向调用它的 Vue 实例。  
2. 不要在选项属性或回调上使用箭头函数,因为箭头函数是和父级上下文绑定在一起的，this 不会是如你所预期的 Vue 实例  
3. 