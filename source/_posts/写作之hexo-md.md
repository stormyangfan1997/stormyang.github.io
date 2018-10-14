---
title: 写作之hexo.md
date: 2018-10-14 14:21:45
tags:
- 写作
- hexo
categories:
- hexo
---


今天比较系统的记录hexo 创建一篇新文章

<!--more-->

## 命令格式

```
hexo new [layout] <title>

```
`layout`表示你可以指定新建文章的格式，默认是`post`.也可以通过修改配置文件`_config.yml`中的`default_layout`参数来指定默认布局。
## 布局(layout)
hexo 有三种默认布局`post`,`page`,`draft`,它们对于不同的路径，但自定义的布局都将存储在`source/_post`文件夹中。
| **布局** | **路径** |
| --- | --- |
| `post` | `source/_post` |
| `page` | `source` |
| `draft` | `source/_drafts` |
>**不处理我的文章**
>如何你不想你的文章被处理， 你可以将 Front-Matter 中的`layout：`设置成`false`


## 草稿(draft)
建立的`draft`文稿在`source/_draft`中，可以通过`publish`命令将草稿移到`source/_posts`中。

```
hexo publish [layout] <title>
```
## 模板(scaffold)

在新建文稿时，hexo 会根据`scaffolds`文件夹中寻找相应的文件来建立文件，例如
```
hexo new photo "my gallary"
```
在执行这个命令时，hexo 会尝试在`scaffolds`文件夹中寻找`photo.md`.并根据其内容建立文章。

<!--more-->

## 命令格式

```
hexo new [layout] <title>

```
`layout`表示你可以指定新建文章的格式，默认是`post`.也可以通过修改配置文件`_config.yml`中的`default_layout`参数来指定默认布局。
## 布局(layout)
hexo 有三种默认布局`post`,`page`,`draft`,它们对于不同的路径，但自定义的布局都将存储在`source/_post`文件夹中。

| **布局** | **路径** |
| --- | --- |
| `post` | `source/_post` |
| `page` | `source` |
| `draft` | `source/_drafts` |

>**不处理我的文章**
>如何你不想你的文章被处理， 你可以将 Front-Matter 中的`layout：`设置成`false`


## 草稿(draft)
建立的`draft`文稿在`source/_draft`中，可以通过`publish`命令将草稿移到`source/_posts`中。

```
hexo publish [layout] <title>
```
## 模板(scaffold)

在新建文稿时，hexo 会根据`scaffolds`文件夹中寻找相应的文件来建立文件，例如
```
hexo new photo "my gallary"
```
在执行这个命令时，hexo 会尝试在`scaffolds`文件夹中寻找`photo.md`.并根据其内容建立文章。


