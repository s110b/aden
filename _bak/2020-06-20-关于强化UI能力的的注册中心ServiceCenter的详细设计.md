---
layout: post
title: 关于强化UI能力的的注册中心ServiceCenter的详细设计
description: "关于强化UI能力的的注册中心ServiceCenter的详细设计"
tags: [注册中心 微服务 UI] 
---


## 目标 
开发一个开源的，开箱即用的，用户友好，扩展性好的，状态实时的的注册中心Frontend。

## 注册中心的对象图如下图，Frontend的职责是把下述的数据结构，对象以及他们的相互关系通过各种View清晰的展示出来：
![scf-uml](/images/scf-images/SCF-UML.png)
1个应用包含多个Service,Service之间有provide和comsume的关系，Service的主键为ID:Version, 每个Serivce包含多个Instance，也包含多个API的Contract,
每个Contacts包含多个TestCase,TestCase包含针对该API的输入和期望的输出，以及上次调用（如果有）时的输出。

## 系统中各组件交互的流程图：
以前端显示Service列表的前端组件为例：
![scf-uml](/images/scf-images/ListServiceProcess2.png)
因为很多Service的变化是一个不定时发生的异步事件，所以对这类情况采用，前端订阅，后端发现变化后推送最新版本的数据的方式来交互。当前端发起首次订阅时，后端总会推送一次数据当前版本的数据给前端。


## 架构图
![scf-arch](/images/scf-images/SCF-ARCH.png)
有上图可以看出，主要的职责集中在SCF-Backend中，即ServiceCenter UI的后端部分。它的职责包括：
* 把部分API请求转发给SerivceCenter以获取数据。
* 把SeriviceCenter已有的非异步的又不好改造的API,可以通过轮询的方式，转化为异步API提供给前端。
* 提供一些非原始SerivceCenter数据对象的API操作接口，比如TestCase，对的增删改查接口。
* 提供非原始SerivceCenter数据对象的持久化保存功能，通过etcd.
* 对一些异步的变化的数据，可以考虑将其存入时序数据库中，供后续查询，比如instances out of service的事件。前期该类型事件不多的情况下，为了不引入新的数据库，可以同样用etcd
持久话保存或用内存数据结构做非持久化存储。

## Frontend Views
目前ServiceCenter Frontend包括如下这些视图:
* API doc: 显示当前某服务的所有的API接口列表，按Service分组。
* API detail: 显示某API接口的Swagger UI, 显示历史的TestCase列表，可以执行某一个TestCase，显示执行结果，可以对上个执行的TestCase进行保存。
* ....

## API doc View的详细设计
1. 接口 GET /apis  参数： Service Id, Service Version, Channel ID， 返回该Service的所有的接口的概要列表。

## API Detail View的详细设计
1. 接口 Get /api_detail/:id  参数： API id， 返回该该API详情的json。包括：contract yaml, test case 列表。
2. 接口 Post /testcases， 参数， 一个测试用例的输入，和期望输出。 创建新的测试用例。
3. 接口 Delete /testcases/:id 参数， 测试用例ID。
4. 接口 PUT /api_detail/:id/try_out 参数，测试用例的输入和输出。
 

  
  
    
  
  
  
  
   
  
  
  







   
