---
layout: post
title: Linux下Git和GitHub使用方法
category: git & github
tags: [git & github]
---

## Git环境的搭建

### 安装前的准备

* 检查是否安装ssh,如果没有则安装
* 检查是否存在ssh公钥

```
$ cd ~/.ssh
```

### 安装Git

```
$ sudo apt-get install git
```

### 生成ssh公钥

```
$ ssh-keygen -t rsa -C [sample@mail.com]
```

### 将公钥添加到github

打开github，找到账户里面添加SSH，把~/.ssh/idrsa.pub的内容复制到key里面。

### 测试是否生效

```
$ ssh -T git@github.com
balabala...
// 输入yes
Hi username! 
You've successfully authenticated, but GitHub does not provide shell access.
// 连接成功
```

## git常见命令

### 创建代码库

```
// 在当前目录新建一个Git代码库
$ git init
// 下载项目及历史代码
$ git clone [url]
```

### 配置Git

Git的设置文件为.gitconfig，它可以在用户主目录下（全局配置），也可以在项目目录下（项目配置）。

```
// 显示当前的Git配置
$ git config --list
// 配置用户名
$ git config --global user.name [your_name]
// 配置email
$ git config --global user.email [your_email]
```

### 将修改提交到暂存区

```
// 添加指定文件
$ git add [file1] [file2] ...
// 添加指定目录，包括子目录
$ git add [dir]
// 添加当前目录的所有文件到暂存区
$ git add .
```

### 将修改提交到版本库

```
// 提交暂存区到版本库
$ git commit -m [message]
// 提交暂存区的指定文件到版本库
$ git commit [file1] [file2] ... -m [message]
// 提交工作区自上次commit之后的变化，直接到版本库
$ git commit -a
// 提交时显示所有diff信息
$ git commit -v
```

### git分支与版本管理

```
// 列出所有本地分支
$ git branch
// 列出所有远程分支
$ git branch -r
// 列出所有本地分支和远程分支
$ git branch -a
// 新建一个分支，但依然停留在当前分支
$ git branch [branch-name]
// 新建一个分支，并切换到该分支
$ git checkout -b [branch]
// 新建一个分支，指向指定commit
$ git branch [branch] [commit]
// 新建一个分支，与指定的远程分支建立追踪关系
$ git branch --track [branch] [remote-branch]
// 切换到指定分支，并更新工作区
$ git checkout [branch-name]
// 切换到上一个分支
$ git checkout -
# 建立追踪关系，在现有分支与指定的远程分支之间
$ git branch --set-upstream [branch] [remote-branch]
// 合并指定分支到当前分支
$ git merge [branch]
// 选择一个commit，合并进当前分支
$ git cherry-pick [commit]
// 删除分支
$ git branch -d [branch-name]
// 删除远程分支
$ git push origin --delete [branch-name]
$ git branch -dr [remote/branch]
```

### git标签管理

```
// 列出所有tag
$ git tag
// 新建一个tag在当前commit
$ git tag [tag]
// 新建一个tag在指定commit
$ git tag [tag] [commit]
// 删除本地tag
$ git tag -d [tag]
// 删除远程tag
$ git push origin :refs/tags/[tagName]
// 查看tag信息
$ git show [tag]
// 提交指定tag
$ git push [remote] [tag]
// 提交所有tag
$ git push [remote] --tags
// 新建一个分支，指向某个tag
$ git checkout -b [branch] [tag]
```

### git查看信息

```
// 显示有变更的文件
$ git status
// 显示当前分支的版本历史
$ git log
// 显示commit历史，以及每次commit发生变更的文件
$ git log --stat
// 搜索提交历史，根据关键词
$ git log -S [keyword]
// 显示某个commit之后的所有变动，每个commit占据一行
$ git log [tag] HEAD --pretty=format:%s
// 显示某个commit之后的所有变动，其"提交说明"必须符合搜索条件
$ git log [tag] HEAD --grep feature
// 显示某个文件的版本历史，包括文件改名
$ git log --follow [file]
$ git whatchanged [file]
// 显示指定文件相关的每一次diff
$ git log -p [file]
// 显示过去5次提交
$ git log -5 --pretty --oneline
// 显示所有提交过的用户，按提交次数排序
$ git shortlog -sn
// 显示指定文件是什么人在什么时间修改过
$ git blame [file]
// 显示暂存区和工作区的差异
$ git diff
// 显示暂存区和上一个commit的差异
$ git diff --cached [file]
// 显示工作区与当前分支最新commit之间的差异
$ git diff HEAD
// 显示两次提交之间的差异
$ git diff [first-branch]...[second-branch]
// 显示今天你写了多少行代码
$ git diff --shortstat "@{0 day ago}"
// 显示某次提交的元数据和内容变化
$ git show [commit]
// 显示某次提交发生变化的文件
$ git show --name-only [commit]
// 显示某次提交时，某个文件的内容
$ git show [commit]:[filename]
// 显示当前分支的最近几次提交
$ git reflog
```

### github代码提交

```
// 下载远程仓库的所有变动
$ git fetch [remote]
// 显示所有远程仓库
$ git remote -v
// 显示某个远程仓库的信息
$ git remote show [remote]
// 增加一个新的远程仓库，并命名
$ git remote add [shortname] [url]
// 取回远程仓库的变化，并与本地分支合并
$ git pull [remote] [branch]
// 上传本地指定分支到远程仓库
$ git push [remote] [branch]
// 强行推送当前分支到远程仓库，即使有冲突
$ git push [remote] --force
// 推送所有分支到远程仓库
$ git push [remote] --all
```

### 撤销修改

```
// 恢复暂存区的指定文件到工作区
$ git checkout [file]
// 恢复某个commit的指定文件到暂存区和工作区
$ git checkout [commit] [file]
// 恢复暂存区的所有文件到工作区
$ git checkout .
// 重置暂存区的指定文件，与上一次commit保持一致，但工作区不变
$ git reset [file]
// 重置暂存区与工作区，与上一次commit保持一致
$ git reset --hard
// 重置当前分支的指针为指定commit，同时重置暂存区，但工作区不变
$ git reset [commit]
// 重置当前分支的HEAD为指定commit，同时重置暂存区和工作区，与指定commit一致
$ git reset --hard [commit]
// 重置当前HEAD为指定commit，但保持暂存区和工作区不变
$ git reset --keep [commit]
// 新建一个commit，用来撤销指定commit
// 后者的所有变化都将被前者抵消，并且应用到当前分支
$ git revert [commit]
// 暂时将未提交的变化移除，稍后再移入
$ git stash
$ git stash pop
```
