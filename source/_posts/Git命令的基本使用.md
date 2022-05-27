---
title: Git命令的基本使用
excerpt: Git操作项目、Git分支管理以及Git合并、提交、回滚等
sticky: 100
date: 2020-07-11 23:12:39
update: 2022-05-03 17:14:00
categories: 
  - Git
tags:
  - Git
  - 技术
---

# Git基本操作
> Git学习参考：
> 
> https://git-scm.com/book/zh/v2

## 一、Git操作本地项目
### 1. 初始化仓库
先进入项目文件夹，通过命令 git init 把这个目录变成git可以管理的仓库
```bash
git init
```
### 2. 查看仓库状态
```bash
git status
```
### 3. 把更新的文件添加到版本库中
使用命令 git add .添加到暂存区里面去，不要忘记后面的小数点 "."，意为添加文件夹下的所有文件
```bash
git add .
```
### 4. 提交更新
用命令 git commit告诉Git，把文件提交到仓库。引号内为提交说明。
```bash
git commit -m 'first commit'
```
### 5. 查看提交记录
```bash
git log
git log -p <file>
git blame <file>
```
### 6. commit之前查看更新内容，文件差异
```bash
git diff
```
## 二、Git分支管理
### 1. Git查看分支
```bash
$ git branch -a
* main
  master
  remotes/origin/main
```
### 2. 查看每一个分支的最后一次提交
```bash
$ git branch -v
  iss53   93b412c fix javascript issue
* master  7a98805 Merge branch 'iss53'
  testing 782fd34 add scott to the author list in the readmes
```
### 3. Git创建切换分支
创建本地分支，并切换到分支：
```bash
# 新建与合并
$ git checkout -b iss53
Switched to a new branch "iss53"

# 它是下面两条命令的简写：
# 创建分支
$ git branch iss53
# 切换分支
$ git checkout iss53
```
### 4. 删除分支：
#### (1) 查看所有分支
```bash
$ git branch -a
* main
  master
  remotes/origin/main
```
#### (2) 删除本地分支
```bash
git branch -D BranchName

其中-D也可以是--delete，如：

git branch --delete BranchName
```
#### (3) 删除本地的远程分支(解除关联)
```bash
# 先查看查看远程库信息
$ git remote -v
origin  git@github.com:xxx/xxx.git (fetch)
origin  git@github.com:xxx/xxx.git (push)
# 然后，根据名字删除，比如删除origin：
$ git remote rm origin
```
#### (4) 远程删除Git服务器上的分支
```bash
git push origin -d BranchName

其中-d也可以是--delete，如：

git push origin --delete BranchName

注意：git命令区分大小写，例如-D和-d在不同的地方虽然都是删除的意思，并且它们的完整写法都是--delete，但简易写法用错大小写会执行失败。
```
## 三、Git操作远程项目
### 1. Git关联远程项目
```bash
git remote add origin 你的远程库地址。
如：
git remote add origin https://github.com/xxx/xxx.git
```
> 注：“origin” 并无特殊含义
>
> 远程仓库名字 “origin” 与分支名字 “master” 一样，在 Git 中并没有任何特别的含义一样。 同时 “master” 是当你运行 `git init` 时默认的起始分支名字，原因仅仅是它的广泛使用， “origin” 是当你运行 `git clone` 时默认的远程仓库名字。 如果你运行 `git clone -o booyah`，那么你默认的远程分支名字将会是 `booyah/master`。

### 2. Git获取远程库与本地同步合并
push之前先pull远程代码，如果远程库不为空必须做这一步，否则后面的提交会失败。
```bash
git pull --rebase origin develop
```
或者：
```bash
git pull origin develop
```
### 3. 把本地库的内容推送到远程
使用 git push命令，实际上是把当前分支develop推送到远程。第一次推送内容使用如下命令，执行此命令后会要求输入用户名、密码，验证通过后即开始上传。
```bash
git push -u origin develop
```
以后提交可以使用：
```bash
git push origin serverfix
```
> 这里有些工作被简化了。 Git 自动将 `serverfix` 分支名字展开为 `refs/heads/serverfix:refs/heads/serverfix`， 那意味着，“推送本地的 `serverfix` 分支来更新远程仓库上的 `serverfix` 分支。” 你也可以运行 `git push origin serverfix:serverfix`， 它会做同样的事——也就是说“推送本地的 `serverfix` 分支，将其作为远程仓库的 `serverfix` 分支” 可以通过这种格式来推送本地分支到一个命名不相同的远程分支。 如果并不想让远程仓库上的分支叫做 `serverfix`，可以运行 `git push origin serverfix:awesomebranch` 来将本地的 `serverfix` 分支推送到远程仓库上的 `awesomebranch` 分支。

## 四、Git Clone远程代码
```bash
git clone https://github.com/xxx/xxx.git
```
clone远程仓库到制定目录：
```bash
git clone xxx.git "指定目录"
```

## 五、Git合并分支
### 1.查看分支

$ git branch
* master
  newtest

### 2.合并某分支到当前分支：git merge <name>

$ git merge newtest

### 3.合并完之后就可以删除掉不需要的分支了

$ git branch -d newtest
Deleted branch newtest (was c1501a2).

### 4.关于merge回滚操作参考：

 https://blog.csdn.net/adsl624153/article/details/81155664

### 5.执行完merge操作后，没有修改代码

#### ⑴ 查看merge操作的上一个提交记录的版本号

git reflog

#### ⑵ 回滚到merge之前的状态

git reset --hard 版本号

> 参考：https://blog.csdn.net/songxi_bo/article/details/123384233
>
> 回退命令：
> $ git reset --hard HEAD^ 回退到上个版本
> $ git reset --hard HEAD~3 回退到前3次提交之前，以此类推，回退到n次提交之前
> $ git reset --hard commit_id 退到/进到 指定commit的sha码
>
> 强推到远程：
>
> $ git push origin HEAD --force



## 六、Git 回滚操作

> 参考：https://www.jianshu.com/p/c55958563f5a

Git撤销&回滚操作(git reset 和 get revert)
Git 的工作流
工作区：在 git add xx 之前，在自己当前分支所修改的代码内容！
暂存区：已经 git add xxx 进去，且没有执行 git commit xxx 的。
本地分支：已经 git commit -m xxx 提交到本地分支的。
远程分支：git push origin HEAD:refs/for/master HEAD 是本地，master是远程分支

代码回滚
在上传代码到远程仓库的时候，不免会出现问题，任何过程都有可能要回滚代码：

1、在工作区的代码（checkout ~ 修改工作区文件）
git checkout -- a.txt # 丢弃某个文件，或者
git checkout -- . # 丢弃全部

注意：git checkout – . 丢弃全部，也包括：新增的文件会被删除、删除的文件会恢复回来、修改的文件会回去。这几个前提都说的是，回到暂存区之前的样子。对之前保存在暂存区里的代码不会有任何影响。对commit提交到本地分支的代码就更没影响了。当然，如果你之前压根都没有暂存或commit，那就是回到你上次pull下来的样子了。

2、代码 git add 到缓存区，并未 git commit 提交（reset ~ 修改暂存区文件）
git reset HEAD .
git reset HEAD a.txt

注意：这个命令仅改变暂存区，并不改变工作区，这意味着在无任何其他操作的情况下，
工作区中的实际文件同该命令运行之前 无任何变化

3、代码 git commit 到本地分支，但没有 git push 到远程 （git reset --hard ~ commit 之后）
git log # 得到你需要回退一次提交的commit id
git reset --hard <commit_id> # 回到其中你想要的某个版本
git reset --hard HEAD^ # 回到最新的一次提交
git reset HEAD^ # 此时代码保留，回到 git add 之前

4、代码 git push 把修改提交到远程仓库 (git reset || git revert)
（1）通过git reset是直接删除指定的commit
git log # 得到你需要回退一次提交的commit id
git reset --hard <commit_id>
git push origin HEAD --force # 强制提交一次，之前错误的提交就从远程仓库删除

(2) 通过git revert是用一次新的commit来回滚之前的commit
git log # 得到你需要回退一次提交的commit id
git revert <commit_id> # 撤销指定的版本，撤销也会作为一次提交进行保存

（3） git revert 和 git reset的区别
(a). git revert是用一次新的commit来回滚之前的commit，此次提交之前的commit都会被保留( 会有 两次 commit id)；
(b). git reset是回到某次提交，提交及之前的commit都会被保留，但是此commit id之后的修改都会被删除 ( 只有一次 commit id)

作者：_画圆_
链接：https://www.jianshu.com/p/c55958563f5a
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

## 九十九、错误解决：

### 1、执行git命令时出现fatal: 'origin' does not appear to be a git repository错误
在执行git pull origin master时出现：
　　fatal: 'origin' does not appear to be a git repository
　　fatal: Could not read from remote repository.
　　Please make sure you have the correct access rights and the repository exists

解决方案：
```
git remote add origin git@github:bx_reader/bx-reader-api.git

将关联远程仓库为origin
```

### 2、Reinitialized existing Git repository
“git init” 的时候出现：Reinitialized existing Git repository
解决方法：
```
可以使用 rm -rf .git，删除.git，然后在 git init 即可
```

### 3、refusing to merge unrelated histories
“git pull origin master ” 的时候出现：refusing to merge unrelated histories

解决方法：
```
可以在 “git pull origin master” 后添加 “--allow-unrelated-histories”
即整个命令行为：
    git pull origin master --allow-unrelated-histories
```

如果你是git pull或者git push报fatal: refusing to merge unrelated histories
同理：
git pull origin master --allow-unrelated-histories
等等，就是这样完美的解决咯！
