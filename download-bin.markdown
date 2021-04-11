---
layout: page
title: 固件下载
permalink: /download-bin/
---

[固件发布说明](/assets/oaf/bin/README.txt)

发布的固件集成了应用过滤功能，但固件不会一一测试，如果升级或刷机遇到的问题与发布者无关。  
如果这里没有你想要的固件，可以去恩山论坛搜索OpenWrt应用过滤固件  
以下为恩山论坛集成了应用过滤的帖子，可以选择自己合适的固件  
- https://www.right.com.cn/forum/thread-4049182-1-2.html
- https://www.right.com.cn/forum/thread-4066849-1-1.html

红米AC2100:

{% assign bins = site.static_files | where: "ac2100", true %}
{% for bin in bins %}
 [{{bin.name}}]({{ bin.path }})

{% endfor %}

X86:


{% assign bins = site.static_files | where: "bin_x86", true %}
{% for bin in bins %}
 [{{bin.name}}]({{ bin.path }})

{% endfor %}


Newifi3:

{% assign bins = site.static_files | where: "newifi3", true %}
{% for bin in bins %}
 [{{bin.name}}]({{ bin.path }})


{% endfor %}
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

{% assign bins = site.static_files | where: "k2p", true %}
{% for bin in bins %}
 [{{bin.name}}]({{ bin.path }})


{% endfor %}


7621系列:

{% assign bins = site.static_files | where: "bin_mt7621", true %}
{% for bin in bins %}
 [{{bin.name}}]({{ bin.path }})
{% endfor %}


R2S:

敬请期待

OpenWrt刷机教程可以关注公众号获取

![](/assets/img/qrcode-openwrt.jpg)
