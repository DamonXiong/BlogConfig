---
title: Android-学习笔记
date: 2019-03-10 16:21:46
categories: 技术笔记
tags:
 - Android
---

# RXJava
## 学习链接
### 文章
[feiq's Blog](http://blog.inching.org/categories/RxJava/)  
[给 Android 开发者的 RxJava 详解](https://gank.io/post/560e15be2dca930e00da1083)  
[RxBus – Implementing event bus with RxJava](https://androidwave.com/rxbus-implementing-event-bus-with-rxjava/)
[Android常用之Butterknife使用详解](https://segmentfault.com/a/1190000016460847)

### 视频
[RxJava与RxAndroid基础入门](https://www.imooc.com/learn/877)

### Github
[ReactiveX/RxAndroid](https://github.com/ReactiveX/RxAndroid)  
[rengwuxian/RxJavaSamples](https://github.com/rengwuxian/RxJavaSamples)  
[JakeWharton/RxBinding](https://github.com/JakeWharton/RxBinding)  
[JakeWharton/butterknife](https://github.com/JakeWharton/butterknife)

### 学习笔记
1. flatMap() 的原理是这样的：
   1. 使用传入的事件对象创建一个 Observable 对象；
   2. 并不发送这个 Observable, 而是将它激活，于是它开始发送事件；
   3. 每一个创建出来的 Observable 发送的事件，都被汇入同一个 Observable ，而这个 Observable 负责将这些事件统一交给 Subscriber 的回调方法。
2. 


# 应用服务器
[LeanCloud](https://leancloud.cn/dashboard/login.html#/signin)  
[Bmob](https://www.bmob.cn/)  

# Gson使用
[GSON序列化时排除字段的几种方式](https://my.oschina.net/orgsky/blog/368768)

# 《Android基础视频课程》
1. 存储方式： sharepreference(系统配置信息)轻量键值存储基本类型、Files(应用程序私有)、sqlite(数据库)、NetWork（通过网络存储和获取数据）。


# 《Android必学-AsyncTask基础》
1. 子线程更新UI
2. 封装、简化异步操作

# 《Android必学-异步加载》
## 课程地址
[Android必学-异步加载](https://www.imooc.com/learn/406)

## 学习笔记
1. 子线程更新UI
2. 

# 《深入理解Android：卷1》
## JNI
### 概述
1. JNI，是Java Native Interface的缩写，中文为Java本地调用。JNI是一种技术
2. JNI将java与native紧密连接起来，使java能够调用native函数，native能够调用java函数
3. JNI必须实现为动态库的形式，这样java虚拟机才能加载它并调用它的函数。
4. Native语言中“.”有特殊的意义，所以JNI需要把java函数中的"."换成"_"。
5. JNI注册：将Java层的native函数和JNI层对应的实现函数关联起来。
6. JNI注册两种方法  
   a. 静态注册：根据函数名来找对应的JNI函数。需要依照一定规则生产函数，增加编译工作、函数名长、初次调用建立关联影响效率  
   b. 动态注册：JNI中实现JNI_OnLoad
7. JNIENV与线程相关，OnLoad中JNIVM是独一份的，可以通过JNIVM获取当前线程的JNIENV
   1. 调用JavaVM的AttachCurrentThread函数，就可得到这个线程的JNIEnv结构体。这样就可以在后台线程中回调Java函数了
   2. 另外，后台线程退出前，需要调用JavaVM的DetachCurrentThread函数来释放对应的资源。

## 深入理解init
