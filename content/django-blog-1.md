---
title: 如何用Django搭建一个博客[一]
date: 2019-07-08 13:55:16
description: Django博客搭建教程-如何用Django搭建一个博客[一]
tags:
- 博客建设
- 其他
nav:
- 博客建设
categories:
- Django博客搭建
image: img/blog_img/django1.png
---

1. 克隆项目到本地
```
https://github.com/waitnoww/www.dengnao.com.cn
```
2. 创建并激活虚拟环境

   在命令行进入到保存虚拟环境的文件夹，输入如下命令创建并激活虚拟环境：

   ```
   virtualenv blogproject_env

   # windows
   blogproject_env\Scripts\activate

   # linux
   source blogproject_env/bin/activate
   ```


3. 安装项目依赖

   如果使用了虚拟环境，确保激活并进入了虚拟环境，在命令行进入项目所在的 django-blog-tutorial 文件夹，运行如下命令：

   ```
   pip install -r requirements.txt
   ```

4. 迁移数据库

   在上一步所在的位置运行如下命令迁移数据库：

   ```
   python manage.py migrate
   ```

5. 创建后台管理员账户

   在上一步所在的位置运行如下命令创建后台管理员账户

   ```
   python manage.py createsuperuser
   ```


6. 运行开发服务器

   在上一步所在的位置运行如下命令开启开发服务器：

   ```
   python manage.py runserver
   ```

   在浏览器输入：127.0.0.1:8000

7. 进入后台发布文章

   在浏览器输入：127.0.0.1:8000/admin

   使用第 5 步创建的后台管理员账户登录

8. enjoy it！


