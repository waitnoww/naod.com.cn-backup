---
title: 使用python的turtle来画图
date: 2020-04-02 09:16:06
description: 测试开发用python-使用python的turtle来画图
tags:
- 测试开发
- python
- 测试工具开发
nav:
- 测试开发
categories:
- python-awesome
image: img/blog_img/python-turtle.png
---
首先是安装turtle包，安装教程[在这里](https://www.dengnao.com.cn/post/python-install-turtle-error.html)

然后开始画图吧

#### 默认窗口
源代码如下：
```
import turtle
import time


# 默认窗口
def new():
    turtle.dot(10, 'red')
    turtle.write('(0, 0), zfont = (8)')
    turtle.ht()
    # 这里sleep是为了让窗口展示时间延长，大家可以自由调整
    time.sleep(5)

if __name__ == "__main__":
    new()
```
运行结果：
![默认窗口](https://tva1.sinaimg.cn/large/00831rSTgy1gdf5vlle31j30v30u0jsj.jpg)

#### 画个简版太阳
源代码如下：
```
import turtle
import time


# 太阳
def sun():
    turtle.color('red')
    turtle.penup()
    turtle.goto(250, 200)
    turtle.pendown()
    turtle.begin_fill()
    turtle.circle(50)
    turtle.end_fill()
    turtle.color('black', 'blue')
    turtle.begin_fill()
    # 这里sleep是为了让窗口展示时间延长，大家可以自由调整
    time.sleep(5)

if __name__ == "__main__":
    sun()
```
运行结果：
![默认窗口](https://tva1.sinaimg.cn/large/00831rSTgy1gdf5xzn7mwj30uy0u00tc.jpg)

#### 画纸飞机
源代码如下：
```
import turtle
import time


# 飞机
def plane():
    turtle.penup()
    turtle.home()
    turtle.pendown()
    turtle.pensize(5)
    turtle.goto(-300, 150)
    turtle.goto(100, 50)
    turtle.goto(0, 0)
    turtle.end_fill()
    turtle.goto(-30, -125)
    turtle.goto(-50, -50)
    turtle.begin_fill()
    turtle.goto(-300, 150)
    turtle.goto(-125, -125)
    turtle.goto(-50, -50)
    turtle.goto(-30, -125)
    turtle.goto(-85, -85)
    turtle.end_fill()
    # 这里sleep是为了让窗口展示时间延长，大家可以自由调整
    time.sleep(5)

if __name__ == "__main__":
    plane()
```
运行结果：
![默认窗口](https://tva1.sinaimg.cn/large/00831rSTgy1gdf60i8g1cj30v90u0jsl.jpg)

#### 画线条
源代码如下：
```
import turtle
import time


# 线条
def lines():
    turtle.pensize(3)
    turtle.penup()
    turtle.goto(75, 25)
    turtle.pendown()
    turtle.goto(200, 0)
    turtle.penup()
    turtle.goto(50, -5)
    turtle.pendown()
    turtle.goto(250, -30)
    turtle.penup()
    turtle.goto(10, -80)
    turtle.pendown()
    turtle.goto(100, -150)
    turtle.penup()
    turtle.goto(-80, -125)
    turtle.pendown()
    turtle.goto(120, -200)
    turtle.ht()
    # 这里sleep是为了让窗口展示时间延长，大家可以自由调整
    time.sleep(5)

if __name__ == "__main__":
    lines()
```
运行结果：
![默认窗口](https://tva1.sinaimg.cn/large/00831rSTgy1gdf61rb8tyj30uv0u0t98.jpg)


#### 画小猪佩奇
源代码如下：
```
import turtle as t


# 小猪佩奇
def pig():
    t.pensize(4)
    t.hideturtle()
    t.colormode(255)
    t.color((255, 155, 192), "pink")
    t.setup(840, 500)
    t.speed(10)

    # 鼻子
    t.pu()
    t.goto(-100, 100)
    t.pd()
    t.seth(-30)
    t.begin_fill()
    a = 0.4
    for i in range(120):
        if 0 <= i < 30 or 60 <= i < 90:
            a = a + 0.08
            t.lt(3)  # 向左转3度
            t.fd(a)  # 向前走a的步长
        else:
            a = a - 0.08
            t.lt(3)
            t.fd(a)
            t.end_fill()

    t.pu()
    t.seth(90)
    t.fd(25)
    t.seth(0)
    t.fd(10)
    t.pd()
    t.pencolor(255, 155, 192)
    t.seth(10)
    t.begin_fill()
    t.circle(5)
    t.color(160, 82, 45)
    t.end_fill()

    t.pu()
    t.seth(0)
    t.fd(20)
    t.pd()
    t.pencolor(255, 155, 192)
    t.seth(10)
    t.begin_fill()
    t.circle(5)
    t.color(160, 82, 45)
    t.end_fill()

    # 头
    t.color((255, 155, 192), "pink")
    t.pu()
    t.seth(90)
    t.fd(41)
    t.seth(0)
    t.fd(0)
    t.pd()
    t.begin_fill()
    t.seth(180)
    t.circle(300, -30)
    t.circle(100, -60)
    t.circle(80, -100)
    t.circle(150, -20)
    t.circle(60, -95)
    t.seth(161)
    t.circle(-300, 15)
    t.pu()
    t.goto(-100, 100)
    t.pd()
    t.seth(-30)
    a = 0.4
    for i in range(60):
        if 0 <= i < 30 or 60 <= i < 90:
            a = a + 0.08
            t.lt(3)  # 向左转3度
            t.fd(a)  # 向前走a的步长
        else:
            a = a - 0.08
            t.lt(3)
            t.fd(a)
            t.end_fill()

    # 耳朵
    t.color((255, 155, 192), "pink")
    t.pu()
    t.seth(90)
    t.fd(-7)
    t.seth(0)
    t.fd(70)
    t.pd()
    t.begin_fill()
    t.seth(100)
    t.circle(-50, 50)
    t.circle(-10, 120)
    t.circle(-50, 54)
    t.end_fill()

    t.pu()
    t.seth(90)
    t.fd(-12)
    t.seth(0)
    t.fd(30)
    t.pd()
    t.begin_fill()
    t.seth(100)
    t.circle(-50, 50)
    t.circle(-10, 120)
    t.circle(-50, 56)
    t.end_fill()

    # 眼睛
    t.color((255, 155, 192), "white")
    t.pu()
    t.seth(90)
    t.fd(-20)
    t.seth(0)
    t.fd(-95)
    t.pd()
    t.begin_fill()
    t.circle(15)
    t.end_fill()

    t.color("black")
    t.pu()
    t.seth(90)
    t.fd(12)
    t.seth(0)
    t.fd(-3)
    t.pd()
    t.begin_fill()
    t.circle(3)
    t.end_fill()

    t.color((255, 155, 192), "white")
    t.pu()
    t.seth(90)
    t.fd(-25)
    t.seth(0)
    t.fd(40)
    t.pd()
    t.begin_fill()
    t.circle(15)
    t.end_fill()

    t.color("black")
    t.pu()
    t.seth(90)
    t.fd(12)
    t.seth(0)
    t.fd(-3)
    t.pd()
    t.begin_fill()
    t.circle(3)
    t.end_fill()

    # 腮
    t.color((255, 155, 192))
    t.pu()
    t.seth(90)
    t.fd(-95)
    t.seth(0)
    t.fd(65)
    t.pd()
    t.begin_fill()
    t.circle(30)
    t.end_fill()

    # 嘴
    t.color(239, 69, 19)
    t.pu()
    t.seth(90)
    t.fd(15)
    t.seth(0)
    t.fd(-100)
    t.pd()
    t.seth(-80)
    t.circle(30, 40)
    t.circle(40, 80)

    # 身体
    t.color("red", (255, 99, 71))
    t.pu()
    t.seth(90)
    t.fd(-20)
    t.seth(0)
    t.fd(-78)
    t.pd()
    t.begin_fill()
    t.seth(-130)
    t.circle(100, 10)
    t.circle(300, 30)
    t.seth(0)
    t.fd(230)
    t.seth(90)
    t.circle(300, 30)
    t.circle(100, 3)
    t.color((255, 155, 192), (255, 100, 100))
    t.seth(-135)
    t.circle(-80, 63)
    t.circle(-150, 24)
    t.end_fill()

    # 手
    t.color((255, 155, 192))
    t.pu()
    t.seth(90)
    t.fd(-40)
    t.seth(0)
    t.fd(-27)
    t.pd()
    t.seth(-160)
    t.circle(300, 15)
    t.pu()
    t.seth(90)
    t.fd(15)
    t.seth(0)
    t.fd(0)
    t.pd()
    t.seth(-10)
    t.circle(-20, 90)

    t.pu()
    t.seth(90)
    t.fd(30)
    t.seth(0)
    t.fd(237)
    t.pd()
    t.seth(-20)
    t.circle(-300, 15)
    t.pu()
    t.seth(90)
    t.fd(20)
    t.seth(0)
    t.fd(0)
    t.pd()
    t.seth(-170)
    t.circle(20, 90)

    # 脚
    t.pensize(10)
    t.color((240, 128, 128))
    t.pu()
    t.seth(90)
    t.fd(-75)
    t.seth(0)
    t.fd(-180)
    t.pd()
    t.seth(-90)
    t.fd(40)
    t.seth(-180)
    t.color("black")
    t.pensize(15)
    t.fd(20)

    t.pensize(10)
    t.color((240, 128, 128))
    t.pu()
    t.seth(90)
    t.fd(40)
    t.seth(0)
    t.fd(90)
    t.pd()
    t.seth(-90)
    t.fd(40)
    t.seth(-180)
    t.color("black")
    t.pensize(15)
    t.fd(20)

    # 尾巴
    t.pensize(4)
    t.color((255, 155, 192))
    t.pu()
    t.seth(90)
    t.fd(70)
    t.seth(0)
    t.fd(95)
    t.pd()
    t.seth(0)
    t.circle(70, 20)
    t.circle(10, 330)
    t.circle(70, 30)
    t.done()


if __name__ == "__main__":
    pig()
```
运行结果：
![默认窗口](https://tva1.sinaimg.cn/large/00831rSTgy1gdf65qid7cj31ag0ssmyf.jpg)

开始玩耍吧。