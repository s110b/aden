---
layout: post
title: "jekyll 管理 添加图片"
description: ""
category: 
tags: []
---




jekyll如何管理图片

	http://otaku-elite.com/code/2012/01/31/managing-images-with-jekyll/

我们的目标是通过脚本生成如下图所示的目录结构：



<div class="mediaobject">
        <img alt="The CSS Spy in action" src="/images/2013/09/08/20130908150401.jpg">
</div>


首先在根目录建立images目录，把需要的图片存入这个文件夹内。

然后我们在Rakefile文件末添加下面代码。

{% highlight ruby %}

    desc 'Move all images in images/ to the current date image directory'
    task :images do
      images = FileList['images/*.*']
      time = Time.new
      target = Rake.application.original_dir + time.strftime('/%Y/%m/%d/')
      #unless the file list is empty
      unless images.existing.empty?
          puts 'Cleaning images: ' + images.existing.to_s + ' => ' + target
          begin
            Dir::mkdir(target)
          rescue
          end
          mv images.existing, target
      end
    end

{% endhighlight %}

进入images目录，执行rake images，脚本会把图片移动到对应的日期目录文件夹下。

最后在编辑文件时，如下添加图片：

	/images/2013/09/08/image004.png



