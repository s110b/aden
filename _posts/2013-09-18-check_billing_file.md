---
layout: post
title: "关于稽核系统"
date: 2013-09-18 23:07
description: ""
category: 
tags: []
---


## 缘起
稽核系统是被领导强迫要做的。当时我心理其实不是那么愿意。觉得这玩意离核心系统远点。不想做出来之后，解决了计费的大问题。这也说明了一个道理，`你想做的不一定是对的，被强迫做的，也不一定就是错的。`每个人的判断力不一样。
据说 科波拉当年也不愿意拍`教父`，不想拍了之后却成了经典。
## 开发过程
稽核系统的开发并不顺利，我们第一次迭代就失败了。当时党总还在会上问：`你觉得失败的原因是什么？ 为了对应他讲的项目管理，答曰：风险失控。` ，我当时觉得是人员的失控，其实，对技术考虑不周也是主要原因。
## 设计
之前SNP整个部门都不重视设计，党总来了之后就要求在项目起步前必须要有设计文档。虽然我也做了，但是在项目期间其实做的并不好，因为刚开始都是被强迫的。没有主观能动性。但是正是有了这个设计文档。开发的过程顺利很多。后来我崇拜的大牛caoz也在博客发文论述设计文档的重要性。这次项目起码有了设计文档。
## 持续改进
项目第一次迭代失败后，第二次把入库的逻辑改为用java重写。并参照刷新系统的经验，把他们的系统架构直接搬了过来。这个架构还是蛮不错的。但是，`完全照搬也是有问题的`。这个后面再论。
项目第二次迭代后，成功上线，解决了计费文件传输过程中的监控，但是，经常会间歇性的发生MQ堆积。堆积之后只能重启应用。没有什么好的解决方案。后来我详细查看了celery的配置项，不停的调整配置，当时貌似起了作用，但是仍然没有解决MQ间歇性堆积的问题。在这个过程中，我们做了下面这些事情：

1. 查看计费文件不一致情况，系统刚上线的时候，DM上报，已接收，已处理，差距很大。分别查询原因，找具体的人解决。有的牵涉到别的部门，发邮件，找人逐一解决。到目前，基本上三线合一了。
2. 增加查看异常页面，增加了两个常用功能，用了开源表格控件datatables，各种排序，分页，导出excel功能。非常好用。
3. 增加同步脚本，彻底解决了手动从直传移文件到延迟。这个脚本也是个持续改进过程。

## 同步脚本
- 刚开始我设想的是自动同步，把三小时内不一致的文件自动相互同步，实验了一段时间脚本，发现当发生大规模堆积时，反而掩盖了问题，这个时候最重要的是通知根总处理堆积，而不是同步，因为你同步过来，他的文件最终还是要传过来，造成机器很大的压力。所以这个脚本其实用处不大。
- 在同步的过程中，发现同步机器慢。同步1万个文件能花半小时，在内网花半小时简直没道理。我想到先应该把文件移动到一个临时文件夹然后打成tar包。 然后写了脚本验证。效果不错。
- 但是怎样才能让同步程序发挥效用，比如：当延迟上有一些小坑，每天基本都有，如果不同步，直接找根总，他也解决不了。这些文件积攒多了，也影响系统稳定性。于是我把同步脚本改成时间可以任意设定。只有当觉得有必要的时候才登陆上去手动执行一次。在此过程中。还可以监控主机压力，目前效果也很好，执行一次不到5分钟，节省了以前可能半天才能弄完的事，而且准确高效。同步完成成后，过几分钟刷新下稽核系统，能立竿见影的看到同步效果。

## 解决MQ堆积


