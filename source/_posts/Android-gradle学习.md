---
title: Android-gradle学习
date: 2019-03-02 20:11:59
categories: 技术笔记
tags: 
  - Android
  - gradle
  - 构建工具
---

# 准备工作
1. 基于jvm 查看jdk是否安装 java -version
2. init.d运行前会运行的脚本
# Groovy基础
1. 基于java虚拟机的敏捷动态语言。一种面向对象语言。可以编程，也可以作为脚本执行。
2. 兼容java代码。分号可选，默认方法public
3. 属性自动添加getter和setter。
4. assert语句，断言
5. 弱类型语言，def
6. 括号可选
7. 集合api
8. 闭包
9. 双引号中可以通过${}插入变量，三个单引号可以换行
# gradle应用
1. 去官网学习主要方法和基础应用。
2. project使用和了解
3. task最小执行单元
4. 生命周期：初始化：project->配置：task依赖关系和执行图->执行动作代码
5. mavenLocal/mavenCentral/jcenter;自定义仓库；文件仓库（不建议使用）
6. 