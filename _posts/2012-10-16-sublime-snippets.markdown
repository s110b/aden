---
layout: post
title: "Snippets 自动提示功能"
date: 2012-10-11 11:52
comments: true
categories: 
- note
---

* sublime 的 Snippets 可以自定义代码补全功能。

<!--more-->

    1. 我建了一个python的main方法自动提示,步骤如下：

        1.  (Tools > new Snippet) 

                <!-- See http://www.sublimetext.com/docs/snippets for more information -->
                <snippet>
                    <tabTrigger>main_song</tabTrigger>
                    <scope>source.python</scope>
                    <description>main</description>
                    <content><![CDATA[
                if __name__ == '__main__' :
                    ${0:pass}
                ]]></content>
                </snippet>

        2.  保存为文件名 main.sublime-snippet。默认保存到package文件下。这样升级的时候不会覆盖掉。


****

参考以下链接：

>  [Sublime Text 2 使用配置心得 – notepad++ 略丑](http://7626.net/?p=164 "引用") 

>  [Sublime Text 2配置和使用](http://qilei.org/201204/sublime-text2-setting/ "引用") 

为win7创建软连接：
命令格式为： mklink source origin ,即在桌面创建一个指向 `c:\Users\song\octopress\
source\_posts` 的超链接。

    C:\Users\song>mklink /d   C:\Users\song\Desktop\_postse c:\Users\song\octopress\
    source\_posts


<http://sinosmond.github.com/blog/2012/06/24/centos6-dot-2-plus-jdk6-plus-tomcat7-plus-nginx1-dot-2-plus-mysql5-dot-x/>





---
