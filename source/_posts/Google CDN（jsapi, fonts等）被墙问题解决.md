title: Google CDN（jsapi, fonts等）被墙问题解决
date: 2016-03-31 12:42:56
tags: Raspberry Pi, Pi
categories: 
---
Google的隔离导致许多引用了Google CDN上包括字体，jsapi以及常用第三方库的网页会一直等待被墙的响应，直至其失败后才继续后面的加载，解决方法如下：
<!--more-->

1. 如果是你自己的网站，这个相对容易考虑直接替换相应的链接为360或者中科大的镜像，或者自己host需要的库文件：
    googleapis.com 替换为 lug.ustc.edu.cn / useso.com

    注：360的镜像不支持Https，如果是Https建议使用中科大的镜像

2. 如果是别人的网站请直接翻墙，如无法翻墙请安装国内网友的插件[ReplaceGoogleCDN](https://github.com/justjavac/ReplaceGoogleCDN)，如果你有什么特殊需求请直接git clone修改后再安装自己的定制版。
