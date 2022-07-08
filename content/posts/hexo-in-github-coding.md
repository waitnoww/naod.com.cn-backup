---
title: hexo同时托管在github和coding
date: 2020-03-08 13:55:16
description: hexo博客搭建教程-hexo博客同时托管在github和coding
tags:
- 博客建设
- 其他
nav:
- 博客建设
categories:
- hexo博客搭建
image: img/blog_img/hexo1.png
---
#### 前提：
- 已拥有hexo博客
- 已拥有github仓库
- 已拥有coding page仓库
#### 1。修改配置文件
找到hexo目录下站点配置文件 _config.yml
```
deploy:
  type: git
  repo:
      github: https://github.com/waitnoww/waitnoww.github.com.git,master
      coding: https://git.coding.net/waitnoww/www.dengnao.com.cn.git,coding-pages
```
#### 2.hexo安装部署插件：
```
    npm install hexo-deployer-git --save
```
#### 3.尝试一下
```
hexo clean
hexo g
hexo d
```