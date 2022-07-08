---
title: python使用163邮箱发邮件
date: 2020-03-09 16:14:11
description: 测试开发用python-python使用163邮箱发邮件
tags:
- 测试开发
- python
- 测试工具开发
nav:
- 测试开发
categories:
- python-awesome
image: img/blog_img/python2.png
---
```
# -*- coding: UTF-8 -*-

# 引入邮件对象
import smtplib
from email.header import Header
from email.mime.text import MIMEText

# 设置163邮箱的smtp服务
# 邮箱发送地址
sender = 'python@163.com'
# 设置发送邮箱密码(163为授权码)
password = 'python'
# 设置邮件接收地址
receivers = 'python@qq.com'
# 设置163服务器地址
server_host = 'smtp.163.com'

# 邮件正文
msg = MIMEText('hello, send from Python...', 'plain', 'utf-8')
msg['From'] = sender
msg['To'] = receivers
# 邮件标题
msg['Subject'] = Header('python脚本邮件', 'utf-8').encode()

try:
    server = smtplib.SMTP_SSL(server_host, 465)
    # 开启邮件服务操作日志 1为开启 0为关闭
    server.set_debuglevel(0)
    server.login(sender, password)
    server.sendmail(sender, [receivers], msg.as_string())
    server.quit()
    print '哈哈好，邮件发送成功了'
except Exception as e:
    print ('Exception: 嘤嘤嘤，邮件发送失败了', e)
    
```