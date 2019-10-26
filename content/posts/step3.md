---
title: "hugo 的安装"
date: 2019-10-24T22:23:56+08:00
draft: false
toc: true
tags: 
  - untagged
---

首先我们要知道：hugo 是一个静态博客生成器

## 第一步 下载

Windows 系统下：

32 位：

[hugo_0.59.0_Windows-32bit](/step3/hugo_0.59.0_Windows-32bit.zip)

64 位：

[hugo_0.59.0_Windows-64bit](/step3/hugo_0.59.0_Windows-64bit.zip)


其他系统请参考官方指导：

https://gohugo.io/getting-started/installing/

## 第二步 下载后

### 打开压缩包

打开压缩包，我们取出 hugo.exe 这个已经为我们编译好的软件。

（ 如果你是其他操作系统，也可以下载源代码，在自己的操作系统上编译，需要知道的是 hugo 是由 golang 编写的语言，而不是 c

![](/step3/1.png)

### 新建文件夹

在 `C:\apps` 文件夹下新建一个 hugo 文件夹，和我们之前已有的 Git 文件夹放在一起

![](/step3/2.png)

### 把 hugo.exe 放到特定位置

把 hugo.exe 放到我们新建的 hugo 文件夹里，像这样：

![](/step3/3.png)

### 还有一步很重要，虽然不必要，但是能减少点以后的操作难度

那就是为 hugo.exe 编辑环境变量。

#### 呼出环境变量设置界面

使用搜索工具，找到 操作系统环境变量 的位置。

![](/step3/4.png)

点击："环境变量"

![](/step3/5.png)

#### 找到 "系统变量" 下的 "Path"，编辑它

在 "系统变量" 下的 "Path" 新建一条环境变量：`C:\apps\hugo`

![](/step3/6.png)

#### 编辑完成后，保存退出

![](/step3/7.png)

#### 验证新添的系统变量是否生效

1. 打开 CMD (如果已经打开，那请关掉它重新打开)

2. 输入 hugo 命令

如果有下面的显示，说明环境变量配置成功。

![](/step3/8.png)

#### 如果不成功呢？

解决方法我们后面再说明


# 第三步 使用 hugo 新建博客

注意，这里我们要学一个新的命令： cd, 它用于在 CMD 中切换文件路径)

## 学习 cd 命令

首先，打开 CMD

### 输入 `cd C:\` 讓我們看看发生了什么

![](/step3/9.png)

看到吗，执行了这条命令后，我们所在的文件位置变为了 `C:\`

同理，我们依葫芦画瓢，前往 `C:\apps\hugo`

![](/step3/10.png)

## 学习 cd 命令之后

### 执行 hugo help 命令

在 `C:\apps\hugo` 文件路径下，我们执行这条命令：`hugo help`

![](/step3/12.png)

hugo 为我们输出了一些文本，这些文本，便是它的使用说明书。

从说明中，我们可以知道，hugo 程序有一个 new 指令，用来新建博客相关的文件。

### 执行 hugo new site blog 命令

我们执行 `hugo new site blog` 命令，来新建博客站点

![](/step3/11.png)

它给我们一个回应："Congratulations！" , 说明我们这一条命令执行成功了。

### 打开文件管理器看看

![](/step3/13.png)

看，生成的 blog 已经出现在了这里

打开 blog 文件夹，我们会看到：

![](/step3/14.png)

这便是以后我们操作博客的地方，虽然有很多陌生的文件和文件夹，但是我们其实只需要接触：

1. content 文件夹，这是我们存放文章的地方

2. config.toml 站点的配置文件

3. static 文件夹，存放静态资源的地方，比如：图片

4. themes 文件夹，存放主题的地方，主题 theme 决定站点的外观

# 第四步 使用 git 将本地的博客项目上传到 GitHub

在博客项目的路径（`C:\apps\hugo\blog`）下, 使用 `git init` 命令进行初始化。

![](/step3/15.png)








