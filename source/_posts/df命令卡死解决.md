title: df命令卡死解决
date: 2016-04-11 23:04:01
tags: df,nfs,linux,mount
---
如果挂载的文件系统无法访问，df命令就会卡住，这个时候就需要墙纸卸载挂载点。
<!--more-->

1. 先检查挂载的文件系统 `mount | column -t`
2. 比如极有可能是NFS服务器关了，这边客户端就会卡死，这个时候就需要强制卸载`umount -fl /mnt`
3. 如果发现正忙，杀死所有占用的进程：`fuser -uck /mnt`
4. umount完后再重新挂载即可：`mount -t nfs Server:/data /mnt`