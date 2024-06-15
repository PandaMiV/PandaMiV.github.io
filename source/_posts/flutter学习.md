---
title: flutter学习
date: 2024-06-15 16:32:30
tags:
- 博客
- 菜鸟学习
- flutter
- dart
categories: 又要学新技术😇
---
## Dart

### Dart介绍

> Dart是谷歌开发的计算机编程语言，可以被用于web、服务器、移动应用 和 物联网等领域的开发
> 学Flutter必须先学Dart


### Dart环境搭建(Win10)

#### Dart下载

> https://gekorm.com/dart-windows/ 下载Dart软件(无脑安装)
> 不推荐命令行下载

#### 测试Dart SDK是否安装成功

> 打开cmd 输入
>> dart --version
>
>  显示 Dart SDK version: 3.4.4 (stable) (Wed Jun 12 15:54:31 2024 +0000) on "windows_x64" 安装成功


### VS Code 配置 Dart

> Dart的开发工具有：IntelliJ IDEA、WebStorm、Atom、VS Code等
> VS Code中配置Dart
>> 1、安装Dart插件
>> 2、安装Code Runner插件
>
> 新建Dart文件
>> .dart结尾，例：index.dart


### Dart 语法

#### Dart 基础运行
> Dart要执行的东西都放在入口方法里
> 
>     main() {
>       print('Hello Dart'); // 每句话后面要加分号，里面内容双引号单引号都可以
>     }
> 
> 保存文件，右键 Run Code 运行，输出：
> 
>     [Running] dart "d:\Dart_Demo\demo001\index.dart"
>     Hello Dart
>     Hello Dart1
>
>     [Done] exited with code=0 in 0.338 seconds
> 
> 输出以上内容代表SDK和VS Code配置搞定
> 如果输出乱码，重启电脑解决（重启大法好😎）