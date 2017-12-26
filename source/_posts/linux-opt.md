---
title: 如何更换 Ubuntu Linux 内核。

date: 2017-03-8 00:00:00

categories:
- Linux

tags:
- Ubuntu

toc: true

---

* 查看当前系统内核版本

`dpkg -l|grep linux-image`

* 更新 Ubuntu 包索引

`sudo apt-cache search linux-image`

* 安装新内核 ( aa 为你需要更新的版本 )

`sudo apt-get install linux-image-3.13.0-aa-generic linux-image-extra-3.13.0-aa-generic`

* 卸载旧版本内核 ( xx 为你当前版本内核 )

`sudo apt-get purge linux-image-3.13.0-xx-generic linux-image-extra-3.13.0-xx-generic`

* 更新 grub 引导

`sudo update-grub`

* 重启ubuntu

`reboot`