---
title: 搭建blog遇到的坑
date: 2018-10-13 12:42:44
tags:
- blog
categories:
- 搭建blog
---
这里记录了为在完善blog 中遇到的问题···

<!-- more -->

### hexo 文章无法折叠

- 官网推荐了三种方法，我就记录我用的这一种
> 在你想要折叠的地方加`<!-- more -->`
* 要注意的是，折叠不能出现在文章开头，否则就会被视为无效：
![](https://pic4.zhimg.com/80/c52da62fc27f69e5ab028642ad34910f_hd.png)

### 修改头像

1. 首先先把头像 存放在`themes/next/source/images/`目录下
2. 修改配置`themes/next/_config.yml` ，搜索`avatar` 将`url`注释`#`去掉,并把地址改为你刚才存放images 的地址。

### 百度统计

* 建议直接参考官方文档：[Next主题百度统计](http://theme-next.iissnan.com/getting-started.html#analysis-system-baidu)

* 建议么事多看看官方文档，比较权威

### 


