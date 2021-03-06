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
[史上最详细“截图”搭建Hexo博客并部署到Github-angelen10](http://jingyan.baidu.com/article/d8072ac47aca0fec95cefd2d.html)  
[HEXO+Github,搭建属于自己的博客-潘柏信](http://www.jianshu.com/p/465830080ea9)
[创建GitHub技术博客全攻略-铁锚的CSDN博客](http://blog.csdn.net/renfufei/article/details/37725057/)
## 安装Node
到[Node官网](https://nodejs.org)下载相应平台的最新版进行安装
## 安装Git
安装Git是为了将hexo的内容提交到github上,到[git下载网页](https://git-scm.com/download)下载相应平台的安装
## 申请Github账号
到[github官网](https://github.com/)注册,并选择Free免费账号完成设置
## 创建Repository(页面仓库)
到[仓库创建页面](https://github.com/new)创建与自己账号对应的账号分支,如damonxiong.github.io。  
创建仓库按如下图显示设置
![](http://img.blog.csdn.net/20140712125914603?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcmVuZnVmZWk=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
# hexo
[hexo官网](https://hexo.io/)  
[NexT文档](http://theme-next.iissnan.com/)  
[hexo博客更换主题-小道博客](http://www.tuicool.com/articles/zeIZJzv)

## hexo安装
### 安装
安装完成后,鼠标右键使用Git Bash Here 
![](搭建我的Blog/右键gitbashhere.png) 
或者直接打开cmd命令行操作
![](搭建我的Blog/cmd.png) 
输入命令：
<pre><code>npm install -g hexo</code></pre>  

> 注意：npm命令中-g代表全局安装  

### 创建自己的hexo目录并初始化
到自己喜欢的路径下创建文件夹，并进入到相应文件夹中，如下图：
![](搭建我的Blog/指定文件夹.png)  
输入命令:
<pre><code>hexo init</code></pre>

生成如下目录结构如下图:
![](搭建我的Blog/hexo-init目录.png)

### 安装依赖库
调用以下命令安装依赖库
<pre><code>npm install</code></pre>

### 生成默认静态测试helloWord
执行以下命令：
<pre><code>hexo generate</code></pre>

### 本地查看页面
执行以下命令：
<pre><code>hexo server</code></pre>

成功后，在浏览器中输入[http://localhost:4000](http://localhost:4000)访问。
正常情况下是可以的，但是有的电脑可能不行，我这边出现过4000端口被占用，可以在node_modules目录下的hexo-server目录下的index.js文件中修改端口配置，如下图：
![](搭建我的Blog/修改server的port.png)

重新执行命令，可以看到端口修改，使用相应的链接查看：
![](搭建我的Blog/端口修改后启动提示.png)

## hexo配置
### 资源文件夹使用
[在hexo中无痛使用本地图片-M-x codefalling](http://www.tuicool.com/articles/umEBVfI)
根据提示配置后，可以在写博客时使用本地图片。

### 标签(Tags)和分类(categories)

#### 添加方式
新建的marddown文件开始title区段中添加
<pre><code>categories: xxx
tags: 
  - tag1
  - tag2
</code></pre>

**注意点：**
1. 冒号后面要有空格
2. 要添加tags和categories页面
3. 主题的配置文件和站点的配置文件tags和categories的注释要打开

#### 添加标签
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

#### 添加分类
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

## hexo主题相关
在[官网主题](https://hexo.io/themes/)中有一些主题，可以自己根据喜好进行选择，我个人使用的是NexT主题
### NexT主题
主题安装配置参考[NexT主题主页](http://theme-next.iissnan.com/)，根据个人喜好配置

## hexo代码提交github
### 修改deploy配置
编辑站点配置文件，_config.yml，修改deploy字段下配置如下：
![](搭建我的Blog/deploy配置.png)  
> repository字段可以使用https链接，但是有时候会出现上传失败问题，上网查看了一些资料，将其修改为SSH方式就成功。

### 安装hexo-deployer-git
执行命令：
<pre><code>npm install hexo-deployer-git --save</code></pre>

> \-\-save将配置信息写入package.json中  

### 代码提交
执行命令：
<pre><code>hexo deploy</code></pre>

### 访问我的Blog
[DamonXiong's Blog](http://damonxiong.github.io)

# 编写博客
使用MarkDown编写文件
## MarkDown相关链接
[Cmd Markdown 编辑阅读器](https://www.zybuluo.com/mdeditor)  
[认识与入门 Markdown - 少数派](http://sspai.com/25137)  
[Markdown 语法说明(简体中文版)](http://wowubuntu.com/markdown/#list)  
