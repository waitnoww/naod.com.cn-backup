---
title: mac Unable to access Android SDK add-on list
date: 2020-04-01 14:02:09
description: 测试工具分享系列-mac Unable to access Android SDK add-on list
tags:
- 测试工具
- 测试相关
nav:
- 测试工具
categories:
- Android Studio
image: img/blog_img/androidstudio.png
---
当我的Mac搭建好Android Studio环境后，第一次使用Android Studio时，会提示Unable to access Android SDK add-on list，如下图所示：
![上传成功](https://tva1.sinaimg.cn/large/00831rSTgy1gde8ezktanj31440fu41x.jpg)

网上查询到的解决方法也是Windows中的相同：打开bin\idea.properties这个文件，末尾添加一行disable.android.first.run=true就行了。

那问题来了，刚刚入手mac的我来说，首要的问题是怎么找到bin\idea.properties这个文件

继续网上检索到最后的答案是：
- 打开Finder 
- 在左侧的列表中点击应用程序
- 然后会在右侧的程序列表中看到已经安装的AndroidStudio
- 右键AndroidStudio的图标 
- 选择显示包内容 
- 会看到一个Contents文件夹 
-  进入Contents文件夹 
-  就会看到bin文件夹了 
-  进入bin文件夹然后修改idea.properties文件了
-  末尾添加一行disable.android.first.run=true



