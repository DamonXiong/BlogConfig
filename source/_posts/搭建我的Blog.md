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
## 安装NodeJS
## 安装Git
## 申请Github账号
# hexo配置
## 标签(Tags)和分类(categories)

### 添加方式
新建的marddown文件开始title区段中添加
<pre><code>categories: xxx
tags: 
  \- tag1
  \- tag2
</code></pre>

> 注意点：
1. 冒号后面要有空格
2. 要添加tags和categories页面
3. 主题的配置文件和站点的配置文件tags和categories的注释要打开

### 添加标签
确认站点配置文件里有tag_dir: tags  
确认主题配置文件里有tags: /tags 
输入命令：
<pre><code>hexo new page tags</code></pre>
编辑站点的source/tags/index.md，添加
<pre><code>
---
title: tags
date: 2015-10-20 06:49:50
type: "tags"
comments: false
---
</code></pre>

### 添加分类
确认站点配置文件里有category_dir: categories  
确认主题配置文件里有categories: /categories
输入命令：
<pre><code>hexo new page categories</code></pre>
编辑站点的source/tags/index.md，添加
<pre><code>
---
title: categories
date: 2015-10-20 06:49:50
type: "categories"
comments: false
---
</code></pre>

## 参考链接
[史上最详细“截图”搭建Hexo博客并部署到Github-angelen10](http://jingyan.baidu.com/article/d8072ac47aca0fec95cefd2d.html)
[HEXO+Github,搭建属于自己的博客-潘柏信](http://www.jianshu.com/p/465830080ea9)
[hexo博客更换主题-小道博客](http://www.tuicool.com/articles/zeIZJzv)