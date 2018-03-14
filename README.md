主题样式来至[阮一峰](http://www.ruanyifeng.com/blog/)的博客。

<!--more-->

## 基本使用

```git 
git clone 
```

```js
根目录配置  theme: ryf
```



## 主题配置

资源文件都在source文件里。

```
 favicon: /favicon.ico     //配置网页ico
 avatar: /avatar.jpg       //头像
 keywords: 当然我没扯淡,DE清平  // 网站关键字
 highlight_theme: github-gist // 高亮样式，详细见下
 github: https://github.com/duzhihao-github //github地址
 weibo: https://weibo.com/u/1783756832/home?wvr=5#_loginLayer_1521011243864
//微博地址

//资源文件目录，如要修改主题<%- url_for(theme.css)%>表示css文件夹其他同理。
css: css
js: js
img: images
```

## 根目录配置

```
title: 当然我没扯淡   //网站标题

subtitle: DE清平的博客 // 网站副标题

description: 吾将上下而求索...  //个人简介

author: DE清平 // 作者名字

```

```
首页能显示多少篇文章取决于per_page的值
index_generator:
  path: ''  
  per_page: 20
  order_by: -date
```

```
这个配置设置为0，不然会导致文章数目显示不全
per_page: 0
pagination_dir: page
```

## 代码高亮

首先把根目录的代码高亮关闭

```
highlight:
  enable: false
  line_number: false
  auto_detect: false
```

到[这里](https://highlightjs.org/)下载你想要的css样式，放到css文件夹中。在主题配置文件中

```
highlight_theme: github-gist  //你下载的css文件名
```

## 补充

首页默认显示的最新的文章。摘要写在文章的` <!--more-->`之前。