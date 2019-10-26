---
title: "git 的安装"
date: 2019-10-24T22:23:57+08:00
draft: false
toc: true
tags: 
  - untagged
---

首先我们要知道：git 是一个版本管理工具

声明：考虑到大部分人使用 Windows 系统，所以本章就 Windows 进行演示。其他操作系统下的教程未来可能会补上。

## 第一步 下载

打开浏览器，我们搜索一下 git

![](/step2/1.png)

可以发现它的官网稳稳地站在第一位

在浏览器的地址栏里输入 `git-scm.com/downloads` 进入下载页

![](/step2/2.png)

点击图中红勾处，下载 git

### 官方给出的下载渠道好像下载速度不是一点点的慢？

如果下载比较慢的话，可以访问下面两个链接：

64 位： https://npm.taobao.org/mirrors/git-for-windows/v2.23.0.windows.1/Git-2.23.0-64-bit.exe

32 位： https://npm.taobao.org/mirrors/git-for-windows/v2.23.0.windows.1/Git-2.23.0-32-bit.exe

#### 不知道电脑是 64 还是 32 位？

按 win + R 组合键，呼出 运行 窗口：

![](/step2/9.png)

输入 cmd ，回车，呼出 CMD。

![](/step2/10.png)

输入 systeminfo 命令，回车：

![](/step2/13.png)

得到结果：

![](/step2/14.png)

系统类型所对应文字说明： x64 即是 64 位，x86 即 32 位

## 下载后，安装前

前往 C 盘，在 C 盘下新建一个文件夹，文件夹名为 apps

为了方便管理软件，所以我们把软件安装到特定路径下方便索引与管理。

![](/step2/4.png)

打开 刚才下载好的 git 安装程序，把 安装路径 设定为： `C:\apps\Git`

![](/step2/5.png)

点击 next 后，便开始安装：

![](/step2/6.png)

之后，一律点击 NEXT 按钮，直到安装流程最后一步：

![](/step2/7.png)

选择 Finish，完成安装

## 安装后

安装后，我们需要检验一下安装是否成功

按 win + R 组合键，呼出 运行 窗口：

![](/step2/9.png)

输入 cmd ，回车，呼出 CMD。

![](/step2/10.png)

在 cmd 中输入 `git` 命令：

![](/step2/11.png)

如果有下面这样的输出，表示安装成功：

![](/step2/12.png)

（输出的内容是 git 的基本使用说明

到此，本章结束