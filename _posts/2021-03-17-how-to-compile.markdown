---
layout: post
title:  "如何编译带应用过滤的OpenWrt固件"
date:   2021-03-16 09:03:30 -0800
categories: appfilter
---

[源码地址](https://github.com/destan19/OpenAppFilter)

{% highlight ruby %}
下载OpenWrt源码
git clone https://github.com/coolsnowwolf/lede.git
cd package
git clone https://github.com/destan19/OpenAppFilter.git
cd -
make menuconfig
选择luci-app-oaf
然后make V=99 生成应用过滤固件

{% endhighlight %}


OpenWrt刷机教程可以关注公众号获取

![](/assets/img/qrcode-openwrt.jpg)