---
title: Git 常用命令
date: 2017-05-22 15:17:24
tags: 
    - git
---

## 安装
#### 源码安装：
先安装依赖库
```
$ sudo yum install curl-devel expat-devel gettext-devel \
   openssl-devel zlib-devel
$ sudo apt-get install libcurl4-gnutls-dev libexpat1-dev gettext \
   libz-dev libssl-dev
```
为了能够添加更多格式的文档（如 doc, html, info），安装依赖包：
```
$ sudo yum install asciidoc xmlto docbook2x
$ sudo apt-get install asciidoc xmlto docbook2x
```
编译安装：
```
$ tar -zxf git-2.0.0.tar.gz
$ cd git-2.0.0
$ make configure
$ ./configure --prefix=/usr
$ make all doc info
$ sudo make install install-doc install-html install-info
```
更新
```
$ git clone git://git.kernel.org/pub/scm/git/git.git
```
## 常用命令
| 命令 | 描述 |
|------|------|
|`git init`|创建版本库|
|`git add <file>`| 把文件添加到仓库 |
|`git add -A`| 全部添加到仓库 |
|`git commit -m "message"`|提交到仓库，并添加描述|
|`git status`|查看当前仓库状态|
|`git diff`|查看修改|
|`git log`|查看提交历史|