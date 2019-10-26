---
title: "使用 markdown 语法撰写文章，并在本地预览你的博客"
date: 2019-10-24T22:23:55+08:00
draft: false
toc: true
tags: 
  - markdown
---

# 第一步 认识 markdown

首先：你可以在 https://www.runoob.com/markdown/md-tutorial.html 看到最适合菜鸟的 markdown 教程

markdown 被广泛运用，不只是程序员在使用这个高效工具。

markdown 是高效的，人性化的，几乎没有学习成本。

Markdown 编写的文档后缀为 `.md`, `.markdown`，一般使用 `.md`

## 1-1 特别说明

markdown 只是一个标记语言，如果你想看到样式美观的 markdown 文章需要有特别的工具将它进行翻译。

常见的翻译过程是： markdown => html

## 1-2 让我们看看 md 到底有多高效

作为示范，让我们先学习一个 md 语法：

语法：# 号标记

使用 # 号可表示 1-6 级标题，一级标题对应一个 # 号，二级标题对应两个 # 号，以此类推。

```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

翻译成 html 后，效果如下：

![](https://www.runoob.com/wp-content/uploads/2019/03/md2.gif)

还记得你在 office word 里是怎么调一级标题、二级标题的吗？在 office word 你需要用一连串的鼠标点击来调整字体大小或者间距，而在 markdown 的世界里，只需要一个 `#` 号。

## 1-3 在 markdown 中展示代码

书写为：

<pre>
&#96;&#96;&#96;c
#include <stdio.h>

int main(){
    return 0;
}
&#96;&#96;&#96;
</pre>

翻译后，并且由 highlight 程序着色后：

```c
#include <stdio.h>

int main(){
    return 0;
}
```

## 1-4 我觉得 markdown 的教程实在不用重复总结，所以

还是请你跟随 runoob 的教程来学习： https://www.runoob.com/markdown/md-tutorial.html

# 第二步 在 hugo 中写文章，还需要一些别的功夫

打开我们本地刚刚新建的 posts/hello_world.md 文件，里面内容如下：

![](/step4/1.png)

这里，我用一个图来解释：

![](/step4/2.png)
 
解释完后，我们编辑 posts/hello_world.md 为以下内容：

```md
---
title: "你好，世界！"
date: 2019-10-26T21:31:25+08:00
draft: false
toc: false
tags: 
  - untagged
---

你好，世界！

```

# 第三步 在本地预览你的博客

在 `C:\apps\hugo\blog` 路径下，执行 `hugo server -D` 命令

![](/step4/3.png)

结果如下图，则说明执行成功：

![](/step4/4.png)

这时，我们已经在本地开启了一个web服务器，现在我们在浏览器地址栏里输入 `http://localhost:1313/`

进入网页，你会来到博客的欢迎页 / 首页

![](/step4/5.png)

点击中央的绿色文字，跳转到 文章列表页:

![](/step4/6.png)


在 本地预览时，你对博客项目里的文件的更新会被实时加载，现在打开 posts/hello_world.md ，在正文里写点什么（注意写完之后要保存），你会发现网页也随之刷新了内容。