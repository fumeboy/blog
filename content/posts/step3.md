---
title: "hugo 的安装以及博客的初始化"
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

### 2-1 打开压缩包

打开压缩包，我们取出 hugo.exe 这个已经为我们编译好的软件。

（ 如果你是其他操作系统，也可以下载源代码，在自己的操作系统上编译，需要知道的是 hugo 是由 golang 编写的语言，而不是 c

![](/step3/1.png)

### 2-2 新建文件夹

在 `C:\apps` 文件夹下新建一个 hugo 文件夹，和我们之前已有的 Git 文件夹放在一起

![](/step3/2.png)

### 2-3 把 hugo.exe 放到特定位置

把 hugo.exe 放到我们新建的 hugo 文件夹里，像这样：

![](/step3/3.png)

### 2-4 还有一步很重要，虽然不必要，但是能减少点以后的操作难度

那就是为 hugo.exe 编辑环境变量。

#### 2-4-1 呼出环境变量设置界面

使用搜索工具，找到 操作系统环境变量 的位置。

![](/step3/4.png)

点击："环境变量"

![](/step3/5.png)

#### 2-4-2 找到 "系统变量" 下的 "Path"，编辑它

在 "系统变量" 下的 "Path" 新建一条环境变量：`C:\apps\hugo`

![](/step3/6.png)

#### 2-4-3 编辑完成后，保存退出

![](/step3/7.png)

#### 2-4-4 验证新添的系统变量是否生效

1. 打开 CMD (如果已经打开，那请关掉它重新打开)

2. 输入 hugo 命令

如果有下面的显示，说明环境变量配置成功。

![](/step3/8.png)

#### 2-4-5 如果不成功呢？

解决方法我们后面再说明


# 第三步 使用 hugo 新建博客

注意，这里我们要学一个新的命令： cd, 它用于在 CMD 中切换文件路径)

## 3-1 学习 cd 命令

首先，打开 CMD

### 3-1-1输入 `cd C:\` 讓我們看看发生了什么

![](/step3/9.png)

看到吗，执行了这条命令后，我们所在的文件位置变为了 `C:\`

同理，我们依葫芦画瓢，前往 `C:\apps\hugo`

![](/step3/10.png)

## 3-2 学习 cd 命令之后

### 3-2-1 执行 hugo help 命令

在 `C:\apps\hugo` 文件路径下，我们执行这条命令：`hugo help`

![](/step3/12.png)

hugo 为我们输出了一些文本，这些文本，便是它的使用说明书。

从说明中，我们可以知道，hugo 程序有一个 new 指令，用来新建博客相关的文件。

### 3-2-2 执行 hugo new site blog 命令

我们执行 `hugo new site blog` 命令，来新建博客站点

![](/step3/11.png)

它给我们一个回应："Congratulations！" , 说明我们这一条命令执行成功了。

### 3-2-3 打开文件管理器看看

![](/step3/13.png)

看，生成的 blog 已经出现在了这里

打开 blog 文件夹，我们会看到：

![](/step3/14.png)

这便是以后我们操作博客的地方，虽然有很多陌生的文件和文件夹，但是我们其实只需要接触：

1. content 文件夹，这是我们存放文章的地方

2. config.toml 站点的配置文件

3. static 文件夹，存放静态资源的地方，比如：图片

4. themes 文件夹，存放主题的地方，主题 theme 决定站点的外观

# 第四步 下载一个博客主题并进行相关配置

在浏览器地址栏中输入 `https://github.com/fumeboy/example_blog_theme`

那里有我预先准备的一个主题，我们就使用这个主题作为博客的外观载体。

## 4-1 下载主题

![](/step3/21.png)

进入网页后，按上图所示，点击绿色的 clone 按钮，选择 download ZIP

## 4-2 打开压缩包，移动主题文件到指定文件位置

下载后，打开压缩包，结果如图：

// 一个压缩包内容的图

我们将压缩包中的文件夹移动到 `C:\apps\hugo\blog\themes` 路径下，得到的结果应当是：

// 一个文件管理器的图

修改主题文件所在文件夹的名字，去掉尾部的 "-master" , 改为 "example_blog_theme"

// 一个文件管理器的图

## 4-3 编辑 config.toml

回到  `C:\apps\hugo\blog` ，我们找到 config.toml ，打开，用下面的文本覆盖它的内容：

（ 你可以依据其中的注释进行适当的修改

```toml
baseURL = "http://example.org"
languageCode = "zh-hans"
defaultContentLanguage = "zh-hans"
title = "blog's title"
theme = "example_blog_theme" # 此处的 example_blog_theme，指向 themes/example_blog_theme 这个文件夹。

# 这里的 pygments 设置用于文章中代码的高亮处理
pygmentsCodefences  = true
pygmentsUseClasses  = true

hasCJKLanguage = true
# 如果 Chinese/Japanese/Korean 是这个博客的主要语言, 启用这个选项好让负责字数统计的程序可以正确的计数.

rssLimit = 10
# RSS feed 中条目的最大显示数量.

copyright = "This work is licensed under a Creative Commons Attribution-NonCommercial 4.0 International License."
# 这条信息只会被 RSS template 使用.

enableEmoji = true
# 在你的博客里启用 emoji 表情，表情的代码可以在这里查阅 - https://www.webfx.com/tools/emoji-cheat-sheet/
# 比如 "你好 :heart: 世界"，其中 ":heart:" 会被翻译成 emoji 中的 爱心

[author]
  name = "fumeboy"

[taxonomies]
  tag = "tags"

[params]
  homeSubtitle = "A minimal and fast blog built by hugo"
  dateform        = "Jan 2, 2006"
  dateformShort   = "Jan 2"
  dateformNum     = "2006-01-02"
  dateformNumTime = "2006-01-02 15:04 -0700"
  themeColor = "#494f5c"
  footerCopyright = ' &#183; <a href="https://creativecommons.org/licenses/by-nc/4.0/" target="_blank" rel="noopener">CC BY-NC 4.0</a>'
  code_copy_button = true # Turn on/off the code-copy-button for code-fields

  # 社交链接，如果你希望其他人可以通过你的博客访问到你的 知乎、豆瓣、GitHub、微博等网站的主页，可以在下面添加链接
  [[params.social]]
    name = "twitter"
    url = "https://twitter.com/"

  [[params.social]]
    name = "instagram"
    url = "https://instagram.com/"

  [[params.social]]
    name = "github"
    url = "https://github.com/"

[menu]# 菜单，作为网站的索引而使用

  [[menu.main]]
    name = "About"
    url = "about_me/"
    weight = 10

```

# 第五步 使用命令新建文章

打开 CMD，前往 `C:\apps\hugo\blog`

1. 输入命令 `hugo new posts/hello_world.md` 回车

1. 输入命令 `hugo new about_me.md` 回车

1. 输入命令 `hugo new friends.md` 回车

# END

本章结束，下一节是，学习使用 markdown 语法编写文章。






