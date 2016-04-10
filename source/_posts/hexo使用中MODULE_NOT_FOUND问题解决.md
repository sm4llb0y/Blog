title: hexo使用中MODULE_NOT_FOUND问题解决
date: 2016-04-10 00:49:07
tags: Hexo
---

运行hexo命令的时候报如下错误：

```bash
{ [Error: Cannot find module './build/Release/DTraceProviderBindings'] code: 'MODULE_NOT_FOUND' }
{ [Error: Cannot find module './build/default/DTraceProviderBindings'] code: 'MODULE_NOT_FOUND' }
{ [Error: Cannot find module './build/Debug/DTraceProviderBindings'] code: 'MODULE_NOT_FOUND' }
```
<!--more-->

可以加--no-optional参数重新安装一下hexo即可：
```bash
$ npm install hexo -g --no-optional
```