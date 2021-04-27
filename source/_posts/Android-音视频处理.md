---
title: Android-音视频处理
date: 2019-03-10 16:21:46
categories: 技术笔记
tags:
   - Android
   - 音视频
---
# 参考链接
[移动端音频视频入门](https://www.imooc.com/learn/959)  
[Android互动直播APP开发入门](https://www.imooc.com/learn/923)

# 架构图
![实时互动直播架构](.\Android-音视频处理\实时互动直播架构.png)  

![泛娱乐化直播架构](.\Android-音视频处理\泛娱乐化直播架构.png)

# CDN网络
## 来历
解决用户访问网络资源慢产生的技术。
### 产生原因
1. 链路过长导致，任何节点等出现问题，用户体验效果很差
2. 人为因素，运营商之间切割

## CDN构成
1. 边缘节点：用户从边缘节点上获取数据
2. 二级节点：主干网节点，主要用于缓存，减轻源站压力
3. 源站：CP（内容提供方）将内容放到源站

## CDN网络
![CDN网络](.\Android-音视频处理\CDN网络.png)
1. 传统CDN，追求热点，拉取方式
2. 音视频CDN，源push主干，边缘pull主干

## 搭建直播系统
1. ffmpeg
2. ffplay
3. flashplayer（RTMP协议解析）

### 搭建流媒体服务
1. 准备流媒体服务器（linux或MAC）
2. 编译并安装Nginx
3. 配置RTMP服务并启动Nginx服务
   
### ffmpeg命令
1. 推流：  
    `ffmpeg -re -i out.mp4 -c copy -f flv rtmp://server/live/streamName`
2. 拉流：  
   `ffmpeg -i rtmp://server/live/streamName -c copy dump.flv`

3. flash播放器  
   `http://bbs.chinaffmpeg.com/1.swf`

# 音频入门
## 声音三要素
1. 音调：就是音频，高音区和低音区
2. 音量：声音振动的幅度
3. 音色：与材质有关，本质就是谐波
   ![音色](.\Android-音视频处理\音色.png)
## 量化和编码
### 音频量化过程
![音频量化过程](.\Android-音视频处理\音频量化过程.png)

### 量化基本概念
1. 采样大小：一个采样用多少bit存放。常用16bit
2. 采样率：8k、16k、32k、44.1k、48k
3. 声道数：单声道、双声道、多声道
### 码率计算
采样率 * 采样大小 * 声道数




