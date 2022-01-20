---
layout: post
title:  "breed下升级OpenWrt固件"
date:   2022-01-20 20:03:30 -0800
categories: appfilter
---


### 如何给路由器刷breed
要想给路由器刷breed，需要先破解进入路由器ssh后台，每款路由器方式不一样，大家可以去恩山无线论坛查找自己路由器教程。

![](https://gitee.com/destan19/picture/raw/master/picgo/202201201000959.png)

刷入breed教程非常多，也比较容易，但是有些设备通过breed刷入openwrt却有点麻烦，教程也相对较少。

### openwrt镜像说明
我们要通过breed刷openwrt固件首先必须要知道openwrt各种镜像的用途，一般一个型号的设备包含多个openwrt镜像，比如kernel镜像、upgrade镜像等。

以下为红米AC2100路由器的OpenWrt镜像列表，包含四个文件

![](https://gitee.com/destan19/picture/raw/master/picgo/202201191558855.png)

作为新手你可能不知道如何选择镜像进行升级

官方也对这四种镜像做了简单解释，是通过文件名来区分的。

![](https://gitee.com/destan19/picture/raw/master/picgo/202201191556521.png)


这里来讲这四种镜像在实际刷机过程中的使用方法

- kernel镜像
具有最少文件系统的Linux内核，包含只读文件系统，也就是说升级该镜像后，配置是不能保存的。一般在breed下先升级该镜像，作为中间固件，然后再升级sysupgrade镜像。因为大部分小米路由器在breed下不能直接升级sysupgrade镜像，需要先升级kernel镜像。

- kernel1镜像
linux内核单独镜像，在首次刷机会用到，一般通过mtd命令写入。

- rootfs0镜像
文件系统镜像，包含linux系统的配置文件、进程等，在首次刷机会用到，一般通过mtd命令写入。

- sysupgrade镜像
系统升级固件，也是最常用的镜像，用于通过web页面升级，sysupgrade镜像是包含了linux内核和文件系统的。
如果出现sysupgrade镜像格式不对，但是型号确实没问题，这可能是openwrt新旧版本的问题，这时候就需要通过breed升级。

**breed升级固件说明**
一般刷机都会刷入breed不死uboot，这样路由器就永不变砖，除非手残刷错uboot。
我自己也买了一些设备进行了测试，通过breed刷入老毛子固件还是很方便，不需要额外修改参数，但是通过breed刷openwrt固件就有点麻烦了。

这里给大家大概总结下：
k2p、newifi3等固件一般直接可以通过breed升级，比较方便
小米系列路由器通过breed升级固件比较麻烦，需要先升级中间固件（kernel镜像），并且需要设置环境变量xiaomi.r3g.bootfw，比如红米ac2100需要设置xiaomi.r3g.bootfw的值为2，小米的其他设备也类似。

![](https://gitee.com/destan19/picture/raw/master/picgo/202201191638350.png)

**升级详细步骤(红米AC2100)**
1. 准备一台刷好breed的红米AC2100路由器
2. 按住reset键重启设备，发现灯快闪几下后松开
3. 电脑连接设备，浏览器访问192.168.1.1进入breed界面
4. 添加环境变量xiaomi.r3g.bootfw，值设置为2，只有设置后才能正确引导openwrt系统
5. 升级中间固件
在breed菜单的"固件更新"中选择发布版本的kernel镜像升级
openwrt-ramips-mt7621-xiaomi_redmi-router-ac2100-initramfs-kernel.bin

6. 升级upgrade镜像
进入openwrt中间固件后台，通过web选择sysupgrade镜像直接升级即可

openwrt-ramips-mt7621-xiaomi_redmi-router-ac2100-squashfs-sysupgrade.bin

升级完成后最好恢复下出厂，防止残留老固件配置。







