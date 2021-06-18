---
layout: page
title: 特征库下载
permalink: /feature/
---

特征库更新是一项繁琐的工作，要持续更新
如果没有你想要过滤的app，可以加v订制
linux4096(备注：特征码订制)

#### 特征库列表：

{% assign feature_files = site.static_files | where: "oaf", true %}
{% for feature in feature_files %}
 [{{feature.name}}]({{ feature.path }})
{% endfor %}




OpenWrt刷机教程可以关注公众号获取

![](/assets/img/qrcode-openwrt.jpg)