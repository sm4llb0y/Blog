title: 制作Mac OSX安装U盘
date: 2016-04-08 00:49:07
tags: Mac, Mac OSX
---

以下以El Capitan为例，其他系统类似：

1. 准备好App（就是app store下载的最新OS X El Capitan）和U盘（大于8G）
2. 格式化U盘：`实用工具》磁盘工具》抹掉》名字MyVolume》格式OS X 扩展（日志式）》方案GUID分区图`
3. 运行命令：`sudo /Applications/Install\ OS\ X\ El\ Capitan.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume --applicationpath /Applications/Install\ OS\ X\ El\ Capitan.app`
4. 等待终端输出Done.，完成制作：
```
Password:
Ready to start.
To continue we need to erase the disk at /Volumes/Toshiba.
If you wish to continue type (Y) then press return: Y
Erasing Disk: 0%... 10%... 20%... 30%...100%...
Copying installer files to disk...
Copy complete.
Making disk bootable...
Copying boot files...
Copy complete.
Done.
```