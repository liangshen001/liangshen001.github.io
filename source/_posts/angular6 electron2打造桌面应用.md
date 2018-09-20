---
title: angular6 electron2打造桌面应用
date: 2018-09-19 12:30:05
wordcount: 
tags: [angular6,electron2,ngrx,ngx-electron]
categories: 前端技术
---
[https://github.com/liangshen001/moon](https://github.com/liangshen001/moon) 目前在维护的项目一个聊天软件，类似qq

<!--more-->

数据在应用中的存储主要基于ngrx管理，在实际应用中主进程和渲染进程的通讯非常的繁琐，并且难以开发出脱离electron环境的web应用，所以我在electron的rpc基础上做了封装，@ngx-electron

@ngx-electron分为三个项目

* electron-core

在渲染进程中使用 可以在渲染进程中打开一个窗体 并初始化数据，窗体可以是单例的（需要electron-main支持，否则非单例），可以在窗体之间发送和广播数据 可以对tray进行操作（需要electron-main支持，否则非单例）

* electron-main

在主进程中使用 在主进程中创建窗体 创建tray （管理tray和所有的窗体）

* electron-data-shared

在渲染进程中使用 可以在渲染进程 中打开一个窗体







