# Git常用命令


## 基本命令

`git init` 初始化仓库

`git status` 查看当前状态

`git add` 添加到暂存区

`git commit -m "注释内容"` 提交至版本库


## log 回退版本

`git log` 查看commitID

`git log --pretty=oneline` commitID

`git reset --hard commitID`  回退版本

`git reset --hard origin/master` 强制用远程master的代码覆盖本地代码

​	hard 不保存所有变更

​	soft 保留变更且变更内容处于Staged（即已经commit）

​	mixed 保留变更且变更内容处于Modified

`git reflog` 查看最新的commitID


## 克隆 拉取 推送

`git clone 仓库地址` 克隆线上仓库

`git pull` 拉去线上仓库最新版本

`git push`  提交到线上仓库


## 分支

`git branch` 查看分支

`git branch 分支名` 创建分支

`git branch -d 分支名` 删除分支

`git checkout 分支名` 切换分支

`git chenkout -b 分支名` 创建并切换分支

`git checkout -b 分支名 模板名` 创建基于模板的分支并切换分支

`git checkout -b 分支名 origin 模板名` 创建基于模板的分支并切换分支

`git merge 被合并的分支名` 合并分支 


## 分支git push失败 需先设置上流分支

`git push --set-upstream origin 分支名`

## 分支改名

 远程分支改名步骤

`git branch -m oldName newName` 重命名远程分支对应的本地分支

`git push --delete origin oldName` 删除远程分支

`git push origin newName` 上传新命名的本地分支

`git branch --set-upstream-to origin/newName` 把修改后的本地分支与远程分支关联

## 本地仓库与远程分支的连接与断开 

`git remote` 查看remote

`git remote add origin repository_url` 添加远程仓库origin 连接的仓库为repository_url

`git remote set-url origin repository_url` 更改origin所连接的仓库 更改后的仓库为repository_url

`git remote set-url origin https://accessToken@github.com/V19931210/REPO.git` github携带Token

`git remote remove origin` 移除远程仓库origin


## 忽略文件

在当前目录下通过Git Bash 的touch指令 创建.gitignore文件 `touch .gitignore`

常见规则写法

/mtk/ 过滤整个文件夹

*.zip 过滤.zip文件

/mtk/do.c 过滤具体某个文件

!index.go 不过滤某个具体文件

