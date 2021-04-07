---
layout: page
title: 特征库下载
permalink: /feature/
---

列表中的feature.cfg为当前最新的特征库文件
由于app会有重复的特征码，会出现误判，这是不可避免的，提类似的问题将不处理


特征库列表：

{% assign feature_files = site.static_files | where: "oaf", true %}
{% for feature in feature_files %}
 [{{feature.name}}]({{ feature.path }})
{% endfor %}

OpenWrt刷机教程可以关注公众号获取

![](/assets/img/qrcode-openwrt.jpg)