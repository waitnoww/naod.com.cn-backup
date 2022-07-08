---
title: 从0到1搭建接口自动化测试框架-python环境搭建
date: 2020-03-21 20:55:40
description: python接口自动化测试框架开发教程-python环境搭建
tags:
- 测试开发
- python
- 测试工具开发
nav:
- 测试开发
categories:
- 从0到1搭建接口自动化测试框架
image: img/blog_img/python_api_test_pic_1.png
---
网上搭建python环境的教程很多，我推荐菜鸟教程的[Python3 环境搭建](https://www.runoob.com/python3/python3-install.html).

下面我列举一下主要步骤，以windows系统为例(苹果电脑python环境搭建有问题的直接评论下留言，我会一一帮你解答）

#### python安装包下载
 - 1.进入[python官网](https://www.python.org)
 - 2.选择downloads-[windows](https://www.python.org/downloads/windows/)
 - 3.选择最新release的python3版本，我以[python3.8.3](https://www.python.org/downloads/release/python-382/)举例
 - 4.进入页面后，选择下载 [Windows x86-64 executable installer](https://www.python.org/ftp/python/3.7.7/python-3.7.7-amd64.exe)
 - 5.等待安装包下载完成
  
#### 安装python包
- 1.直接点击运行
- 2.选择默认安装install now
- 3.记得勾选Add Python 3.8 to PATH（若不勾选，就需自己设置python的path环境，所以建议勾选）
- 4.按照安装程序指示，将python安装完成

#### windows命令行执行python
- 1.进入windows系统cmd命令行界面
- 2.输入python，未报错且展示了你安装的python3.8.2版本号,说明python3环境安装成功,若展示的不是你安装的版本号，有可能你系统安装了多个python版本，后面我会单独出文章介绍如何一个系统多个python版本共存
- 3.输入简单python程序
  ```
  print(hello_python)
  ```
- 4.按下回车键执行展示hello_python，代表python程序执行成功

#### python自带IDLE
- windows系统程序列表搜索python，选择IDLE，就可以展示python的脚本边界页面

#### python开发工具
- 推荐PyCharm,好用，推荐[pycharm官网](https://www.jetbrains.com/pycharm/download/#section=windows)安装

#### windows系统python环境变量配置
- 右键点击"计算机"，然后点击"属性"，选择"高级系统设置"
- 然后选择"系统变量"窗口下面的"Path",在"Path"行，添加python安装路径即可（注意：安装路径直接用分号"；"分割开）
- 保存后，重新打开cmd命令行，输入命令"python"，展示python版本号无报错表明环境变量设置成功。