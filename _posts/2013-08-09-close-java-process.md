---
layout: post
title: "如何优雅的关闭java进程。（避免 kill -9 ）"
description: ""
category:
tags: ["java"]
---

--
#### 一、为什么不能用kill -9 ：
项目中需要一个死循环不断从队列中获取消息存入数据库，但是，当项目需要重启时，
操作人员往往会用kill -9 直接关闭java进程。导致数据丢失。为了解决这个问题，
用到下面技术，

	1. 一个是 java的hook ，钩子函数，在虚拟机启动时注册一个钩子函数，
	   当执行kill时，java虚拟机会对钩子函数中资源进行回收。

	2. 多线程，用线程启动死循环，然后钩子函数接收到关闭命令时传递死循环标志位。
	   示例代码如下：

#### 二、线程方法：

{% highlight java linenos=table %}

public class MyRunnable implements Runnable {
	private volatile boolean quit =false;

	public boolean isQuit() {
		return quit;
	}

	public void setQuit(boolean quit) {
		this.quit = quit;
	}

	public void run() {
		int i = 0;
		while (!quit) {
			doStuff(i++);
		}
	}

	private void doStuff(int n) {

		try {
			Thread.sleep(1000);
		} catch (InterruptedException e) {
			e.printStackTrace();
		}
		System.out.println("----->" + n);
	}

}


import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

public class TestThread {

	public static void main(String[] args) {

		final MyRunnable test = new MyRunnable();
		

		final ExecutorService executorService = Executors.newCachedThreadPool();
		executorService.execute(test);

		Runtime.getRuntime().addShutdownHook(new Thread() {
			public void run() {
				test.setQuit(true);
				sleep(5);
					while (test.isQuit()&&!executorService.isShutdown()) {
						System.out.println("thread is closed, now ,close executorService!"); // optional
						executorService.shutdown();
					}

			}

			private void sleep(int n) {
				try {
					Thread.sleep(1000*n);
				} catch (InterruptedException e) {
					e.printStackTrace();
				}
			}
		});

	}

}

{% endhighlight %}

