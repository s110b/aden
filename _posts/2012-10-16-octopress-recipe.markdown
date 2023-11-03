---
layout: post
title: "octopress 乱码解决方法,以及云同步方法"
date: 2012-10-16 16:13
comments: true
categories: [note,octopress]

---

* octopress 存在乱码，编译不过去的现象。有时候主页没有乱码，链接点进去有乱码。这个问题困扰很久。现在总算解决了。
当然，categories 还没有加上。这个增加就会出现乱码，只能TODO

<!--more-->

1. 自动生成的文件名称用中文，改写title时 用双引号扩住。
2. 默认主页显示所有内容。编辑时在页面中增加 `<!--more-->` 这行上下要空开，会只显示 more前面的部分。后面的省略。
3. 在环境变量中增加字符集。如下。安装了git.bash后可以用下面的命令。

        $ vim ~/.bash_profile
        export   LC_ALL=zh_CN.UTF-8
        export   LANG=zh_CN.UTF-8

4. 书写markdwon文件时保存为utf-8 。
5. 为octopress 设置百度云同步。前段时间baidu活动，网盘100g。实在太给力了。
    现在把md文件和百度网盘同步：

 >   *   为win7创建软连接：
        命令格式为： mklink source origin ,即在桌面创建一个指向 `c:\Users\song\octopress\
        source\_posts` 的超链接。

 >           C:\Users\song>mklink /d   C:\Users\song\Desktop\_postse c:\Users\song\octopress\
            source\_posts

6. Disqus 语言设置后还是英文，general 选项中    `Enable Disqus 2012 features for your site.` 勾去掉。

