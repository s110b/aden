---
layout: post
title: "用python计算程序处理效率"
date: 2013-09-28 08:28 
comments: true
categories: [note]

---

	用程序解决重复性的问题
公司的同事喜欢用excel解决问题，我们入库程序压力比较大。现在经常要计算一下它的处理效率。一般的处理方法就是脚本加excel，半天才出一个结果。我写了一个脚本，现在只要一行命令，就能计算出程序的效率了。

## 分析问题
1. 日志文件大，需要逐行读取，不能一次性读到内存中，不能影响服务器性能。
2. 无用的行需要过滤掉，只分析有效内容的行。
3. 每次只计算一个文件结果，输入参数为文件名称
4. 用shell循环执行。分析目录下所有日志。


## 编程步骤

python逐行读取文件方法


    with open(filename) as infile:
        for line in infile:
			do something line

过滤无用的行

    if line.find("pattern*") == -1:
        return None
    else:
        return line
读取参数

	if __name__ == '__main__':
	    isInput = len(sys.argv)
	    if isInput == 1:
	        print "pleas input log path and log name "
	    else:
	        path = sys.argv[1]
输出结果，字符串中间用tab分隔

        print path, "\t", str

脚本完成，用shell执行

	ls | grep core.log.2013-09 | while read f; do python read_file.py $f; done

ok，输出结果如下

	core.log.2013-09-18     96 ge/s          587 KB/s
	core.log.2013-09-19     95 ge/s          621 KB/s
	core.log.2013-09-20     90 ge/s          645 KB/s
	core.log.2013-09-21     87 ge/s          617 KB/s
	core.log.2013-09-22     88 ge/s          607 KB/s
	core.log.2013-09-23     83 ge/s          548 KB/s
	core.log.2013-09-24     86 ge/s          564 KB/s
	core.log.2013-09-25     85 ge/s          544 KB/s
	core.log.2013-09-26     79 ge/s          506 KB/s
	core.log.2013-09-27     74 ge/s          478 KB/s

可以看出最近入库效率明显下降，问题暴漏出来，才能在下一步采取措施







