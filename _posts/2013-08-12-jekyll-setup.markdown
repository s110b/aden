---
layout: post
title: "jekyll win7 install"
date: 2013-08-12 17:22
comments: true
categories: 
---
## 运行环境 ##
1. 安装ruby环境，安装gem，安装git，windows上还要安装，要全部安装的很麻烦。网上有一个安装包合集。可以一次性安装所有jekyll必须的环境。地址如下：
2. [RailsInstaller](http://railsinstaller.org/en "railsinstaller")
	<pre>
	RailsInstaller向Windows开发者提供了一种便捷的方式以轻松、快速创建Ruby on Rails 3应用
	</pre>

2. 字符集，jeykll统一设置为utf-8，在环境变量中增加：

	<pre>
	LANG=zh_CN.UTF-8 
	LC_ALL=zh_CN.UTF-8
	</pre>


3. 在github上注册账户，并用`邮件激活`，必须激活，否则提交之后会不会更新，（第一次能更新，后	面就不能更新了。）
4. 安装bootstrapjekyll。[jekyllbootstrap](http://jekyllbootstrap.com/ 	"jekyllbootstrap")
5.	bootstrapjekyll提供了一种快速安装jekyll的方案，只要在下图的输入框中输入你的用户名，然后直接拷贝页面内的命令挨个执行就安装成功了。
![1](https://f.cloud.github.com/assets/2377148/953407/6d1e73be-03f5-11e3-90f7-c6bd8e5e7c3c.jpg)




	