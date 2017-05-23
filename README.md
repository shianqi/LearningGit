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
更新 git
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
|`git diff`|工作区(work dict)和暂存区(stage)的比较|
|`git diff --cached`|暂存区(stage)和分支(master)的比较|
|`git diff HEAD -- <file>`|查看工作区和版本库里面最新版本的区别|
|`git log`|查看提交历史|
|`git reflog`|记录操作命令|
|`git reset --hard HEAD~n`|回退n个版本|
|`git reset --hard $id`|回到 $id 版本|
|`git checkout -- <file>`|丢弃工作区的修改|
|`git reset HEAD <file>`|把暂存区的修改撤销掉|

## 远程命令

| 命令 | 描述 |
|------|------|
|`git remote add origin <git@address>`|关联远程库|
|`git push -u origin master`|把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来|
|`git push origin master`|推送到远程|
|`git clone <git@address>`|克隆远程库到本地|

## 分支管理
| 命令 | 描述 |
|------|------|
|`git branch`|查看分支信息，带*为当前|
|`git checkout -b <branch-name>`|创建并切换到新分支|
|`git branch <branch-name>`|创建分支|
|`git checkout <branch-name>`|切换分支|
|`git merge <branch-name>`|合并某分支到当前分支|
|`git branch -d <branch-name>`|删除分支|
|`git log --graph`| 查看分支合并图 |

fix bug
