---
title: "把本地的博客项目上传到 GitHub"
date: 2019-10-24T22:23:53+08:00
draft: false
toc: false
tags: 
  - untagged
---

# 让我们再瞄一眼 GitHub 上刚才新建的项目

![](/step6/1.png)

其实 GitHub 已经给了我们一些提示……

不过还是不看它的吧，follow me

# 回到本地博客项目，执行 `git init` 命令

![](/step6/2.png)

这样便进行了本地仓库的初始化

## 特别说明

这里我并不会特别说明 git 的语法，如果你想要更正规地学习它，可以拜访菜鸟教程 https://www.runoob.com/git/git-basic-operations.html

# 再执行 `git add .` 命令

git 的 add 命令用来指明哪些文件需要被提交。

你可以只add单个文件，比如 git add config.toml

新项目中，添加所有文件很普遍，所以我们使用 `git add .` 命令来添加当前项目的所有文件。

这里的 "." 表示当前文件路径，意思是将当前文件路径下的所有文件都进行 add 操作

因为我们是第一次提交项目，所以我们使用 `git add .`

# 再执行 `git commit -m "commit message"` 命令

git 的 commit 命令，记录你的更新旅程。

它需要 `-m "commit message"` 因为你得用一段话来说明你更新了什么，还是修复了什么。

使用 git add 命令将想要快照的内容写入缓存区， 而执行 git commit 将缓存区内容添加到仓库中。

# 再执行 

`git remote add origin https://github.com/{{Username}}/blog.git` 命令

同样的，把这里的 `{{Username}}` 替換為你的用户名。

## 为什么这样做？

我们有了本地仓库，也有了在 GitHub 平台上的远端仓库，那么这两个仓库之间如何联系呢

所以我们要告诉本地仓库："你的上线是……"

# 最后执行 `git push -u origin master`

將本地仓库的数据提交到远端仓库

![](/step6/6.png)
