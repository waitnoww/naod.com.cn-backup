---
title: 从0到1搭建接口自动化测试框架-python2&python3共存
date: 2020-03-22 19:13:35
description: python接口自动化测试框架开发教程-python2&python3共存
tags:
- 测试开发
- python
- 测试工具开发
nav:
- 测试开发
categories:
- 从0到1搭建接口自动化测试框架
image: img/blog_img/python_api_test_pic_2.png
---
很多同学之前的电脑系统都装过python2，很多老程序也是只兼容python2的，所以不想卸载系统的python2，想要python2和python3共存，我也是一样的想法。

下面是windows系统python2&python3共存方案步骤：

1.安装python3

　备注：安装方法参考我上一篇博文

2.修改python3目录下python.exe为python3.exe，修改python3目录下pythonw.exe为pythonw3.exe


　　备注：因为博主我之前都是使用python2，所以修改了python3目录

3.配置pip3

```
python3 -m pip install --upgrade pip --force-reinstall
```
4.命令行验证

```
（1）命令行输入python，正常展示python2的版本且无报错则ok
（2）命令行输入python3，正常展示python3的版本且无报错则ok
（3）命令行输入pip -v，正常展示python2的pip版本且无报错则ok
（4）命令行输入pip3 -v，正常展示python3的pip版本且无报错则ok
```
5.python包安装
```
（1）python2安装，pip2 install XXX
（2）python3安装，pip3 install XXX
```
6.pycharm和python3开发环境设置

 在项目设置中打开project Interpreter选择已有的运行环境，路径选择电脑上的python3安装路径即可
