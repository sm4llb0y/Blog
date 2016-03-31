title: AutoIt简明教程
date: 2013-10-25 23:42:40
tags: AutoIt, 脚本, 控制程序
categories: 编程
---

AutoIt正如下面官网[wiki](http://www.autoitscript.com/wiki/AutoIt_Introduction)介绍：

>AutoIt v3 is a freeware BASIC-like scripting language designed for automating the Windows GUI and general scripting. It uses a combination of simulated keystrokes, mouse movement and window/control manipulation in order to automate tasks in a way not possible or reliable with other languages (e.g. VBScript and SendKeys). AutoIt is also very small, self-contained and will run on all versions of Windows out-of-the-box with no annoying "runtimes" required! 

它是一种类似BASIC语法的用于windows GUI自动化的脚本语言，它可以模拟键盘按键，鼠标移动等达到自动化任务的目的，优点包括短小精悍、自包含并且可以不需要任何运行时环境在所有版本的windows中运行。

<!--more-->

下面以打开系统属性对话框然后点击“确定”按钮关闭为例进行简单介绍AutoIt的开发过程：

1. 下载安装[AutoIt V3](http://www.autoitscript.com/files/autoit3/autoit-v3-setup.exe)
2. 打开“系统属性”对话框，利用“AutoIt Window Info”(开始->AutoIt V3->AutoIt Window Info)查看对话框的title以及按钮ID

![AutoIt](/images/posts/AutoIt.png)

3. 可以看到对话框的title为“系统属性”，确定按钮的ID为1
4. 打开任意文本编辑器编写代码如下，另存为system.au3

		Run("Control Sysdm.cpl") 		#打开系统属性对话框
		WinWait("系统属性")				#等待启动完成	
		ControlClick("系统属性", "", 1)	#点击确定按钮关闭

5. 运行查看结果

最后关于AutoIt的详细文档，请查阅官方文档（开始->AutoIt V3->AutoIt Help File），另外请查看官方的Example（AutoIt3\Examples）进行快速入门。

![AutoIt Help](/images/posts/AutoIt_Help.png)

马上试着自己去写一些有用的脚本吧！

**-本文完-**