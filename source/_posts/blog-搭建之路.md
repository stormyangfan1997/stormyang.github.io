---
title: blog 搭建之路
date: 2018-10-12 09:33:02
tags: "blog"
---

# 我为什么选择搭建一个自己的blog？
1. 给自己找一个可以输出的地方，督促自己的输入。
2. 选择github是因为喜欢这里，这里是你需要去挖掘的宝藏
···

# 搭建准备

## 硬件环境

* 电脑 （我的是macair ，学生党。我的目标之一 赚钱买自己第一台mac pro）

## 软件环境

1. Github 账号
2. Git
3. Node.js
4. npm
5. hexo 

# 安装步骤

### 本地搭建

#### 安装 git
 在Mac OS X中自带Git， 不需要安装Git， 在Mac terminal中输入一下命令查看git版本


```
git --version
```

 
#### 安装[Node.js](https://nodejs.org/en/) 
 安装Node.js 的过程也会安装npm
![](https://ws4.sinaimg.cn/large/006tNbRwly1fw57i4g7orj30zq0p6dgu.jpg)


#### 安装Hexo


```
 sudo npm install -g hexo
```


输入可以查询hexo 版本号
```
 hexo -v
```


#### 初始化 hexo 


```
 hexo init
```

#### 安装依赖
在部署博客之前，需要安装依赖。

```
 npm install
```

#### 生成静态页面

```
 hexo generate
```

#### 启动服务

```
 hexo server
```

![](https://ws4.sinaimg.cn/large/006tNbRwly1fw57secbiej30i2022a9w.jpg)
浏览器打开输入网址就可以看到自己的本地blog了
ps：停止服务使用`CTRL+C`

### 部署到Github
#### 创建github账号
#### 创建repository
1. 登录 GitHub 个人账号以后，在首页右上角会有 New repository 按钮，点击按钮会出现下图所示界面：![](https://ws4.sinaimg.cn/large/006tNbRwly1fw57xa5r8jj31480ywgmp.jpg)
2. Repository name 的格式必须是：yourGitHubId.github.io，例如我的是：lijiankun24.github.io；
3. Description 可以为空；
4. 免费服务的话，只能选择 Public (公开的)
#### 安装git 部署器
```
npm install hexo-deployer-git -save
```
#### 修改配置文件
在 hexo 的根目录下会有 _config.yml 文件，打开 _config.yml 文件，在文件最末尾，修改如下配置：![](https://ws1.sinaimg.cn/large/006tNbRwly1fw581t6ea2j30vi05ot96.jpg)
#### 部署
在 hexo 目录下执行以下命令， 即可完成对将静态博客部署到 GitHub 上
```
hexo deploy
```
部署成功以后，在浏览器中输入 http://yourname.github.io 即可在线浏览自己的博客啦~
