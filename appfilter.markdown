---
layout: page
title: 简介
permalink: /appfilter/
---

{% assign imgs = site.static_files | where: "oaf_image", true %}
{% for img in imgs %}
![Alt text]({{ img.path }})

{% endfor %}


![](/assets/img/qrcode-openwrt.jpg)