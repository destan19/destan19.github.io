---
layout: page
title: 特征库下载
permalink: /feature/
---

#### 特征库列表：

{% assign feature_files = site.static_files | where: "oaf", true %}
{% for feature in feature_files %}
 [{{feature.name}}]({{ feature.path }})
{% endfor %}

#### 更新日志
#### 2021.04.09
增加原神、秦时明月、天涯明月刀

#### 2021.04.01
增加阴阳师、狼人杀、小森生活、使命召唤、欢乐麻将


OpenWrt刷机教程可以关注公众号获取

![](/assets/img/qrcode-openwrt.jpg)