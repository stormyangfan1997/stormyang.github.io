---
title: blog搭建之路
date: 2018-10-13 11:50:49
tags:
- blog
categories:
- 搭建blog
---
这里记录我搭建blog 的全过程！
<!-- more -->
# 我为什么选择搭建一个自己的blog？
1. 给自己找一个可以输出的地方，督促自己的输入。
2. 选择github是因为喜欢这里，这里是你需要去挖掘的宝藏
  ···
# 搭建准备
## 硬件环境
* 电脑
## 软件环境
1. GitHub 账号
2. Git
3. Node.js
4. npm
5. hexo 
## 本地搭建

### 安装 git
mac  下自带git
```
git -- version \\ 查询版本
```

### 安装[Node.js](https://nodejs.org/en/)
安装Node.js 的过程也会安装npm
![](https://ws4.sinaimg.cn/large/006tNbRwly1fw57i4g7orj30zq0p6dgu.jpg)

### 安装hexo
```
sudo npm install -g hexo \\ 安装
hexo -v			  \\版本	
```
### 初始化hexo

```
hexo init
```
### 安装依赖
在部署blog 前 需要安装依赖

```
npm install
```
### 生成静态页面

```
hexo generate
```

### 启动服务

```
hexo server
```
![](https://ws4.sinaimg.cn/large/006tNbRwly1fw57secbiej30i2022a9w.jpg)
看图提示就可以看自己的本地blog 了


## 部署到GitHub
### 创建账号
后期补上

### 创建 repository
1. 登录 GitHub 个人账号以后，在首页右上角会有 New repository 按钮，点击按钮>    会出现下图所示界面：![](https://ws4.sinaimg.cn/large/006tNbRwly1fw57xa5r8jj31480ywgmp.jpg）
2. Repository name 的格式必须是：yourGitHubId.github.io，例如我的是：lijiank    un24.github.io；
3. Description 可以为空；
4. 免费服务的话，只能选择 Public (公开的)

### 安装git  部署器
```
npm install hexo-deployer-git -save
```
### 修改配置文件
在 hexo 的根目录下会有 _config.yml 文件，打开 _config.yml 文件，在文件最末 ，修改如下配置：![](https://ws1.sinaimg.cn/large/006tNbRwly1fw581t6ea2j30vi05ot96.jpg)
### 部署
 在 hexo 目录下执行以下命令， 即可完成对将静态博客部署到 GitHub 上
```
hexo deploy
```
部署成功以后，浏览器中输入 http://yourname.github.io 即可在线浏览自己的博客了



## 备份本地blog
### 为什么需要备份呢？
1. 万一自己换电脑呢？
2. 万一本地blog 丢失呢？ 你要明白我们上传的多是处理过的静态html
### 方法一 远程仓库创建分支
![](https://pic2.zhimg.com/80/v2-fac8f8564c4f1de0c54e3c142ae1f81d_hd.png)
#### 仓库创建hexo分支 并设置默认分支
> 在Github的username.github.io仓库上新建一个xxx分支，并切换到该分支，并在该仓库->Settings->Branches->Default branch中将默认分支设为xxx，save保存；然后将该仓库克隆到本地，进入该username.github.io文件目录。
![](https://upload-images.jianshu.io/upload_images/2859254-01cb597e80e5005b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/990/format/webp)
![](https://upload-images.jianshu.io/upload_images/2859254-67ed8c22531dd66d.png?imageMogr2/auto-orient/)
#### 克隆远程仓库
```
git clone git@github.com:username/username.github.io.git 
```
1. 进入刚才clone 的仓库 将`.git`复制到blog 根目录
2. 将博客目录下`themes`文件夹下每个主题文件夹离面的`.git,.gitignor`删掉。如果不删除么有办法备份该文件夹。
3.`cd`到博客目录，
```
git add -A
git commit -m "modify my blog"
git push origin hexo
```
这样就可以把blog 更新到`hexo`分支里面
4. 在新电脑上操作 先把电脑上环境安装好 创建好`blog`目录 
```
 git clone git@github.com:username/username.github.io.git
```
5. `cd`到`blog ` 下执行
```
npm install 
hexo g && hexo s
```
便可
```
