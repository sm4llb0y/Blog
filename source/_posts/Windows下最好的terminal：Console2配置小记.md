title: Windows下最好的terminal：Console2配置小记
date: 2014-05-15 15:08:40
tags: Console2, Terminal, Console
categories: 编程
---

Console2是本人用过的windows下最好的Terminal Tools经过简单的配置之后更是用起来更加顺手。

<!--more-->


1.  下载安装[Console2](http://sourceforge.net/projects/console/)与[Putty](http://www.putty.org)
2.  配置Console
    ![Appearance](/images/posts/Console2_config_1.jpg)
    ![more...](/images/posts/Console2_config_2.jpg)
3.  设置颜色，替换掉Console.xml中相应的片段
    <code>
    <colors>
        <color id="0" r="7" g="54" b="66"/>
        <!-- black -->
        <color id="1" r="38" g="139" b="210"/>
        <!-- blue -->
        <color id="2" r="133" g="153" b="0"/>
        <!-- green -->
        <color id="3" r="42" g="161" b="152"/>
        <!-- cyan -->
        <color id="4" r="220" g="50" b="47"/>
        <!-- red -->
        <color id="5" r="211" g="54" b="130"/>
        <!-- magenta -->
        <color id="6" r="181" g="137" b="0"/>
        <!-- yellow/brown -->
        <color id="7" r="238" g="232" b="213"/>
        <!-- white -->
        <color id="8" r="0" g="43" b="54"/>
        <!-- brblack -->
        <color id="9" r="131" g="148" b="150"/>
        <!-- brblue -->
        <color id="10" r="88" g="110" b="117"/>
        <!-- brgreen -->
        <color id="11" r="147" g="161" b="161"/>
        <!-- brcyan -->
        <color id="12" r="203" g="75" b="22"/>
        <!-- brred -->
        <color id="13" r="108" g="113" b="196"/>
        <!-- brmagenta/violet -->
        <color id="14" r="101" g="123" b="131"/>
        <!-- bryellow -->
        <color id="15" r="253" g="246" b="227"/>
        <!-- brwhite  -->
    </colors>
    </code>
4.  为putty添加ANSI设置，下载[ANSICON](https://github.com/adoxa/ansicon/downloads)，解压响应的dll与exe到Console2根目录：
    >ANSI32.dll
    >ANSI64.dll
    >ansicon.exe
5.  设置启动alias脚本，在Console2根目录新建start.cmd，内容是你想要使用的alias command，例如：
    >doskey pt=C:\Programs\Console2\ansicon.exe "C:\Program Files (x86)\PuTTY\plink.exe" -load $*
6.  最终效果
    ![最终效果](/images/posts/Console2_running.jpg)

**Reference:**
> 1. http://blog.jimueller.com/post/29709142253/use-putty-with-console2
> 2. http://superuser.com/questions/594688/console2-run-command-on-start
> 3. http://superuser.com/questions/49170/create-an-alias-in-windows-xp
> 4. http://www.curlybrace.com/words/2012/02/12/console2-and-cygwin-with-solarized-color-palette/

**-本文完-**