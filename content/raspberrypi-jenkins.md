---
title: 在RaspberryPi上安装Jenkins
date: 2020-05-24 09:40:00
description: 在RaspberryPi上安装Jenkins
tags:
- 测试工具
- 测试相关
- jenkins
- raspberrypi
nav: 
- 测试工具
categories:
- jenkins
image: img/blog_img/raspberry-jenkins.png
---

## 安装Java
```
pi@raspberrypi:~ $ java -version
java version "1.8.0_65"
Java(TM) SE Runtime Environment (build 1.8.0_65-b17)
Java HotSpot(TM) Client VM (build 25.65-b01, mixed mode)
```
## 安装Jenkins
```
pi@raspberrypi:~ $ wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
OK
pi@raspberrypi:~ $ sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
pi@raspberrypi:~ $ sudo apt-get update
Ign http://pkg.jenkins.io binary/ InRelease
Get:1 http://mirrordirector.raspbian.org jessie InRelease [15.0 kB]
Get:2 http://pkg.jenkins.io binary/ Release.gpg [181 B]
Get:3 http://pkg.jenkins.io binary/ Release [2,042 B]
Get:4 http://archive.raspberrypi.org jessie InRelease [22.9 kB]
Get:5 http://mirrordirector.raspbian.org jessie/main armhf Packages [9,539 kB]
Get:6 http://pkg.jenkins.io binary/ Packages [14.7 kB]
Get:7 http://archive.raspberrypi.org jessie/main armhf Packages [170 kB]
Ign http://pkg.jenkins.io binary/ Translation-en_GB
Ign http://pkg.jenkins.io binary/ Translation-en
Get:8 http://archive.raspberrypi.org jessie/ui armhf Packages [58.9 kB]
Ign http://archive.raspberrypi.org jessie/main Translation-en_GB
Ign http://archive.raspberrypi.org jessie/main Translation-en
Ign http://archive.raspberrypi.org jessie/ui Translation-en_GB
Ign http://archive.raspberrypi.org jessie/ui Translation-en
Hit http://mirrordirector.raspbian.org jessie/contrib armhf Packages
Get:9 http://mirrordirector.raspbian.org jessie/non-free armhf Packages [88.2 kB]
Hit http://mirrordirector.raspbian.org jessie/rpi armhf Packages
Ign http://mirrordirector.raspbian.org jessie/contrib Translation-en_GB
Ign http://mirrordirector.raspbian.org jessie/contrib Translation-en
Ign http://mirrordirector.raspbian.org jessie/main Translation-en_GB
Ign http://mirrordirector.raspbian.org jessie/main Translation-en
Ign http://mirrordirector.raspbian.org jessie/non-free Translation-en_GB
Ign http://mirrordirector.raspbian.org jessie/non-free Translation-en
Ign http://mirrordirector.raspbian.org jessie/rpi Translation-en_GB
Ign http://mirrordirector.raspbian.org jessie/rpi Translation-en
Fetched 9,911 kB in 10min 54s (15.1 kB/s)
Reading package lists... Done
pi@raspberrypi:~ $ sudo apt-get install jenkins
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following extra packages will be installed:
  daemon
The following NEW packages will be installed:
  daemon jenkins
0 upgraded, 2 newly installed, 0 to remove and 20 not upgraded.
Need to get 76.8 MB of archives.
After this operation, 77.6 MB of additional disk space will be used.
Do you want to continue? [Y/n]
Get:1 http://mirrordirector.raspbian.org/raspbian/ jessie/main daemon armhf 0.6.4-1 [80.9 kB]
Get:2 http://pkg.jenkins.io/debian-stable/ binary/ jenkins 2.164.2 [76.7 MB]
Fetched 76.8 MB in 15s (4,904 kB/s)
Selecting previously unselected package daemon.
(Reading database ... 165286 files and directories currently installed.)
Preparing to unpack .../daemon_0.6.4-1_armhf.deb ...
Unpacking daemon (0.6.4-1) ...
Selecting previously unselected package jenkins.
Preparing to unpack .../jenkins_2.164.2_all.deb ...
Unpacking jenkins (2.164.2) ...
Processing triggers for man-db (2.7.5-1~bpo8+1) ...
Processing triggers for systemd (215-17+deb8u11) ...
Setting up daemon (0.6.4-1) ...
Setting up jenkins (2.164.2) ...
Processing triggers for systemd (215-17+deb8u11) ...
```
## 启动Jenkins
```
pi@raspberrypi:~ $ sudo /etc/init.d/jenkins start
Correct java version found
[ ok ] Starting jenkins (via systemctl): jenkins.service.
```
## 浏览器登录127.0.0.1:8080

![](https://raw.githubusercontent.com/waitnoww/hexoblogimg/master/img1/20200524215014.png)

## 复制密码
```
pi@raspberrypi:~ $ sudo cat /var/lib/jenkins/secrets/initialAdminPassword
11d12b7daad44e8daf93778c23e89a81
```
## Tips:
```
安装插件的时候，遇到一些报错，解决方法是勾选“Use browser for metadata download”选项。Go To ->Manage Jenkins -> Configure Global Security -> Plugin Manager and check the box for Use browser for metadata download.
```
## 开始你的树莓派jenkins之旅吧

