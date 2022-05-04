---
title: Git回滚操作
excerpt: Git回滚操作
date: 2022-03-26 00:05:39
update: 2022-03-26 00:05:39
tags:
---

# Git 回滚操作

https://www.jianshu.com/p/c55958563f5a

### Git撤销&回滚操作(git reset 和 get revert)

#### Git 的工作流

工作区：在 git add xx 之前，在自己当前分支所修改的代码内容！
暂存区：已经 git add xxx 进去，且没有执行 git commit xxx 的。
本地分支：已经 git commit -m xxx 提交到本地分支的。
远程分支：git push origin HEAD:refs/for/master HEAD 是本地，master是远程分支

#### 代码回滚

在上传代码到远程仓库的时候，不免会出现问题，任何过程都有可能要回滚代码：

##### 1、在工作区的代码（checkout ~ 修改工作区文件）

git checkout -- a.txt # 丢弃某个文件，或者
git checkout -- . # 丢弃全部

注意：git checkout – . 丢弃全部，也包括：新增的文件会被删除、删除的文件会恢复回来、修改的文件会回去。这几个前提都说的是，回到暂存区之前的样子。对之前保存在暂存区里的代码不会有任何影响。对commit提交到本地分支的代码就更没影响了。当然，如果你之前压根都没有暂存或commit，那就是回到你上次pull下来的样子了。

#### 2、代码 git add 到缓存区，并未 git commit 提交（reset ~ 修改暂存区文件）

git reset HEAD .
git reset HEAD a.txt

注意：这个命令仅改变暂存区，并不改变工作区，这意味着在无任何其他操作的情况下，
工作区中的实际文件同该命令运行之前 无任何变化

#### 3、代码 git commit 到本地分支，但没有 git push 到远程 （git reset --hard ~ commit 之后）

git log # 得到你需要回退一次提交的commit id
git reset --hard <commit_id> # 回到其中你想要的某个版本
git reset --hard HEAD^ # 回到最新的一次提交
git reset HEAD^ # 此时代码保留，回到 git add 之前

#### 4、代码 git push 把修改提交到远程仓库 (git reset || git revert)

- （1）通过git reset是直接删除指定的commit

git log # 得到你需要回退一次提交的commit id
git reset --hard <commit_id>
git push origin HEAD --force # 强制提交一次，之前错误的提交就从远程仓库删除

- (2) 通过git revert是用一次新的commit来回滚之前的commit

git log # 得到你需要回退一次提交的commit id
git revert <commit_id> # 撤销指定的版本，撤销也会作为一次提交进行保存

- （3） git revert 和 git reset的区别
  (a). git revert是用一次新的commit来回滚之前的commit，此次提交之前的commit都会被保留( 会有 两次 commit id)；
  (b). git reset是回到某次提交，提交及之前的commit都会被保留，但是此commit id之后的修改都会被删除 ( 只有一次 commit id)

#### 开发过程中，场景处理：

##### 场景一： 糟了，我刚把不想要的代码，commit到本地仓库中了，但是还没有做push操作！

##### 撤销

上述场景一，在未进行git push前的所有操作，都是在“本地仓库”中执行的。我们暂且将“本地仓库”的代码还原操作叫做“撤销”！



![img](https://upload-images.jianshu.io/upload_images/16517912-c80eec34e53c58ca.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

情况一.png

##### 场景二：彻底完了，刚线上更新的代码出现问题了，需要还原这次提交的代码！

##### 回滚

上述场景二，已进行git push，即已推送到“远程仓库”中。我们将已被提交到“远程仓库”的代码还原操作叫做“回滚”！
注意： 对远程仓库做回滚操作是有风险的，需提前做好备份和通知其他团队成员！

如果你每次更新线上，都会打tag，那恭喜你，你可以很快的处理上述场景二的情况



![img](https://upload-images.jianshu.io/upload_images/16517912-499c18ed38977cf6.png?imageMogr2/auto-orient/strip|imageView2/2/w/714/format/webp)

情况二.png



二者区别：
revert是放弃指定提交的修改，但是会生成一次新的提交，需要填写提交注释，以前的历史记录都在；
reset是指将HEAD指针指到指定提交，历史记录中不会出现放弃的提交记录。

##### 场景三：刚才我发现之前的某次提交太愚蠢了，现在想要干掉它！

##### 情况三：需要回滚某次提交

找到要回滚的commitID
git log
git revert commitID
删除某次提交
git log --oneline -n5

git rebase -i "commit id"^
注意：需要注意最后的^号，意思是commit id的前一次提交

git rebase -i "5b3ba7a"^
在编辑框中删除相关commit，如pick 5b3ba7a test2，然后保存退出（如果遇到冲突需要先解决冲突）！

git push origin master -f
通过上述操作，如果你想对历史多个commit进行处理或者，可以选择git rebase -i，只需删除对应的记录就好。
rebase还可对 commit 消息进行编辑，以及合并多个commit。