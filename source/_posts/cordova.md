---
title: cordova 结合 vue 构建 webapp 教程
date: 2019-03-03 19:34:52
tags: 
- cordova
categories: web前端
---
## 一、环境搭建篇

> Apache Cordova 生态比较活跃而且还是歪果仁开发的一个混合APP框架，反正最近比较闲就试试研究研究一番。还是先从环境搭建开始，准备好了吗？要开车咯

## 1、开发环境
* node 8.9.0 (我在用的版本)
* android sdk (生成 *.apk)
* Xcode(生成*ipa)

>说明下Xcode要在Mac系统上才会有 本人没有Mac 只能从安卓玩起

## 2、Cordova安装，创建项目（windows为例）

[Cordova官方文档](https://cordova.apache.org/docs/zh-cn/8.x/guide/cli/index.html)

  ### 2.1 在Windows安装cordova
  ```shell
  npm install -g cordova
  ```
![安装cordova](/images/20190303/20190303152801.png)

* 创建coedova项目
> cordova create (hello) 这个换成自己想要的名字 
```shell
cordova create hello com.example.hello HelloWorld
```
* 添加平台需要的插件
```shell
cordova platform add ios --save
cordova platform add android --save
```
* 添加Android成功

![添加Android成功](/images/20190303/20190303153825.png)

查看下平台

```shell
D:\myapp>cordova platform ls
Installed platforms:
  android 7.1.4
Available platforms:
  browser ~5.0.1
  ios ~4.5.4
  osx ~4.0.1
  windows ~6.0.0
```

* 添加cordova插件

```shell
cordova plugin search camera // 搜索插件
cordova plugin add cordova-plugin-camera // 添加所需的插件
```

* 查看已添加的插件

```shell
D:\myapp>cordova plugin ls
cordova-plugin-camera 4.0.3 "Camera"
cordova-plugin-whitelist 1.3.3 "Whitelist"
```
## 3、构建App

>重要：请首先确保你的 Windows 已经安装了Android SDK 或者 Android Studio，配置好环境变量，iOS 需要安装Xcode

[Android 官方指导](https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html)

[iOS 官方指导](https://cordova.apache.org/docs/en/latest/guide/platforms/ios/index.html)

* 如果你没有安装SDK会出现这样的局面

![未安装SDK](/images/20190303/20190303155903.png)

* 我是直接安装Android studio （需要一把梯子俗称VPN）

> 强烈建议安装Android studio 简单快捷，工具直接百度就有了

环境要求

1. Android 5.1.1 （API 22） 平台 SDK
2. Android SDK 生成工具版本 19.1.0 或更高版本
3. Android 支援存储库 （额外）
4. JDK 7.0或更高版本（推荐8版本）

> 请严格按照这里的SDK来配置不然会报错JDK选择8版本的就够了java环境配置请直接百度一下

# 最后我想说的是我不建议新手直接玩这个，因为你可能会在配置安卓环境的时候惨死
附赠运行成功图

![成功](/images/20190303/20190303175102.png)