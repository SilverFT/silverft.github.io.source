---
title: Linux
copyright: true
date: 2019-11-10 19:39:58
tags:
---



# samba服务

* yum install samba
  * 











### yum 

* yum clean all
  * yum 会把下载的软件包和header存储在cache中，而不自动删除
  * 如果觉得占用磁盘空间，可以使用yum clean指令进行清除，更精确 的用法是
    * yum clean headers清除header
    * yum clean packages清除下载的rpm包
    * yum clean all一全部清除
*  yum check-update 
  *  列出所有可更新的软件清单
*  yum update 
  *  更新所有软件 
*  yum install <package_name> 
  *  仅安装指定的软件 
*  yum update <package_name> 
  *  仅更新指定的软件
*  yum list 
  *  列出所有可安裝的软件清单 











# TIPs

* 环回网卡的作用

  *  可以在实验中用到，有的实验需要网卡处于连接状态，而此时你的物理网卡没有连接网线，于是就可以使用“环回网卡”来欺骗操作系统 - 网卡已经连接了。同理，虚拟光驱有时候也用于欺骗，即，光盘已经挂载上了~ 

  *  microsoft loopback adapter就是安装在本机上的一块虚拟网卡，它跟本机上的其它物理网卡、和物理网卡连接的网络是没有关系的，你可以理解成这块网卡上的网线接到了另外一个空白网络。

    它的作用仅仅是用来给那些需要本机配置有网络的服务程序调试用，它不能与实体网络进行通信。

    举个最简单的例子，你的电脑没有网卡，想给本机安装WINDOWS的DNS服务试着玩，但DNS服务在启动时若检测到本机没有网络会报错停止，这时你安装块loopback adapter网卡就有用了 