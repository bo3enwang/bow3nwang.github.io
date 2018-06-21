---
title: Maven 构建 filter 没有替换属性值

date: 2016-12-8 10:53:00

categories:
- Code
- Java

tags:
- Maven
- Spring boot

toc: true
thumbnail: 
banner: 

---



最近在用Spring boot 搭建环境时遇到了个小问题,当我用maven的resources plugin 的filter功能时，maven没有自动为我替换变量属性，
<!-- more -->
导致我一度很纠结 不停的rebuild,clean项目，后来Google查了一下才知道在spring boot 的依赖下，会产生filter无法替换`${.....}`内属性值的问题，解决办法居然是将花括号换为`@....@` 问题到这就解决了，但这个是为什么呢？有空一定得弄清楚。

