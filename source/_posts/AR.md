---
title: AR
date: 2021-06-06 10:11:11
categories: 技术笔记
tags:
 - AR
---

# 资料
1. [ARCode Gooogle](https://developers.google.com/ar)
2. [Google AR的ARCore下载地址及国内支持的设备](https://zhuanlan.zhihu.com/p/61970665)
3. [WebXR Device API](https://caniuse.com/webxr)
4. [HuaWei AR Engine](https://developer.huawei.com/consumer/cn/hms/huawei-arengine/)
5. [Snap CTO专访：AR内容是未来，不只是社交工具那么简单](https://zhuanlan.zhihu.com/p/76551998)
6. [AR特效相机：设计原则和设计架构](http://www.woshipm.com/pd/4120522.html)
7. [AR引擎技术选型和使用实现方案](https://gameinstitute.qq.com/community/detail/133606)
   
# 调研汇总
    查找资料大部分AR引擎都是Android使用ARCode，iOS使用ARKit；查看ARCode发现有兼容iOS的demo，目前采用ARCode的android和ios sdk example已经都可以实现狐狸面嵌套人脸，Android实现头盔跟随人脸，但是头盔位置还有点问题，需要细调。目前UTU使用的3d显示是modelviewer组件，这个组件是兼容ARCode。因此临时demo建议使用ARCode开发。目前ARCode的demo只能使用一张纹理图片，多张纹理图片渲染需要重新编码，这块需要较长时间。简单显示不知道是否能够满足demo要求

