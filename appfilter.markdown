---
layout: page
title: 软件截图
permalink: /appfilter/
---

{% assign imgs = site.static_files | where: "oaf_image", true %}
{% for img in imgs %}
![Alt text]({{ img.path }})

{% endfor %}

OpenWrt刷机教程可以关注公众号获取

![](/assets/img/qrcode-openwrt.jpg)