---
layout: post
title: "octopress部署后记"
date: 2014-08-28 09:45:41 +0800
comments: true
categories: 
- octopress
- ssh
---

偶然发现github上的source分支下没有源代码文件夹source，可是push不上去，向同事讨教了一下，对git又有些认识：

  1. 分支是从master下分出来的，一定是包含master的内容
  2. 要删除git相关的信息，可通过git rm实现
  3. 装个sourceTree图形化管理git(这个有空再研究)


在理清git原理之后（还只是皮毛，但已经比原先小白的程度好多了，不再是一头雾水），花了半小时的时间重新成功部署了一次。

前一篇里提到说source分支需要手动建立，这个是我搞错了，原来要在发表文章之后才会生成source分支，这个官方教程里没有提到，网上的文章也大都没有提及。。。

通过以上折腾,学习了多ssh key的配置方法，附上[配置教程](http://my.oschina.net/meilihao/blog/157716)


