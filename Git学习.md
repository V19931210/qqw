# Git常用命令



`git init` 初始化仓库


`git status` 查看当前状态

`git add` 添加到暂存区

`git commit -m "注释内容"` 提交至版本库



`git log` 查看commitID

`git log --pretty=oneline` commitID

`git reset --hard commitID`  回退版本

​	hard 不保存所有变更

​	soft 保留变更且变更内容处于Staged（即已经commit）

​	mixed 保留变更且变更内容处于Modified

`git reflog` 查看最新的commitID

`git pull` 拉去线上仓库最新版本



`git clone 仓库地址` 克隆线上仓库

`git push`  提交到线上仓库



分支相关指令

`git branch` 查看分支

`git branch 分支名` 创建分支

`git branch -d 分支名` 删除分支

`git checkout 分支名` 切换分支

`git chenkout -b 分支名` 创建并切换分支

`git checkout -b 分支名 模板名` 创建基于模板的分支并切换分支

`git checkout -b 分支名 origin 模板名` 创建基于模板的分支并切换分支

`git merge 被合并的分支名` 合并分支 



分支git push失败 需先设置上流分支

`git push --set-upstream origin 分支名`



忽略文件

在当前目录下通过Git Bash 的touch指令 创建.gitignore文件 `touch .gitignore`

常见规则写法

/mtk/ 过滤整个文件夹

*.zip 过滤.zip文件

/mtk/do.c 过滤具体某个文件

!index.go 不过滤某个具体文件

