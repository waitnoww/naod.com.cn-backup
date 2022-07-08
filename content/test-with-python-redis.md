---
title: python操作redis
date: 2020-03-10 10:02:30
description: 测试开发用python-python操作redis
tags:
- 测试开发
- python
- 测试工具开发
nav:
- 测试开发
categories:
- python-awesome
image: img/blog_img/python3.png
---
## 安装redis 模块
```
pip3 install redis
```
## 连接redis
```
# -*- coding: UTF-8 -*-
# 引入redis模块
import redis

# 连接redis
r = redis.Redis(host='redis_host', port='redis_host','password': 'redis_password',  decode_responses=True)  

```
## 不同redis数据类型操作
### string类型操作
> string类型在redis中存储格式为按照一个name对应一个value来存储的
```
# 插入key为python，value为helloworld的
r.set('python','helloworld')
# 查询刚才插入的key值
print(r.get('python'))
# 修改key为python的value为helloworld1
r.set('python','helloworld1')
# 删除插入的key值
r.delete('python')
```
### hash类型操作
> hash类型在redis中存储格式为(name,key,value)

- hget(name,key)：获取hash中的value
- hset(name,key,value)：在name对应的hash中设置一个键值对，不存在则创建否则修改
- hmset(name,mapping)：在name对应的hash中批量设置键值对
- hmget(name,keys,*args)：获取过个hash的key的值

- hgetall(name)：获取hash的所有键值对

- hlen(name)：获取hash中键值对的个数

- hkeys(name)：获取hash中所有keys的值

- hvals(name):获取hash中所有value的值

- hexists(name,key)：检查hash中是否存在key

- hdel(name,*key)：删除hash中的key
  
```
# 插入name为python，key为3.8，value为3.8.1的hash值
r.hset('python','3.8','3.8.1')
# 查询刚才插入的key值
print(r.hgetall('python'))
# 修改name为python key为3.8的value为3.8.2
r.hset('python','3.8','3.8.2')
# 删除插入的key值
r.hdel('python','3.8')
```
### list类型操作
> 待补充
### set类型操作
> 待补充
