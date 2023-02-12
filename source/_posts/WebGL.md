---
title: WebGL
date: 2022-08-10 16:47:56
categories: -WebGL
tags:
    - WebGL
    - 学习笔记
---

# WebGL Learning
## Website
1. [WebGL Lesson](https://webglfundamentals.org/webgl/lessons/zh_cn/)
2. [WebGL2 Lesson](https://webgl2fundamentals.org/webgl/lessons/zh_cn/)

## WebGL
### 笔记
1. WebGL在电脑的GPU中运行。因此你需要使用能够在GPU上运行的代码。 这样的代码需要提供成对的方法。每对方法中一个叫顶点着色器， 另一个叫片断着色器，并且使用一种和C或C++类似的强类型的语言 GLSL。 (GL着色语言)。 每一对组合起来称作一个 program（着色程序）。
2. 顶点着色器的作用是计算顶点的位置。
3. 