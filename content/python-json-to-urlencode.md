---
title: python3下json串转urlencode
date: 2020-03-18 09:33:42
description: 测试开发用python-python把json串转urlencode
tags:
- 测试开发
- python
- 测试工具开发
nav:
- 测试开发
categories:
- python-awesome
image: img/blog_img/python5.png
---
昨天在编写一个python自动化脚本时，其中一个需求是把json串进行urlencode，看起来很简单的操作
想要的结果是：
```
{"name":"dengnao","pwd":"123456"}
```
转换如下：
```
%7B%22name%22%3A%22dengnao%22%2C%22pwd%22%3A%22123456%22%7D
```

常规首先的代码如下：
![截图1](https://tva1.sinaimg.cn/large/00831rSTgy1gcxu9mgjy7j30s20i6wgn.jpg)
运行结果为：
```
name=dengnao&pwd=123456
```
看起来没有满足结果

尝试使用urllib.parse.quote

![截图2](https://tva1.sinaimg.cn/large/00831rSTgy1gcxuho6gloj30v20i2mza.jpg)
直接报错了
```
    test = urllib.parse.quote(json_data)
  File "/Users/waitnoww/opt/anaconda3/lib/python3.7/urllib/parse.py", line 834, in quote
    return quote_from_bytes(string, safe)
  File "/Users/waitnoww/opt/anaconda3/lib/python3.7/urllib/parse.py", line 859, in quote_from_bytes
    raise TypeError("quote_from_bytes() expected bytes")
TypeError: quote_from_bytes() expected bytes
```
百度一波后，才发现quote必须是字符串
```
urllib.quote(s, safe='/')
接受参数s为字符串，safe是指定某字符不被urlencode，默认为'/'，
```
那就把传入的json串转成字符串
![截图3](https://tva1.sinaimg.cn/large/00831rSTgy1gcxur6io13j30uq0hagnv.jpg)
运行结果如下：
```
%7B%22name%22%3A%20nn%2C%20%22pwd%22%3A%20%22123456%22%7D
```
确实urlencode了，但是name并没有参数化
再来参数化代码
![截图5](https://tva1.sinaimg.cn/large/00831rSTgy1gcxuvu8u89j30vk0he40q.jpg)
运行结果如下：
```
%7B%22name%22%3A%20dengnao%2C%20%22pwd%22%3A%20%22123456%22%7D
```
还是对不上,对应的name参数没有加引号，再改一波代码
![截图6](https://tva1.sinaimg.cn/large/00831rSTgy1gcxuyxagc6j30vy0i276i.jpg)
终于得到正确的运行结果
```
%7B%22name%22%3A%22dengnao%22%2C%22pwd%22%3A%22123456%22%7D
```

