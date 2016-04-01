title: Google CDN（jsapi, fonts等）被墙问题解决
date: 2016-03-31 12:22:56
tags: Raspberry Pi, Pi
categories: 
---
首次打开Raspberry Pi的浏览器访问中文网站的时候，所有的中文字符都会显示为方块，且无法输入中文。解决方法如下：
<!--more-->

1. 安装中文字体和输入法：
    sudo apt-get update
    sudo apt-get install ttf-wqy-zenhei
    sudo apt-get install scim-pinyin

2. 然后运行下面的命令打开Raspberry Pi的设置，选择Locale为zh_CN.UTF-8
    sudo raspi-config

3. 重启验证显示问题解决，并且能够通过Ctrl+Space切换输入法