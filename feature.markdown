---
layout: page
title: 特征库下载
permalink: /feature/
---

特征库列表：

{% assign feature_files = site.static_files | where: "oaf", true %}
{% for feature in feature_files %}
 [{{feature.name}}]({{ feature.path }})
{% endfor %}

OpenWrt刷机教程可以关注公众号获取

![](/assets/img/qrcode-openwrt.jpg)