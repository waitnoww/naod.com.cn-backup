---
title: python3安装turtle时出错解决办法
date: 2020-03-16 09:43:53
description: 测试开发用python-python3安装turtle时出错解决办法
tags:
- 测试开发
- python
- 测试工具开发
nav:
- 测试开发
categories:
- python-awesome
image: img/blog_img/python4.png
---
前些天看到有个用python3来画飞机的教程，就想来尝试一下。教程中使用的是turtle包，那么首先我们就要来按照turtle，结果第一步就失败了，当我使用pip3安装的时候，出现如下报错
![报错截图1](https://tva1.sinaimg.cn/large/00831rSTgy1gcvjrh4atxj322y0tidos.jpg)

出现报错，阅读了一下报错信息，先使用搜索引擎查找一下报错信息，发现报错信息搜索不到正确答案。可能是我搜索的关键词不对，然后我去turtle包的介绍页看了一下 https://pypi.org/project/turtle
就想说尝试一下下载包来安装，于是下载了turtle 0.0.2进行安装，结果解压之后又报错了，查看报错信息如下
![报错截图2](https://tva1.sinaimg.cn/large/00831rSTgy1gcvkcockxfj30xi0k4k02.jpg)

根据提示 python setup.py egg_info查看详细报错信息
![报错截图3](https://tva1.sinaimg.cn/large/00831rSTgy1gcvkf9brszj30u004aq3o.jpg)
进入turtle下载文件夹下打开setup.py 文件，看看 40 行，发现少了括号
![报错截图4](https://tva1.sinaimg.cn/large/00831rSTgy1gcvkgvc0r9j31620tkwkm.jpg)
加上括号，还是报错，原来是没有指定修改目录导致,那就指定目录安装，安装成功
![报错截图5](https://tva1.sinaimg.cn/large/00831rSTgy1gcvkizcd0pj30w60jc45s.jpg)

总结一下：仔细阅读报错信息，分析根本原因