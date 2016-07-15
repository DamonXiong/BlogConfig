---
title: 搭建我的Blog
date: 2016-07-15 16:32:55
categories: 工具
tags: 
  - hexo
  - github
---

# 简述

近期开始写博客,搜索之后使用hexo和github进行搭建自己的博客,期间出现了问题,仅以做为记录

# 运行环境
### 安装NodeJS
### 安装Git
### 申请Github账号

## 参考链接
[史上最详细“截图”搭建Hexo博客并部署到Github-angelen10](http://jingyan.baidu.com/article/d8072ac47aca0fec95cefd2d.html)
[HEXO+Github,搭建属于自己的博客-潘柏信](http://www.jianshu.com/p/465830080ea9)
[hexo博客更换主题-小道博客](http://www.tuicool.com/articles/zeIZJzv)


```
tags:
  - tag1
  - tag2
categories: xxx
```

冒号后面要有空格  
应该在 ---之上，---下面是页面内容  
令：要添加tags和categories页面；且主题的配置文件和站点的配置文件tags和categories的注释要打开

## 添加标签

hexo new page tags  
确认站点配置文件里有tag_dir: tags  
确认主题配置文件里有tags: /tags  
编辑站点的source/tags/index.md，添加

<button class="selectCode btn btn-xs">全选</button>

<button href="javascript:void(0);" class="copyCode btn btn-xs" data-clipboard-text="title: tags
date: 2015-10-20 06:49:50
type: &quot;tags&quot;
comments: false" data-toggle="tooltip" data-placement="bottom" title="">复制</button>

## 添加分类

hexo new page categories  
确认站点配置文件里有category_dir: categories  
确认主题配置文件里有categories: /categories  
编辑站点的source/categories/index.md，添加

<button class="selectCode btn btn-xs">全选</button>

<button href="javascript:void(0);" class="copyCode btn btn-xs" data-clipboard-text="title: categories
date: 2015-10-20 06:49:50
type: &quot;categories&quot;
comments: false" data-toggle="tooltip" data-placement="bottom" title="">复制</button>

<button href="javascript:void(0);" class="saveToNote btn btn-xs">放进笔记</button>