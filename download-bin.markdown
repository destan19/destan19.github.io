---
layout: page
title: 固件下载
permalink: /download-bin/
---

[固件发布说明](/assets/oaf/bin/README.txt)

红米AC2100:

{% assign bins = site.static_files | where: "ac2100", true %}
{% for bin in bins %}
 [{{bin.name}}]({{ bin.path }})

{% endfor %}

X86:
文件过大，请在网盘下载
链接：https://eyun.baidu.com/s/3deIrSE 密码：29At

GL-MT1300:

{% assign bins = site.static_files | where: "mt1300", true %}
{% for bin in bins %}
 [{{bin.name}}]({{ bin.path }})


{% endfor %}



7620系列:

{% assign bins = site.static_files | where: "bin_mt7620", true %}
{% for bin in bins %}
 [{{bin.name}}]({{ bin.path }})
{% endfor %}

K2P:

敬请期待

R2S:

敬请期待

OpenWrt刷机教程可以关注公众号获取

![](/assets/img/qrcode-openwrt.jpg)
