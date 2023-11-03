---
layout: post
title: "octopress主题修改"
date: 2012-10-17 14:50
comments: true
categories: 
- octopress
---
__看了阮一峰的博客，自己也想搭建一个独立博客。搭建倒也容易，只是没想到跟中毒一样，不停的像修改这个，修改那。__

<!--more-->

## 修改catogry 
 刚开始就只是想在侧边栏增加一个导航页面，因为我的博客比较多。一页一页翻太麻烦。
增加了之后，返现侧边栏老是有这么个玩意也碍眼，于是去掉。突然就发现有人把导航放在顶部。
这个一下子让我茅塞顿开，也放在顶部。发现很好看。
## 修改页面颜色

改变颜色，octopress的颜色都是黑，很多人直接拿来用也没改过。我在网上搜了搜看了几个plugin主题。
  试用后都不满意。还不如原来的好看。还是自己调整的好。然后再网上这找找那找找。终于成了现在这个样子。

## 修改单栏显示

   去掉右边栏之后，发现页面并没有铺开，而是留一个大空。网上搜了搜给了一个[解决方案](https://github.com/imathis/octopress/issues/342)。改完后又发现页面过宽了，继续在

    # In /sass/custom - Change these files for easy customization
    _layout.scss     # Override settings for base/_layout.scss to change the layout
        
里增加 `$max-width: 900px;`  然后就很美观了。