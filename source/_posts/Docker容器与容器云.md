---
title: Docker容器与容器云
date: 2022-03-20 16:02:55
categories: 服务器
tags:
    - Docker
    -  K8s
---

# 学习参考链接
1. [Docker - 从入门到实践](https://yeasy.gitbook.io/docker_practice/)
2. [awesome docker-compose example](https://github.com/docker/awesome-compose)

# 学习摘要
1. Docker通过namesapce实现了资源隔离，通过cgroups实现了资源限制，通过写时复制机制（copy-on-write）实现了高效的文件操作
2. Linux内核实现namesapce的一个主要目的就是实现轻量级虚拟化（容器）服务，针对的是Linux内核3.8及以后版本
3. namesapce的6项隔离
   
| namesapce | 系统调用参数 | 隔离内容 |
| :------: | :------: | :------: |
| UTS（UNIX Time-sharing System） | CLONE_NEWUTS | 主机名与域名 |
| IPC（Inter-Process Communication） | CLONE_NEWIPC | 信号量、消息队列和共享内存 |
| PID | CLONE_NEWPID | 进程编号 |
| Network | CLONE_NEWNET | 网络设备、网络栈、端口等 |
| Mount | CLONE_NEWNS | 挂载点（文件系统） |
| User | CLONE_NEWUSER | 用户和用户组 |
4. namesapce的API包括clone()\setns()\unshare()，还有/proc下的部分文件
5. clone创建进程和namespace实际上是Linux系统调用fork的一种更通用的实现方式，可以通过flags控制使用多少功能
6. setns加入已经存在的namespace
7. unshare在原先进程进行namespace隔离
8. IPC namespace中实际上包含了系统IPC标识符以及实现POSIX消息队列的文件系统
9. 